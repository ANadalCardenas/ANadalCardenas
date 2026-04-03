# Hi, I'm Aina Nadal 👋

Machine Learning & AI Engineer.

---

## Projects

### ⚙️ MLOps Churn Pipeline
**End-to-end MLOps pipeline for customer churn prediction**

Demonstrates production-grade ML practices: data versioning with DVC, remote experiment tracking on DagsHub, CI-driven model comparison on every PR, MLflow Model Registry lifecycle (Staging → Production), and Docker packaging.

Every pull request automatically trains a candidate model on new data (v2) and a baseline on the original data (v1), compares both, and posts a validation report with metric deltas and a BETTER / WORSE verdict as a PR comment.

```mermaid
flowchart LR
    A[v1 data] --> B[Train & register\nProduction]
    B --> C[Data drifts\nv2 arrives]
    C --> D[Open PR]
    D --> E[CI trains candidate\nv2 → Staging]
    D --> F[CI trains baseline\nv1 from main]
    E --> G[compare.py\nBETTER / WORSE]
    F --> G
    G --> H[PR comment\n+ Docker image]
    H --> I[Merge → Production]
```

<p align="center">
  <img width="400" src="https://raw.githubusercontent.com/ANadalCardenas/mlops-churn-pipeline/main/images/model_versions.png" alt="Model versions in DagsHub" />
  <img width="400" src="https://raw.githubusercontent.com/ANadalCardenas/mlops-churn-pipeline/main/images/artifacts.png" alt="MLflow artifacts" />
</p>

<p align="center">
  <img width="280" src="https://raw.githubusercontent.com/ANadalCardenas/mlops-churn-pipeline/main/images/confusion_matrix.png" alt="Confusion matrix" />
  <img width="280" src="https://raw.githubusercontent.com/ANadalCardenas/mlops-churn-pipeline/main/images/roc_curve.png" alt="ROC curve" />
  <img width="280" src="https://raw.githubusercontent.com/ANadalCardenas/mlops-churn-pipeline/main/images/precision_recall_curve.png" alt="Precision-recall curve" />
</p>

**Stack:** Python · scikit-learn · MLflow · DVC · GitHub Actions · Docker · Cloudflare R2 · DagsHub

🔗 [View repository](https://github.com/ANadalCardenas/mlops-churn-pipeline) · [MLflow UI](https://dagshub.com/ANadalCardenas/mlops-churn-pipeline.mlflow) · [Showcase PR](https://github.com/ANadalCardenas/mlops-churn-pipeline/pull/4)

---

### 🛡️ Drowsiness Detection
**Real-time driver drowsiness detection using YOLOv5**

Detects whether a person appears awake or drowsy from webcam or image input. Includes a full training pipeline: dataset collection, annotation, and model training.

[![Watch the demo](https://raw.githubusercontent.com/ANadalCardenas/drowsiness_detection/main/media/demo_preview.gif)](https://github.com/ANadalCardenas/drowsiness_detection)

**Stack:** YOLOv5 · PyTorch · OpenCV · Docker · Label Studio

🔗 [View repository](https://github.com/ANadalCardenas/drowsiness_detection)

---

### 👤 Close Person Detection
**Proximity detection combining object detection and depth estimation**

Detects nearby people in a video stream and highlights individuals closer than a defined distance threshold. Useful for robotics safety, autonomous driving, and security surveillance.

https://github.com/user-attachments/assets/041c215a-568f-42db-915d-bff2ee476140

**Stack:** YOLO · Depth-Anything-V2 · Docker

🔗 [View repository](https://github.com/ANadalCardenas/close_person_detection)

---

### 🎙️ English Conversational Teacher
**AI-powered voice-based English practice assistant**

An interactive web application that helps users practice English through voice conversation. Provides instant sentence corrections, grammar explanations, context-aware follow-up questions, and a final learning summary.

<p align="center">
  <img width="653" height="303" alt="Conversation view" src="https://github.com/user-attachments/assets/26a4e72c-e159-4a56-bf63-0edaea0081a2" />
</p>

<p align="center">
  <img width="648" height="680" alt="Sentence feedback" src="https://github.com/user-attachments/assets/170aa296-c1c6-4706-982a-9eef92d37a1e" />
</p>

<p align="center">
  <img width="633" height="738" alt="Session summary" src="https://github.com/user-attachments/assets/04462fc1-d9d6-486a-ba3b-bab39c74c2a2" />
</p>

**Stack:** FastAPI · OpenAI GPT · Whisper · Docker · Nginx

🔗 [View repository](https://github.com/ANadalCardenas/conversational_teacher_agent)
