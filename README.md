# Paper-Record

### 읽은 논문을 정리하고, 읽을 논문을 기록해두는 Repo입니다. 📖

읽은 논문에 대한 자세한 내용은 [Issues](https://github.com/Songinpyo/Paper-Record/issues)에 별도로 정리합니다.

### 각 Issue 는 다음과 같이 정리되어 있습니다.
❓ Why → 해당 논문의 필요성, abstract

💡 Key insights → 해당 논문의 핵심 아이디어

🔗 Reference URL → 논문 링크

# Paper I read 🎓

### ○ Human Pose Estimation
|제목|핵심 내용|
|------|---|
|[Deep High-Resolution Representation Learning for Human Pose Estimation](https://github.com/Songinpyo/Paper-Record/issues/2) [CVPR2019]|전체 Network에 걸쳐 High-Resolution을 유지하고 병렬적 fuse를 통해 다른 Resolution 사이 정보 교환이 이루어진다.|
|Deep High-Resolution Representation Learning for Visual Recognition [CVPR2020]|2019 HRNet과 아이디어는 같지만, High-Resolution으로부터만 representaiton을 구하던 HRNetV1과 달리 4개의 Resolution 모두에 집중하는 HRNetV2, HRNetV2p 은 각각 Semantic segmentation, Object detection에 사용된다.|
|Multi-Instance Pose Networks: Rethinking Top-Down Pose Estimation [ICCV2021]|기존의 Top-down method architecture에 Multi Instance Modulation Block을 적용하여 Bounding box내의 multi instance 인식을 가능하게 한다. 파라미터 증가 3% 수준으로 매우 효율적|
|[Rethinking the Heatmap Regression for Bottom-up Human Pose Estimation](https://github.com/Songinpyo/Paper-Record/issues/1) [CVPR2021]|Bottom-up method에서 Human scale variance와 labeling ambiguities를 고려하지 않는 fixed Standard deviations를 쓰는 것은 문제가 있다. 이를 위해 Scale-adaptive heatmap regression과 Weight-adaptive heatmap regression을 제안한다.|
|[Deep Dual Consecutive Network for Human Pose Estimation](https://github.com/Songinpyo/Paper-Record/issues/3) [CVPR2021]|연속적인 이미지 즉, Video에서 Human Pose Estimation은 motion blur, video defocus, occlusions 등 다양한 어려움을 겪는다. 해당 논문은 Key Point detection을 위해 과거와 미래의 비디오 프레임의 temporal cues를 활용하는 multi-frame HPE를 제안한다.|

### ○ Vision
|제목|핵심 내용|
|------|---|
|[Deep Residual Learning for Image Recognition](https://github.com/Songinpyo/Paper-Record/issues/2)|Residual learning을 통해 deeper network를 쉽게 최적화 시키고, deeper layer가 유발하는 문제를 해결한다. Residual block, Bottleneck block|

# Paper I'll read ✏️

### ○ Human Pose Estimation
|제목|기한|
|------|---|

### ○ Vision
|제목|기한|
|------|---|
|Solving ImageNet: a Unified Scheme for Training any Backbone to Top Results [Alibaba]|22.06.25|
|DeiT: Training Data-Efficient Image Transformer & Distillation through Attention|22.06.30|
||2022.07.03|
