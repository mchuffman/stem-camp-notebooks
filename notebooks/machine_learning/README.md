# Machine learning notebooks

In 2020, making these notebooks compatible with [colab](https://colab.research.google.com/)

This folder has a few sub-folders:
- [01_Naive_Bayes](01_Naive_Bayes) has lessons on **probability** and **statistics**, as well as **Bayes' Rule** and the **Naive Bayes classifier**.  This is useful
- [02_Logistic_Regression](02_Logistic_Regression) is about **logistic regresion**. I don't think we usually cover this.
- [03_Optimization](03_Optimization) is about **optimization** and **stochastic gradient descent**.  I don't think we usually cover this.
- [data](data) contains helper files for other scripts, so no need to look at this directly
- [object_detection](object_detection) has the [object detection demo](object_detection/object_detection_tutorial.ipynb). I don't think we usually cover This

## Individual notebooks
### Start with these
- [Intro Classification.ipynb](Intro%20Classification.ipynb)
  - Uses scikit-learn to explore **k-nearest-neighbors** and **decision trees**
  - You might want to first see the [Decision_Tree_Lesson.pdf](Decision_Tree_Lesson.pdf)

- [Intro Regression.ipynb](Intro%20Regression.ipynb)
  - Building height example
  - [08_Linear_Regression_Bias_Variance.ipynb](08_Linear_Regression_Bias_Variance.ipynb)

### Supplemental notebooks
- [clustering_and_image_quantization.ipynb](clustering_and_image_quantization.ipynb)
  - This is a demo of using kmeans clustering to quantize an image. At the end, it shows the outputs of different classifiers on the half-moons 2D dataset.
- [Unsupervised Learning.ipynb](Unsupervised%20Learning.ipynb)
    - This is about **kmeans** and visually shows how it works, but most of the coding is already done for you

- [MNIST_classifier.ipynb](MNIST_classifier.ipynb)
  - This is a project where you train a **support vector machine (SVM)** on MNIST data (or use a pretrained one), then right your own digits on the computer, and see if the classifier can tell which digit you wrote.  Unfortunately this requires a bit of manual work, as you need to save your image and get it onto jupyterhub/colab, so this works best if you can run Python locally on your own computer.

- [Fingerprint Classification.pdf](Fingerprint%20Classification.pdf) is a presentation about classifying fingerprints
