# 🐶🐱 PRODIGY ML TASK-03: Cats vs Dogs Classification using SVM

## 📌 **Task Description**

Implement a **Support Vector Machine (SVM)** model to classify images of **cats and dogs** using the *Kaggle Dogs vs Cats dataset*.

Dataset Used: [https://www.kaggle.com/c/dogs-vs-cats/data](https://www.kaggle.com/c/dogs-vs-cats/data)

---

## 📂 **Project Structure**

```
ML_Task3/
│── train.zip                 # Kaggle dataset
│── ML_TASK3.ipynb            # Colab Notebook
│── README.md                 # Project documentation
```

---

## ⚙️ **Technologies Used**

* Python
* Google Colab
* OpenCV
* scikit-image (HOG)
* scikit-learn (SVM)
* NumPy
* tqdm

---

## 🧠 **Approach**

Since SVM cannot be trained on raw images directly, we use **HOG (Histogram of Oriented Gradients)** to extract numerical features.

### ✔ Steps followed

1. Mounted Google Drive
2. Uploaded **train.zip** dataset
3. Extracted dataset in Colab
4. Preprocessed images (resize, grayscale)
5. Extracted HOG features
6. Converted data into NumPy arrays
7. Applied **train-test split (80/20)**
8. Trained SVM classifier (LinearSVC for speed)
9. Evaluated model accuracy
10. Tested model on external images

---

## 🛠️ **Feature Extraction (HOG)**

HOG is used to convert each image into a numeric feature vector.

* Resized each image to **128×128**
* Converted to grayscale
* HOG applied → produces **8100 features per image**

---

## 🤖 **Model: SVM (LinearSVC)**

We used **LinearSVC** instead of classic SVC due to:

* Faster training
* Less RAM usage
* Works better with high-dimensional HOG features

---

## 📊 **Results**

After training on 5000 samples:

* **Model Accuracy: ~60%**

### 🎯 Why accuracy is moderate?

* SVM is not ideal for image classification
* CNNs usually achieve 95%+, but SVM was required for this task

Still, the pipeline is fully correct and valid.

---

## 🖼️ **Testing on New Images**

A custom function was implemented to test any uploaded image:

* Upload image to `/content/`
* Pass its path into `predict_image()`
* Output: **Dog 🐶 / Cat 🐱**

---

## ✔️ **Conclusion**

This project successfully demonstrates:

* Image preprocessing
* Feature extraction using HOG
* Traditional ML classification with SVM
* Model evaluation and external image prediction

Although accuracy is moderate (~60%), the objective of implementing an SVM for image classification was fully achieved.

---

## 📌 **Future Improvements**

* Use **CNN (Convolutional Neural Networks)** for higher accuracy
* Apply PCA for dimensionality reduction
* Train on more samples

---

## ✨ **Author**

Mohit Vishwakarma
