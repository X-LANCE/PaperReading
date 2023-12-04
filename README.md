# 各研究方向经典论文
## ASR
- E2E based ASR
    
    CTC: https://www.cs.toronto.edu/~graves/icml_2006.pdf
    
    Attention based ASR: https://arxiv.org/pdf/1508.01211.pdf
    
    CTC+Attention: https://arxiv.org/pdf/1609.06773.pdf
    
    RNN-T: https://arxiv.org/pdf/1211.3711.pdf
    
    RNN-T+: https://arxiv.org/pdf/1303.5778.pdf
    
    Streaming RNN-T: https://arxiv.org/pdf/1811.06621.pdf?fbclid=IwAR3Ya9ZfBNN40UO0wct7dGupjlBFEpU47IRHK-wXmejI4U2UQGf03sXHMlw.I
    
    T-T: https://arxiv.org/abs/2002.02562 ;  https://arxiv.org/abs/1910.12977
    
    Streaming T-T: https://arxiv.org/abs/2010.11395
    
    Factorized T-T: https://arxiv.org/abs/2110.01500
    
    Transducer in Espnet: https://arxiv.org/pdf/2201.05420.pdf
    
- Review
    
    E2E review:  https://arxiv.org/abs/2111.01690
    
- Streaming LAS
    
    Trigger Attention: https://www.merl.com/publications/docs/TR2019-015.pdf
    
    Online and Linear-Time Attention by Enforcing Monotonic Alignments: https://arxiv.org/abs/1704.00784
    
    MoCha: https://arxiv.org/abs/1712.05382
    
    Monotonic Infinite Lookback Attention for Simultaneous Machine Translation”: https://arxiv.org/abs/1906.05218
    
- Latency optimization
    
    Fastemit:  https://arxiv.org/abs/2010.11148
    
- AM/LM Adaptation
    
    Density Ratio: https://arxiv.org/abs/2002.11268  → HAT; ILMT; ILME
    
    Fast adapt: https://arxiv.org/abs/2104.11127
    
    Factorized T-T: https://arxiv.org/abs/2110.01500
    
    MetaAdapter： https://arxiv.org/pdf/2105.11905.pdf
    
    PERSONALIZATION STRATEGIES FOR END-TO-END SPEECH RECOGNITION SYSTEMS: https://arxiv.org/abs/2102.07739
    
    IMPROVED NEURAL LANGUAGE MODEL FUSION FOR STREAMING RECURRENT NEURAL NETWORK TRANSDUCER: https://arxiv.org/abs/2010.13878
    
