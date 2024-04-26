

# Multilingual Speaker Identification and Verification

The following work was done as part of the minor project for the course CSL7770: Speech Understanding

![1714166078406](https://github.com/KhadgaA/Speaker-Identification/assets/110987239/3ab32103-093b-4a9e-a1cc-7e82a7cb3497)

The project was done as a team with the help of [Khadga Jyoth Alli](https://github.com/KhadgaA), [Manish Vutkoori](https://github.com/ManishHyd), and [Bikram Majhi](https://github.com/bikrammajhi). The project's main aim is to use classical speech processing techniques paired with classical machine learning models to recognize the speaker based on their voice sample correctly. However the main crux of the project lies on the dataset used. To achieve our goal of multilingual speaker identification and verification we need a robust dataset which represesnts real life sceneriaos, like how most of us are bilingual and we subconciously mix two languages together while speaking, this way of speaking feels natural to most of us, some examples are provided below:

> ```
> 1. मुझे  birthday party  के लिए क्या पहनना चाहिए, I can't decide!
> 2. ఈ రోజు  traffic  చాలా ఎక్కువగా ఉంది, we might be late.
>
> ```
>
> To see all transcripts that we used, look at [Speech_transcrips](./speech_minor1_transcripts.md)

## Multilingual Audio Dataset

We collected the multilingual audio data from 20 people, out of which 9 were female and 11 were male and from each person we collected 10 audio samples, out of which 5 audio samples were in Hindi + English and 5 were in their native language + English. The reason for collecting 5 Hindi + English samples from all the participants is that, we observed that everyone here spoke Hindi and English, so we added it as a baseline. The full details of the languages used and number of audio samples collected are given below.

> **Audio Sample Format Description (eg: Aayushi_E_1.m4a)**
>
> Format = `<Name>_<lang>_<idx>.m4a`

| Language    | Samples | People                                                                                       | Examples                                                                          |
| ----------- | ------- | -------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Hindi (E)   | 10      | Aayushi, Abhishek, Arsh, Bikram, Kushal, Mohit,<br />Nachiketa, Deboleena, Swati, Yashmitha | [1](./Speech%20Recordings/Aayushi_E_1.m4a), [2](./Speech%20Recordings/Abhishek_E_6.m4a) |
| Telugu (T)  | 5 + 5   | Datta, Jyothi, Khadga, Manish                                                               | [1](./Speech%20Recordings/Jyothi_T_2.m4a), [2](./Speech%20Recordings/Khadga_E_4.m4a)    |
| Marathi (M) | 5 + 5   | Aditi, Arnav, Manaswi                                                                       | [1](./Speech%20Recordings/Arnav_M_2.m4a), [2](./Speech%20Recordings/Aditi_E_3.m4a)      |
| Bengali (B) | 5 + 5   | Deepraj, Dipan, Ritobina                                                                     | [1](./Speech%20Recordings/Dipan_B_4.m4a), [2](./Speech%20Recordings/Ritobina_E_2.m4a)   |

# Voice Patterns observed in Male Vs Female Voices

![mohit](https://github.com/KhadgaA/Speaker-Identification/assets/110987239/a0e5c303-4f3c-44c4-a838-2cb060df2e3d)![Arsh](https://github.com/KhadgaA/Speaker-Identification/assets/110987239/deabeaab-980e-47d9-8a4e-437c39b334f7)

The graphs represent the normalized dominant frequencies observed in the voice samples by male and female speakers. From the graphs it is evident that male voices have pronounced Lower dominant frequencies as compared to female voices. We consistently observe this trend in all our samples. All the plots can be seen in the [notebook](./speech_project_minor_identification.ipynb).

# Results
## Speaker Identification

| Classifier | Precision | Recall | F1-Score | Accuracy |
|------------|-----------|--------|----------|----------|
| KNeighborsClassifier | 0.41 | 0.43 | 0.39 | 0.43 |
| LogisticRegression | 0.63 | 0.65 | 0.64 | 0.65 |
| DecisionTreeClassifier | 0.70 | 0.68 | 0.66 | 0.68 |
| SVC | 0.97 | 0.97 | 0.97 | 0.97 |
| NuSVC | 0.97 | 0.97 | 0.97 | 0.97 |
| RandomForestClassifier | 0.97 | 0.97 | 0.97 | 0.97 |
| AdaBoostClassifier | 0.92 | 0.92 | 0.91 | 0.92 |
| GradientBoostingClassifier | 0.97 | 0.97 | 0.97 | 0.97 |
| SGDClassifier | 0.97 | 0.97 | 0.97 | 0.97 |
| GaussianNB | 0.89 | 0.82 | 0.82 | 0.82 |
| MultinomialNB | 0.98 | 0.98 | 0.98 | 0.98 |

## Speaker Verification
|EER| Threshold|
|--| --------- |
|0.0176 | 0.947 |



