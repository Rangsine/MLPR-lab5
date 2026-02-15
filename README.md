# Machine Learning and Pattern Recognition Lab 5
### Name: Vageesh Chandra Srivastava  


---

## Aim

The objective of this lab is to:

- Detect faces in an image using Haar Cascade classifier.
- Extract color-based features (Hue and Saturation).
- Perform clustering using K-Means algorithm.
- Classify a template face image based on learned clusters.
- Visualize clusters and analyze results.

---

## Methodology

### Face Detection

- Loaded the image `plaksha_Faculty.jpg`
- Converted image to grayscale.
- Used Haar Cascade (`haarcascade_frontalface_default.xml`) to detect faces.
- Drew bounding boxes around detected faces.
<img width="1283" height="854" alt="image" src="https://github.com/user-attachments/assets/2e31e5fa-5779-45aa-b500-25a7b19acbec" />


---

### Feature Extraction (HSV Color Space)

- Converted the original image to HSV color space.
- For each detected face:
  - Extracted the face region.
  - Computed:
    - Mean Hue value
    - Mean Saturation value
- Stored extracted features as a 2D feature vector
---

### K-Means Clustering

- Applied K-Means clustering with:
  - `n_clusters = 2`
  - `random_state = 0`
- Clustered faces based on Hue and Saturation values.
- Obtained:
  - Cluster centroids
  - Cluster labels
<img width="1005" height="545" alt="image" src="https://github.com/user-attachments/assets/17f3fa18-4ac6-4bb5-bf3f-61b1cb483b37" />


---

### Cluster Visualization

- Plotted Hue vs Saturation values using scatter plot.
- Used different colors for:
  - Cluster 0
  - Cluster 1
- Visualized cluster separation in feature space.
<img width="1005" height="545" alt="image" src="https://github.com/user-attachments/assets/6b087d97-3244-4ca4-a81e-3d1e11647dcb" />


---

### Template Image Classification

- Loaded template image `Dr_Shashi_Tharoor.jpg`.
- Detected face in template image.
- Extracted HSV features (Mean Hue, Mean Saturation).
- Used trained K-Means model to predict cluster label:
- Visualized template classification in feature space.
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/7bedef31-a870-418b-830a-07c8df874bf0" />
<img width="1005" height="545" alt="image" src="https://github.com/user-attachments/assets/6ec850e5-5899-472e-a9fa-55acb4433398" />
<img width="1005" height="545" alt="image" src="https://github.com/user-attachments/assets/5cc9b225-8aa2-4ba8-90cd-20eadd5de528" />




---

## Results

- Faces were successfully detected using Haar Cascade.
- Hue and Saturation features effectively separated faces into two clusters.
- K-Means grouped faces based on color similarity.
- Template image was correctly assigned to one of the clusters.
- Scatter plots clearly showed cluster separation.

---

##  Key Observations

- HSV color space is effective for color-based clustering.
- K-Means works well for grouping similar faces using simple features.
- Feature selection plays a crucial role in clustering quality.
- Visualization helps in understanding cluster separation.

---

## Conclusion

In this lab, face detection and clustering were successfully implemented.  
By extracting Hue and Saturation features from detected faces and applying K-Means clustering, faces were grouped based on color similarity.  

The template image was classified using the trained clustering model, demonstrating practical use of unsupervised learning for image-based grouping and classification.


