# generative video repository
A repo of generative video method paper

Year 2018

March
1. Probabilistic Video Generation using Holistic Attribute Control
     https://arxiv.org/pdf/1803.08085.pdf

       Videos express highly structured spatio-temporal patterns of visual data. 
       two factors: 
           (i) temporally invariant (e.g., person identity), or slowly varying (e.g., activity), attribute- induced 
           appearance, encoding the persistent content of each frame, and 
           (ii) an interframe motion or scene dynamics (e.g., encoding evolution of the person ex- ecuting the action). 
       VideoVAE
          - video generation + future prediction. 
          - generates a video (short clip) by:
              decoding samples sequentially drawn from a latent space distribution into full video frames.
              - VAE: encoding/decoding frames into/from the latent space 
              - RNN: model the dynamics in the latent space.     
          - improve the video generation consistency through temporally-conditional sampling and quality
              structuring the latent space with attribute controls
              ensuring that attributes can be both inferred and conditioned on during learning/generation

2.Learning to Generate Time-Lapse Videos Using Multi-Stage Dynamic Generative Adversarial Networks
    https://arxiv.org/pdf/1709.07592.pdf
 
 
 
3. Every Smile is Unique: Landmark-Guided Diverse Smile Generation
      https://arxiv.org/pdf/1802.01873.pdf

Year 2017
 By the Way I like this stanford homework paper
    http://cs231n.stanford.edu/reports/2017/pdfs/323.pdf
 

1. Dynamics Transfer GAN:  (Dec 2017)
     Generating Video by Transferring Arbitrary Temporal Dynamics from a Source Video to a Single Target Image
     https://arxiv.org/pdf/1712.03534.pdf

         - spatial constructs <---- target image; dynamics <------source video sequence
         - To preserve the spatial construct of the target image:
              - the appearance of the source video sequence is suppressed 
              - only the dynamics are obtained before being imposed onto the target image. 
                     (using the proposed appearance suppressed dynamics feature.)
         - the spatial and temporal consistencies are verified via two discriminator networks.  
               - discriminator A validates the fidelity of the generated frames appearance, 
               -  B validates the dynamic consistency of the generated video sequence. 
               
         - Results:
               - successfully transferred arbitrary dynamics of the source video sequence onto a target image 
               - maintained the spatial constructs (appearance) of the target image while generating spatially and   
                  temporally consistent video sequences.
         [图片]
         
         Note: It is ### everything (Literature Review in its intro) because it is quite new.
    @I didn't complete
    
2. Deep Video Generation, Prediction and Completion of Human Action Sequences
    https://arxiv.org/pdf/1711.08682.pdf
         
3. Video Generation from Text 
    https://arxiv.org/pdf/1710.00421.pdf
    Hybrid VAE plus GAN
    Two parts: Static( Using gist to sketch text-conditioned background color and object layout 
                     (LSTM, RNN structure)
               Dynamic ( A text2Filter. )
               [图片]
               
      3 parts in Model (Section 3) 
          - 3.1 Gist Generator
          - 3.2 Video Generator
          - 3.3 Text2Filter
      Note: Quite compact. Need time to digest
   
4. Learning to Generate Time-Lapse Videos Using Multi-Stage Dynamic Generative Adversarial Networks
   https://arxiv.org/pdf/1709.07592.pdf
   
5. MoCoGAN: Decomposing Motion and Content for Video Generation
    https://arxiv.org/pdf/1707.04993.pdf
   
6. To Create What You Tell: Generating Videos from Captions
     https://www.microsoft.com/en-us/research/wp-content/uploads/2017/11/BNI02-panA.pdf
 
         -Temporal GANs conditioning on Captions, namely TGANs-C
         
         - transformed into a frame sequence with 3D spatio-temporal convolutions. 
         -  GAM evaluation metric ( Section 3.4 Experimental Setting)
         -  Model Architecture 
              3.1.1 Generator 
                    Given a sentence 𝒮, a bi-LSTM is utilized to contextually embed the input word sequence, 
                    + a LSTM-based encoder to obtain the sentence representation S. 
                    + concatenated input of the sentence representation S and random noise variable z.
                     synthesize realistic videos with these
              3.1.2 The discriminator network 𝐷 includes three discriminators: 
                    a.video discriminator classifying realistic videos from generated+ optimizes video-caption matching           
                    b. frame discriminator( between real and fake frames)and aligning frames with the conditioning caption
                    c. motion discriminator emphasizing that the adjacent frames in the generated videos run smoothly 
              3.1.3 The whole part trained with 3 losses:
                    video-level matching-aware loss, frame-level matching-aware loss and temporal coherence loss 
                    
 
       
                    .
    Year 2016
                   
 1. Generating Videos with Scene Dynamics
      https://arxiv.org/abs/1609.02612
 
           - a spatio-temporal convolutional architecture 
           - untangles the scene’s foreground from the background. 
           - experiments show the model internally learns useful features for recognizing actions with minimal supervision,
           - scene dynamics are a promising signal for representation learning.
           [图片]
           Slides : https://pdfs.semanticscholar.org/presentation/7188/6726f0a1b4075a7213499f8f25d7c9fb4143.pdf
           
         
