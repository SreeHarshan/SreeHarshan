# Hi, I'm Sree Harshan 👋

**AI + Backend Engineer** · Associate Software Engineer @ AvenirVista Tech Solutions, Coimbatore
B.Tech in Artificial Intelligence & Machine Learning, Kongu Engineering College (2021–2025)

I build high-throughput backend systems and ML-powered features end to end, from model training and edge deployment to Kubernetes-based serving infrastructure.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-sree--harshan--a--s-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sree-harshan-a-s)
[![Email](https://img.shields.io/badge/Email-sreeharshan12%40gmail.com-D14836?logo=gmail&logoColor=white)](mailto:sreeharshan12@gmail.com)
[![LeetCode](https://img.shields.io/badge/LeetCode-500%2B%20solved-FFA116?logo=leetcode&logoColor=white)](https://leetcode.com/_sree_harshan_)

---

## 🔭 What I'm working on

### Real-Time VLM Streaming Platform (at AvenirVista)
A system I own end to end: a platform that streams live device sessions to a Vision-Language Model service.

- **Isolated sessions:** every device session runs in its own Kubernetes pod, so one crashed session never takes others down.
- **User-to-pod routing:** an nginx OpenResty Lua shared dict maps each user to their pod, keeping routing state on the hot path.
- **Two-path pod lifecycle:** on disconnect the routing entry is cleared and the pod deleted immediately; on crash the pod is left running with logs preserved for postmortems.
- **Control plane (FastAPI):** connect/disconnect lifecycle and force-stop, both client-driven and admin-initiated (delivered as a dedicated WebSocket response).
- **Data plane:** session recordings serialized as Protocol Buffers and streamed into self-hosted MinIO (S3-compatible, chosen to avoid egress costs and vendor lock-in), so an external dashboard can replay history. Live session messages go out over MQTT for admin live tracking.
- **Ops:** structured logging, Kubernetes health probes, and automated pod restarts for self-healing.
- **Performance:** profiled and optimized the mobile→server frame pipeline, cutting latency from ~200 ms to ~100 ms (**2x**).

> Status: designed for concurrent multi-session load and in pre-full-deployment validation.

---

## 🚀 Projects

| Project | What it does | Highlights |
|---|---|---|
| **ADAS Object Detection & Tracking** | Fine-tuned HybridNets (PyTorch) for detection and tracking | Trained on BDD100K (100K images) + a custom 100K-frame dataset; **27% fewer identity mismatches** via track-deletion redesign, multi-factor association and Kalman-filter ego-motion compensation; track-merging to recover fragmented tracks; YOLO-based per-object orientation branch |
| **Vehicle Scenario Prediction** | Encoder-decoder Transformer that classifies live driving scenarios and predicts time-to-collision / time-to-intersection | **91.6% held-out accuracy**; built for a global automotive client; modular design for swapping datasets |
| **ANPR on NVIDIA Jetson Orin Nano** | License plate recognition with YOLO + PaddleOCR | **92% detection / 96% OCR**; TensorRT on-device inference with no cloud round-trips; 🏆 *Best Project Award 2025* |
| **Mechanical Fault Diagnosis** | Vibration signals → MFCC spectrograms → CNN classification | Benchmarked Standard CNN, MobileNetV2 and VGGNet; **98% on the HUST bearing dataset** |
| **BERT Fake-Review Classifier** | Detects AI-generated reviews on the Kaggle Amazon fake-reviews dataset | Fine-tuned BERT; self-hosted on my homelab |
| **Fake Circular Detector** | Flags fake circulars | 🏆 *First prize, SDC Fest* |

---

## 🛠️ Tech stack

**Languages:** Python · JavaScript · Java · Bash

**Backend:** FastAPI · Node.js · Express · REST · WebSockets · MQTT · Protobuf · Microservices · Distributed Systems

**Cloud & DevOps:** Docker · Kubernetes · AWS (EC2, S3, VPC) · Terraform · CI/CD · Nginx / OpenResty · GitLab · MinIO · Linux

**AI / ML:** PyTorch · TensorFlow · Keras · Hugging Face Transformers · OpenCV · YOLOv8 · TensorRT · PaddleOCR · CNNs · LLMs / VLMs · Computer Vision · NLP · Multi-Object Tracking · Kalman Filters

**Mobile:** Flutter

---

## 💼 Experience

- **Associate Software Engineer, AvenirVista Tech Solutions** (Aug 2025 – present): real-time VLM platform, ML-powered backend features, and a self-hosted GitLab instance now used org-wide.
- **Intern, Green Collar Agritech Solutions** (Nov 2023 – May 2024): Flutter app that downloads ~10 MB of encrypted ML weights and runs them on-device for in-field crop scanning, with token-based persistent auth.
- **Intern, Centillion Labs** (Sep 2023 – Nov 2023): automated AWS provisioning (EC2, S3, VPC) with Terraform, cutting environment setup from ~1 hour to under 10 minutes.

---

## 🏠 Homelab

I self-host a Jellyfin media server and my personal projects at home. With no public IP from my ISP, I use dynamic DNS plus Tailscale to reach it. When something breaks at 1 am, I'm both the on-call engineer and the user.

---

## 📄 Publication

**"Machine Learning-driven Precise Automobile Insurance Claim Prediction"**, SoCPaR 2023 (15th International Conference on Soft Computing and Pattern Recognition)

---

## 📫 Let's connect

I'm interested in AI + backend roles and open to relocating to Bangalore.
Reach me on [LinkedIn](https://www.linkedin.com/in/sree-harshan-a-s) or at **sreeharshan12@gmail.com**.