- Entity Recognition
    - 2018
        - Deep context: end-to-end contextual speech recognition: https://arxiv.org/abs/1808.02480
            - baseline：
                
                contextual LM；
                
                $$
                C=\min(\det(S\circ G))
                $$
                
                no weight pushing；only applied at word boundaries
                
                weight pushing at the beginning subword; over-biasing
                
                pushing weights to each subword unit
                
                bias-encoder
                
                grapheme
                
            - bias-encoder
                - feeding the bias-encoder with the sequence of embeddings of subwords
                - the last state of the LSTM
                - h0 is no bias
            - Attention: 和一般的有点不一样
                
                ![image.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/653baa22-35e6-4b68-b917-374a1e5689ab/image.png)
                
            - Every time a match is found a special </bias> symbol is inserted after the match
            - Bias-Conditioning：
                - a list of bias prefixes
                - a bias phrase is “enabled” at step t only when p_i was detected
            - TTS for test data
        - Contextual Speech Recognition in End-to-End Neural Network Systems using Beam Search: https://www.isca-speech.org/archive_v0/Interspeech_2018/pdfs/2416.pdf
            
            基本上就是shallow fusion
            
            grapheme
            
    - 2019
        - END-TO-END CONTEXTUAL SPEECH RECOGNITION USING CLASS LANGUAGE MODELS AND A TOKEN PASSING DECODER: https://arxiv.org/abs/1812.02142
            
            class based LM + token passing
            
            Q：如何解决LAS给异常输入后的抽风？grapheme抽风较弱？
            
        - Contextual Speech Recognition with Difficult Negative Training Examples: https://arxiv.org/abs/1810.12170
            
            sample proper nouns
            
            phonetically similar names such as john and jean as negative examples
            
            grapheme
            
        - Joint Grapheme and Phoneme Embeddings for Contextual End-to-End ASR: https://x-lance.sjtu.edu.cn/papers/2019/zhc00-chen-is2019.pdf
            
            CLAS框架，在bias embeding提取上
            
            A、更换提取方式为BLSTM；avg/concat第一个hidden和最后一个hidden
            
            B、引入phone
            
        - Phoneme-Based Contextualization for Cross-Lingual Speech Recognition in End-to-End Models: https://arxiv.org/abs/1906.09292
            
            shallow fusion
            
            phone mapping for Cross-Lingual
            
        - Shallow-Fusion End-to-End Contextual Biasing: https://www.isca-speech.org/archive_v0/Interspeech_2019/pdfs/1209.pdf
            
            backoff; before beam pruning; wordpiece level; including a prefix; data augment (Proper Noun; Unsupervised; Synthesize; Fuzzing Transcript)
            
    - 2020
        - Contextualizing ASR Lattice Rescoring with Hybrid Pointer Network Language Model: https://arxiv.org/abs/2005.07394
            
            meta data → multiple words; attention on each h_i; 
            
            rare in training data → 有一定概率直接选context里面的word
            
            ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/02a1b998-b011-4478-8137-1df86b3ff815/Untitled.png)
            
        - Contextual RNN-T for open domain ASR: https://arxiv.org/abs/2006.03411
            
            基本就是CLAS
            
        - Rapid RNN-T Adaptation Using Personalized Speech Synthesis and Neural Language Generator: https://indico2.conference4me.psnc.pl/event/35/contributions/3010/attachments/649/680/Mon-3-7-3.pdf
            
            NLG+TTS+finetune
            
        - Class lm and word mapping for contextual biasing in end-to-end asr: https://arxiv.org/abs/2007.05609
            
            训练输入中插入class start/end；推理时当预测出class start，进入FST，走到end state；输出class end；打分有些trick，basepath和ctx path
            
            通过字典，把相同发音的词map成同样的BPE
            
            （输入拼音，很有必要）
            
            18.1 → 9.0
            
        
        Hierarchical Multi-Stage Word-to-Grapheme Named Entity Corrector for Automatic Speech Recognition: https://www.isca-speech.org/archive_v0/Interspeech_2020/pdfs/3174.pdf
        
        Improving proper noun recognition in end-to-end asr by customization of the mwer loss criterion: https://arxiv.org/abs/2005.09756
        
    - 2021
        
        Deep Shallow Fusion for RNN-T Personalization: https://arxiv.org/abs/2011.07754
        
        A Light-weight contextual spelling correction model for customizing transducer-based speech recognition systems: https://arxiv.org/abs/2108.07493
        
        Improving RNN-T for Domain Scaling Using Semi-Supervised Training with Neural TTS: https://www.isca-speech.org/archive/pdfs/interspeech_2021/deng21_interspeech.pdf
        
        Contextual Density Ratio for Language Model Biasing of Sequence to Sequence ASR Systems: https://www.isca-speech.org/archive/pdfs/interspeech_2021/andresferrer21_interspeech.pdf
        
        End to End Transformer-Based Contextual Speech Recognition Based on Pointer Network: https://www.isca-speech.org/archive/pdfs/interspeech_2021/lin21e_interspeech.pdf
        
        Have best of both worlds: two-pass hybrid and E2E cascading framework for speech recognition: https://arxiv.org/abs/2110.04891
        
        Instant One-Shot Word-Learning for Context-Specific Neural Sequence-to-Sequence Speech Recognition: https://arxiv.org/abs/2107.02268
        
        Fast Contextual Adaptation with Neural Associative Memory for On-Device Personalized Speech Recognition: https://arxiv.org/abs/2110.02220
        
        Spell my name: keyword boosted speech recognition: https://arxiv.org/pdf/2110.02791.pdf
        
        Contextualized Streaming End-to-End Speech Recognition with Trie-Based Deep Biasing and Shallow Fusion: https://arxiv.org/abs/2104.02194
        
        CIF-based Collaborative Decoding for End-to-end Contextual Speech Recognition: https://arxiv.org/abs/2012.09466
        
        Tree-constrained Pointer Generator for End-to-end Contextual Speech Recognition: https://arxiv.org/abs/2109.00627
        
- MOE
