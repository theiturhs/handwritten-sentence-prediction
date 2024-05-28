# Handwritten Sentence Prediction

This project is a comprehensive solution for recognizing handwritten digits and text from images, with functionalities for training, testing, and usage, making it suitable for tasks like cheque amount verification and other handwritten text recognition applications.

![Row wise and Column wise histogram](https://github.com/theiturhs/handwritten-sentence-prediction/assets/96874023/8c40abef-dde6-4def-9013-84746ebc8c82)


This project provides solution for extracting the letters and then predicting the sentence. For this, few assumptions are made:

1. The handwriting is not cursive.
2. The text is in english language only.
3. Written text is human-readable.

# Procedure

1. Training model for digit and character prediction using EMNIST and MNIST dataset available on Kaggle.
2. Histogram based segmentation to find out the characters and space between characters and words.
3. Prediction to decode the sentence

# Histogram based Segmentation

1. The original image is converted into binary image.
2. Column wise sum is calculated to figure out the coordinates where the main contents are present and where space is present.
3. Two type of spaces are detected: space between subsequent letters and space between words. These are termed as local space and global space respectively. A threshold value is set to distinguish between local and global space.
4. Row wise sum is calculated to remove any top or bottom space available.
5. The extracted contents are resized for prediction.
6. Model prediction is performed.

# Example

1. Binary Image

   ![Binary Image](https://github.com/theiturhs/handwritten-sentence-prediction/assets/96874023/5066ad97-735b-4671-9701-34a7fc26f3c3)

2. Column wise sum - Histogram: frequency vs total number of columns

   ![Histogram - Column wise](https://github.com/theiturhs/handwritten-sentence-prediction/assets/96874023/2f245fe9-44ab-4ac5-9fad-52c18306dd38)

3. Extracted Characters

   ![Extracted Characters](https://github.com/theiturhs/handwritten-sentence-prediction/assets/96874023/a71cce9f-2815-4a32-8bf3-21834e5e7d97)

4. Row wise content extraction

   	![Row wise content extraction](https://github.com/theiturhs/handwritten-sentence-prediction/assets/96874023/aaff505f-6e94-422f-ae21-a632bacc2c64)


5. Image resizing

   ![Resized extracted characters image](https://github.com/theiturhs/handwritten-sentence-prediction/assets/96874023/a4711ab6-2384-47f9-bcc6-77aca913ae57)

6. Prediction

   ![Precition](https://github.com/theiturhs/handwritten-sentence-prediction/assets/96874023/acfe1e72-f060-4ae7-8650-6e04b4d5e0ed)

   **Predicted Sentence: ONE CAXM FOATY THOOIANO TNENTY SIX**
   
   **Actual Text: ONE LAKH FORTY THOUSAND TWENTY SIX**

   Note: The accuracy of prediction can be increased by increasing accuracy of trained model.


# Application - Cheque amount verification

Decoding amount from extracted text

![Decoded amount from predicted sentence](https://github.com/theiturhs/handwritten-sentence-prediction/assets/96874023/ecc43e46-e87a-4eb0-852e-edd3b9edd8c6)



# Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shrutikshrivastava/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:shrutishrivastava22ss@gmail.com)
[![Carrd](https://img.shields.io/badge/carrd-000000?style=for-the-badge&logo=carrd&logoColor=white)](https://theiturhs.carrd.co/)
[![Kaggle](https://img.shields.io/badge/kaggle-0077B5?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/theiturhs)
[![GitHub](https://img.shields.io/badge/github-000000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/theiturhs)
