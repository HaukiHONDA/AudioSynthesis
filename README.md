# Speech Synthesis and Translation via Exemplar Autoencoders
In this report, we presented a way to make our target speaker utter any translated content in a language where one has never spoken while maintaining the target speaker's voice and appropriate accent for the language.

### Audiosynthesis part
Audiosynthesis_Obama.ipynb and Audiosynthesis_Oprah.ipynb show getting target speaker features. Also, they show voice conversion graphs when opened in Colab.

### Translation part
We benefit from ESPnet and Multilingual TTS papers for the translation part

translation_audiosynthesis.ipynb shows how we generated outputs in the Translation_project (From English speech input to French speech output with target speaker voice)

### Data Pipeline and Foundation
For the translation part, we have a pretrained model on the Librispeech dataset which contains 236 hours of English read speech with its corresponding text in English and French translation. And moreover we added the English to spanish pretrained model based on the Fisher and Callhome spanish dataset as the multilingual translation choice. The Fisher and Callhome spanish dataset contains 170-hours of Spanish read speech with its corresponding Spanish text transcription and English text. 

For Audiosynthesis, we have about 47 minutes audio of Barack Obama [https://www.youtube.com/watch?v=ji6pl5Vwrvk], about 11 minutes audio of Bill Clinton’s speech [ https://www.youtube.com/watch?v=eYTq8MOIJvo] and about 50 minutes audio of Oprah Winfrey[https://www.youtube.com/watch?v=GR_7X0exvh8]. We trained the targeted speaker model with 2000 iterations of batch-size 8 and epochs 10. As the machine setting, we used the Google Colab pro for the experiment. So we could access either T4 or P100GPU with high memory. 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/gist/HaukiHONDA/8ecbdf97314aad8ff92d2acef1754816/29-march_obama_02.ipynb)


### Obama's voice convergence loss
<img width="500" alt="Obama_loss" src="https://user-images.githubusercontent.com/60038634/113201994-80cc6680-926a-11eb-8c93-dc9bc881b481.png">


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/gist/HaukiHONDA/ad1a63158902b3e30435e72f50ebaf4c/29-march_oprah_02.ipynb)

### Oprah's voice convergence loss
<img width="500" alt="Oprah_loss" src="https://user-images.githubusercontent.com/60038634/113202034-8de95580-926a-11eb-8bd3-ede26ceb4538.png">
