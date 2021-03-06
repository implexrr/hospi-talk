# Hospi-Talk #
This project was created during a 36-hour hackathon in March of 2021. I was responsible for designing the app/UI, project management and training HospiTalk to recognize sign language via a KNN model in TensorFlow.js.

# Inspiration #
This project was inspired by a friend of mine who works at St Michael’s hospital in Toronto - he frequently has to communicate with deaf patients, and often has difficulty doing so. In a healthcare setting, where clarity, accuracy and speed are of paramount importance, it is vital that a clear form of communication is accessible to disadvantaged populations such as the hearing impaired. To address this problem, we built a web-app that allows for quick and easy communication between hearing impaired individuals and hospital staff using American Sign Language.

# What it does #
Once the hospital worker, i.e. a receptionist, sees or hears the converted ASL, they can respond to the hearing impaired individual via the bottom right text box. Note that both the hearing impaired individual and the hospital worker would see the exact same screen.

# How we built it #
HospiTalk’s sign language translator was built using a KNN (K-Nearest Neighbors) module in TensorFlow.js. The TensorFlow model was generated by Google's Teachable Machine. The module creates a classifier via the KNN algorithm. I chose KNN over the alternative CNN/RNN options since it was lightweight and easy to use, which was ideal for this initial prototype. The UI of HospiTalk was built using Vue 2.0 alongside Vuetify for bootstrapped components. Our app was hosted via Netlify.

Challenges
One challenge that our team ran into was that HospiTalk would interpret unwanted words in between gestures, which generated incoherent phrases. We fixed this by making sure the sign language was only translated after a certain threshold counter was reached for each word. Since our model interprets the webcam data roughly 10 times per second, we made it so that a word would only go through to the text/speech box if the webcam interpreted that word 5 consecutive times (in other words, for 0.5 seconds).

We’re proud that we managed to create a project that improved accessibility to communication for a vital disadvantaged population. Given that this was the ever first hackathon for 3 of our group members (including me), the whole thing went a lot smoother than expected. We’re also happy that we managed to collaborate well and utilize each group member’s strength to their fullest, which allowed us to achieve our goals efficiently.
We learnt quite a bit about different machine learning models and what each of them are used for. We also learned a lot about frontend JavaScript development using a modern MVC framework. Most importantly, we had a chance to understand more of the difficulties those with disabilities often face.

# What's next for HospiTalk #
We intend on improving HospiTalk in several ways. Since we only had 36 hours to come up with the idea and train our model, we only had time to teach HospiTalk approximately 20 words. We plan on drastically increasing this number in the future. We would also like to modify this project so that it can be used outside of a healthcare setting, since there are many other situations where accessibility to communication for the hearing impaired is an issue.

Additionally, the model has only been trained on one person, the presenter, so in its current state, it inconsistently recognizes the gestures of others. We would expand our model to be trained on a diverse group of people, provided additional time and resources.

[![Watch the video](https://img.youtube.com/vi/5SsZTOIk9Ns/maxresdefault.jpg)](https://youtu.be/5SsZTOIk9Ns)
Try it out: https://hospitalk.netlify.app/
