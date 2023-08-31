# TimeGAN-for-ecgs
My implementation of TimeGAN using PyTorch. <br/>I applied it to generate synthetic ECGs, and evaluated the signals obtained with data utility and privacy preservation metrics.

---
### What is TimeGAN?

TimeGAN is a model proposed by Jinsung Yoon et al. in a paper called [Time-series Generative Adversarial Networks](https://proceedings.neurips.cc/paper_files/paper/2019/file/c9efe5f26cd17ba6216bbe2a7d26d490-Paper.pdf).

Time series data is challenging for classical GANs due to the potentially complex temporal correlations of variables: the model must capture the distributions of features within each time point, but also the stepwise conditional distributions across time. TimeGAN provides a framework that combines the conventional unsupervised GAN training method with a supervised learning approach, in order to generate time series with preserved temporal dynamics. 

The original paper open-sources a [TensorFlow implementation](https://github.com/vanderschaarlab/mlforhealthlabpub/tree/820ccf22d85bdce2e3f1211f84bf3b276016d9d6/alg/timegan), which I used as reference.

---
### Additional contributions

I used TimeGAN for a practical application: generating synthetic ECG signals, and evaluating them.<br/>
ECG data was taken from the [MIT-BIH Arrythmia Database](https://www.physionet.org/content/mitdb/1.0.0/).

Here are the evaluation metrics used:
- Data utility
    - Inception score
    - Distance between samples
    - PCA and t-SNE visualization
    - Discriminative score
    - Cross-classification
- Privacy-preservation
    -  Identifiability
    - Membership Inference Attack

---
### Visualizing Results

Here are some real signals, and synthetic signals created by TimeGAN.
<p align="center">
<img src="/images/real (1).png" width="500"/>
</p>

<p align="center">
<img src="/images/fake_timegan (1).png" width="500"/>
</p>

---
### Code

💻 [TimeGAN](https://nbviewer.jupyter.org/github/HelenaFP/TimeGAN-for-ecgs/blob/main/TimeGAN_train_and_evaluate_pynb.ipynb)<br/>
💻 [Exploratory Data Analysis](https://nbviewer.jupyter.org/github/HelenaFP/TimeGAN-for-ecgs/blob/main/ECG_dataset_exploratory_data_analysis.ipynb)
