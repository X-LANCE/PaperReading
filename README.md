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
    Deep context: end-to-end contextual speech recognition: https://arxiv.org/abs/1808.02480

    Contextual Speech Recognition in End-to-End Neural Network Systems using Beam Search: https://www.isca-speech.org/archive_v0/Interspeech_2018/pdfs/2416.pdf
  
    END-TO-END CONTEXTUAL SPEECH RECOGNITION USING CLASS LANGUAGE MODELS AND A TOKEN PASSING DECODER: https://arxiv.org/abs/1812.02142
            
    Contextual Speech Recognition with Difficult Negative Training Examples: https://arxiv.org/abs/1810.12170
            
    Joint Grapheme and Phoneme Embeddings for Contextual End-to-End ASR: https://x-lance.sjtu.edu.cn/papers/2019/zhc00-chen-is2019.pdf
            
    Phoneme-Based Contextualization for Cross-Lingual Speech Recognition in End-to-End Models: https://arxiv.org/abs/1906.09292
            
    Shallow-Fusion End-to-End Contextual Biasing: https://www.isca-speech.org/archive_v0/Interspeech_2019/pdfs/1209.pdf

    Contextualizing ASR Lattice Rescoring with Hybrid Pointer Network Language Model: https://arxiv.org/abs/2005.07394
            
    Contextual RNN-T for open domain ASR: https://arxiv.org/abs/2006.03411
            
    Rapid RNN-T Adaptation Using Personalized Speech Synthesis and Neural Language Generator: https://indico2.conference4me.psnc.pl/event/35/contributions/3010/attachments/649/680/Mon-3-7-3.pdf

    Class lm and word mapping for contextual biasing in end-to-end asr: https://arxiv.org/abs/2007.05609
            
    Hierarchical Multi-Stage Word-to-Grapheme Named Entity Corrector for Automatic Speech Recognition: https://www.isca-speech.org/archive_v0/Interspeech_2020/pdfs/3174.pdf
        
    Improving proper noun recognition in end-to-end asr by customization of the mwer loss criterion: https://arxiv.org/abs/2005.09756
        
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

## TTS

* Review

  A Survey on Neural Speech Synthesis: https://arxiv.org/pdf/2106.15561.pdf

* Spectrogram-based TTS

  \[Tacotron2\] Natural tts synthesis by conditioning wavenet on mel spectrogram predictions: https://arxiv.org/pdf/1712.05884.pdf
  
  Fastspeech 2: Fast and high-quality end-to-end text to speech: https://arxiv.org/pdf/2006.04558.pdf
  
  Glow-TTS: A Generative Flow for Text-to-Speech via Monotonic Alignment Search: https://proceedings.neurips.cc/paper/2020/file/5c3b99e8f92532e5ad1556e53ceea00c-Paper.pdf
  
  Grad-TTS: A Diffusion Probabilistic Model for Text-to-Speech: http://proceedings.mlr.press/v139/popov21a/popov21a.pdf
  
* End-to-end TTS

  \[VITS\] Conditional Variational Autoencoder with Adversarial Learning for End-to-End Text-to-Speech: http://proceedings.mlr.press/v139/kim21f/kim21f.pdf
  
  NaturalSpeech 2: Latent Diffusion Models are Natural and Zero-Shot Speech and Singing Synthesizers: https://arxiv.org/pdf/2304.09116.pdf
  
* VQ-based and GPT-based TTS

  VQTTS: High-Fidelity Text-to-Speech Synthesis with Self-Supervised VQ Acoustic Feature: https://arxiv.org/pdf/2204.00768.pdf
  
  \[VALLE\] Neural Codec Language Models are Zero-Shot Text to Speech Synthesizers: https://arxiv.org/pdf/2301.02111.pdf

* Vocoder

  MelGAN: Generative Adversarial Networks for Conditional Waveform Synthesis: https://proceedings.neurips.cc/paper/2019/file/6804c9bca0a615bdb9374d00a9fcba59-Paper.pdf
  
  HiFi-GAN: Generative Adversarial Networks for Efficient and High Fidelity Speech Synthesis: https://proceedings.neurips.cc/paper/2020/file/c5d736809766d46260d816d8dbc9eb44-Paper.pdf
  
  BigVGAN: A Universal Neural Vocoder with Large-Scale Training: https://arxiv.org/pdf/2206.04658.pdf

