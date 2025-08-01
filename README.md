# Papers I read

## LLM
- Through the Valley: Path to Effective Long CoT Training for Small Language Models
    - Renjie Luo, Jiaxi Li, Chen Huang, Wei Lu
    - StatNLP Group; SUTD
    - reasoning traces lead to performance drop first before recovery
        - ![fig 2 (llama 3.1 section)](images/through_the_valley/fig2_llama3.1_8b.png)
    - length of response decrease as more examples are seen
        - model learns more than superficial copying
    - using reasoning traces for cold start is good but enough SFT needs to be done
        - ![fig 7](images/through_the_valley/fig7.png)

- Long-Short Alignment for Effective Long-Context Modeling in LLMs
    - Tianqi Du, Haotian Huang, Yifei Wang, Yisen Wang
    - State Key Lab of General AI, Peking University; NUS; MIT CSAIL; Institute for AI, Peking University
    - Idea: Modify Output space of model
    - long-short misalignment
        - new metric to measure differences in output entropy
        - symmetrical cross-entropy between different truncations of a long input
            - ? but the truncated info might be relevant?
            - used as a generalization technique so maybe it's ok in the general case?
        - uses a cute packing method to more optimally compute the loss
            - seq = 0-a-b-end
            - s1 = 0-b
            - s2 = a-end
            - misalignment loss computed at position b
    - this mtd improves close context while not seeming to lead to performance degradation for referring to distant context
        - ![tab 5](images/long_short_alignment/tab5.png)

## Chem
- An evaluation methodology for machine learning-based tandem mass spectra similarity prediction
    - Michael Strobel, Alberto Gil-de-la-Fuente, Mohammad Reza Zare Shahneh, Yasin El Abiead, Roman Bushuiev, Anton Bushuiev, Tomáš Pluskal, Mingxun Wang
    - UC Riverside, Universidad CEU San Pablo, UC San Diego, IOCB Prague, Czech Institute of Informatics, Robotics and Cybernetics
    - [harmonized MC/MC datasets (LC? / GC?)](https://external.gnps2.org/gnpslibrary)
        - 189,467 spectra from 28,132 structures
