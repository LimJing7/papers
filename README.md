# Papers I read
- Through the Valley: Path to Effective Long CoT Training for Small Language Models
    - Renjie Luo, Jiaxi Li, Chen Huang, Wei Lu
    - StatNLP Group, SUTD
    - reasoning traces lead to performance drop first before recovery
        - ![fig 2 (llama 3.1 section)](images/through_the_valley/fig2_llama3.1_8b.png)
    - length of response decrease as more examples are seen
        - model learns more than superficial copying
    - using reasoning traces for cold start is good but enough SFT needs to be done
        - ![fig 7](images/through_the_valley/fig7.png)
