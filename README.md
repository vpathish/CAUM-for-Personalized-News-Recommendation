# Candidate-Aware User Modeling for Personalized News Recommendation

Personalized news recommendations are challenging, requiring a deep understanding of the news items and the users. In this project, we improvised on a novel candidate-aware user modeling approach for personalized news recommendations based on the Microsoft Cognitive Toolkit (CNTK). Our approach considers the candidate news items when modeling user interests, which allows us to generate more accurate and relevant recommendations. We have evaluated our approach on a large-scale real-world dataset, and the results show that our approach outperforms several state-of-the-art baselines regarding recommendations accuracy and relevance. THe results also show that the approach can generate more diverse recommendations than the baselines. The candidate-aware user modeling approach is a
promising new approach for personalized news recommendations. The approach can be used to improve the accuracy and relevance of news recommendations and the diversity of the recommendations.

## Acknowledgments

This project is a fork of the [Original Project](https://github.com/taoqi98/CAUM/), authored by [Tao Qi](https://github.com/taoqi98), which is based on the paper:

> Tao Qi, Fangzhao Wu, Chuhan Wu, and Yongfeng Huang. "News Recommendation with Candidate-aware User Modeling." In Proceedings of the 45th International ACM SIGIR Conference on Research and Development in Information Retrieval (SIGIR’22), July 11–15, 2022, Madrid, Spain. ACM, New York, NY, USA, 5 pages. DOI: [10.1145/3477495.3531778](https://doi.org/10.1145/3477495.3531778).

We would like to acknowledge and thank the original authors for their contributions. The major update and modification we've made to the original code include replacing TensorFlow with CNTK as the backend for the deep learning framework.

## Prerequisites

Before you begin, ensure you have met the following requirements:
- Anaconda: Download and Install the Latest Version of Anaconda from [Anaconda's website](https://www.anaconda.com/distribution/).
- GPU Support: Ensure you have a compatible NVIDIA GPU to take advantage of CNTK.
- Download the MINDLarge 'Training Set' and 'Test Set' Datasets from [Microsoft News Dataset](https://msnews.github.io).
- Download the Pre-Trained Word Vectors of [Common Crawl (840B tokens, 2.2M vocab, cased, 300d vectors)](https://huggingface.co/stanfordnlp/glove/resolve/main/glove.840B.300d.zip) by [Stanford NLP](https://github.com/stanfordnlp/GloVe).

  
## Setup & Usage

1. **Clone the repository:**
   ```bash
   git clone https://github.com/vpathish/CAUM-for-Personalized-News-Recommendation.git

2. **Extract the required datasets and embeddings:**
  - Extract the `MINDlarge_test.zip` and `MINDlarge_train.zip` datasets downladed from [Microsoft News Dataset](https://msnews.github.io) in the project's `code` folder.
  - Extract `glove.840B.300d.txt` file from the downloaded `glove.840B.300d.zip` Archive to the project's `code` folder

The Project Folder Structure should like the following after extracting
```
CAUM-for-Personalized-News-Recommendation/
├── code/
│   ├── MINDlarge_test/
│   │   ├── behaviors.tsv
│   │   ├── news.tsv
│   │   ├── ... (other dataset files)
│   ├── MINDlarge_train/
│   │   ├── behaviors.tsv
│   │   ├── news.tsv
│   │   ├── ... (other dataset files)
│   ├── glove.840B.300d.txt
│   ├── Generator.py
│   ├── Hypers.py
│   ├── Main.ipynb
│   ├── Models.py
│   ├── Preprocessing.py
│   ├── Utils.py
├── .gitignore
├── README.md
├── requirement.txt

```

3. Open Anaconda Prompt

4. Create a conda environment for the project:
   ```bash
   conda create --name caum-env python=3.6.10

5. Activate the conda environment:
   ```bash
   conda activate caum-env

6. Navigate to the Project Directory

7. Install Jupyter:
   ```bash
   conda install jupyter

8. Install other project dependencies:
   ```bash
   pip install -r requirements.txt

9. Start Jupyter Notebook.
   ```bash
   jupyter notebook

10. Run the `main.ipynb` file 


## **Disclaimer:**
This project is based on the work of [Tao Qi, Fangzhao Wu, Chuhan Wu, and Yongfeng Huang](https://doi.org/10.1145/3477495.3531778) and their [News Recommendation with Candidate-aware User Modeling](https://github.com/taoqi98/CAUM/). We do not have permission to repost or distribute the original code. Please refer to the original repository for their code and licensing terms.

Our project builds upon the original work by making specific modifications, such as replacing TensorFlow with CNTK, to improve efficiency. For any questions or issues related to the original code, please contact the original author.

We would like to express our gratitude to the original author for their contributions to the open-source community.

## **Contact Information:**

For any questions or issues related to this project, you can reach out to us:

- [Athish Venkatachalam](mailto:athishv@clemson.edu)
- [Mohan Krishna G](mailto:mgunda@clemson.edu)
