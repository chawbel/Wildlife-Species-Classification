# Wildlife Species Classification for Conservation  
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)  
![PyTorch](https://img.shields.io/badge/PyTorch-1.12%2B-red)  

**Classifying African Wildlife Using Camera Trap Images and Deep Learning**  

![Project Banner](https://via.placeholder.com/800x200?text=Wildlife+Conservation+ML)  


---

## Project Overview  
This project uses a **ResNet50-based CNN** to classify species (e.g., Impala, Zebra) from camera trap images. The goal is to support biodiversity conservation efforts by automating wildlife monitoring. The model was trained on 1,500+ images from OpenMV and Raspberry Pi cameras and achieves **91% accuracy**.

---

## Dataset  
### Source  
- **Mendeley Camera Trap Dataset**:  
  [Dataset Link](https://data.mendeley.com/datasets/6mhrhn7rxc/1)  
  - Contains images from **OpenMV** and **Raspberry Pi** cameras.  
  - Labels include species, count, and geospatial coordinates.  

### Preprocessing  
1. **Data Cleaning**:  
   - Split multi-species entries into separate rows (e.g., `IMPALA, ZEBRA` → two entries).  
   - Removed corrupted/truncated images.  
2. **Folder Structure**:  
   Organized images into species-specific folders (e.g., `dataset/train/IMPALA/`).  
3. **Handling Nested Folders**:  
   Located Raspberry Pi images across 30 deployment subfolders (e.g., `1st-deployment`).  

---

## Tools and Libraries  
| Tool/Library       | Purpose                                  |
|--------------------|------------------------------------------|
| **PyTorch**        | Deep learning framework.                 |
| **ResNet50**       | Pretrained model for feature extraction. |
| **Pandas**         | Data cleaning and manipulation.          |
| **OpenCV**         | Image preprocessing.                     |
| **Matplotlib/Seaborn** | Confusion matrix and result plotting.  |

---

## Setup and Usage  
### 1. Clone the Repository  
```bash
git clone https://github.com/chawbel/Wildlife-Species-Classification.git
cd Wildlife-Species-Classification

### 2. Install Dependencies  
Install the required Python libraries using the following command:  
```bash
pip install -r requirements.txt


```markdown
### 3. Download Dataset  
Download the camera trap dataset from Mendeley Data:  
```bash
wget -O camera_trap_images.zip "https://prod-dcd-datasets-cache-zipfiles.s3.eu-west-1.amazonaws.com/6mhrhn7rxc-1.zip"
unzip camera_trap_images.zip -d camera_trap_images
