# Speech Synthesis and Translation via Exemplar Autoencoders
In this report, we presented a way to make our target speaker utter any translated content in a language where one has never spoken while maintaining the target speaker's voice and appropriate accent for the language.

### Audiosynthesis part
Audiosynthesis_Obama.ipynb and Audiosynthesis_Oprah.ipynb show getting target speaker features. Also, they show voice conversion graphs when opened in Colab.

### Translation part
We benefit from ESPnet and Multilingual TTS papers for the translation part

translation_audiosynthesis.ipynb shows how we generated outputs in the Translation_project (From English speech input to French speech output with target speaker voice)

Obama's voice convergence loss
<img width="978" alt="Obama_loss" src="https://user-images.githubusercontent.com/60038634/113201994-80cc6680-926a-11eb-8c93-dc9bc881b481.png"　width="1200">


Oprah's voice convergence loss
<img width="1002" alt="Oprah_loss" src="https://user-images.githubusercontent.com/60038634/113202034-8de95580-926a-11eb-8bd3-ede26ceb4538.png" width="1200">
