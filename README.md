# Paper-Record

### 읽은 논문을 정리하고, 읽을 논문을 기록해두는 Repo입니다. 📖

읽은 논문에 대한 자세한 내용은 [Issues](https://github.com/Songinpyo/Paper-Record/issues)에 별도로 정리합니다.

### 각 Issue 는 다음과 같이 정리되어 있습니다.
❓ Why → 해당 논문의 필요성, abstract

💡 Key insights → 해당 논문의 핵심 아이디어

🔗 Reference URL → 논문 링크

# Paper I read 🎓

### ○ 2D Human Pose Estimation
|제목|핵심 내용|
|------|---|
|[Deep High-Resolution Representation Learning for Human Pose Estimation](https://github.com/Songinpyo/Paper-Record/issues/2) [CVPR2019]|전체 Network에 걸쳐 High-Resolution을 유지하고 병렬적 fuse를 통해 다른 Resolution 사이 정보 교환이 이루어진다.|
|Deep High-Resolution Representation Learning for Visual Recognition [CVPR2020]|2019 HRNet과 아이디어는 같지만, High-Resolution으로부터만 representaiton을 구하던 HRNetV1과 달리 4개의 Resolution 모두에 집중하는 HRNetV2, HRNetV2p 은 각각 Semantic segmentation, Object detection에 사용된다.|
|Multi-Instance Pose Networks: Rethinking Top-Down Pose Estimation [ICCV2021]|기존의 Top-down method architecture에 Multi Instance Modulation Block을 적용하여 Bounding box내의 multi instance 인식을 가능하게 한다. 파라미터 증가 3% 수준으로 매우 효율적|
|[Rethinking the Heatmap Regression for Bottom-up Human Pose Estimation](https://github.com/Songinpyo/Paper-Record/issues/1) [CVPR2021]|Bottom-up method에서 Human scale variance와 labeling ambiguities를 고려하지 않는 fixed Standard deviations를 쓰는 것은 문제가 있다. 이를 위해 Scale-adaptive heatmap regression과 Weight-adaptive heatmap regression을 제안한다.|
|[Deep Dual Consecutive Network for Human Pose Estimation](https://github.com/Songinpyo/Paper-Record/issues/3) [CVPR2021]|연속적인 이미지 즉, Video에서 Human Pose Estimation은 motion blur, video defocus, occlusions 등 다양한 어려움을 겪는다. 해당 논문은 Key Point detection을 위해 과거와 미래의 비디오 프레임의 temporal cues를 활용하는 multi-frame HPE를 제안한다.|
|[OTPose: Occlusion-Aware Transformer for Pose Estimation in Sparsely-Labeled Videos](https://github.com/Songinpyo/Paper-Record/issues/16)[2022]|제한적인 receptive field를 가지는 CNN의 근본적 한계와 main challenge인 occlusion을 해결하기 위해 여러 프레임의 조합과 transformer를 이용해서 Occlusion aware heatmap, Occlusion Attension mask를 생성한다. Posetrack SOTA |

### ○ 3D Human Mesh Reconstruction
|제목|핵심 내용|
|------|---|
|[Keep it SMPL: Automatic Estimation of 3D Human Pose and Shape from a Single Image](https://github.com/Songinpyo/Paper-Record/issues/10) [ECCV2016]|2D monocular image로부터 3D mesh를 추정하는 방법을 제안한 논문, 현재까지도 smpl parameter를 추정하는 방법 사용하는 논문들에 꾸준히 사용되고 있다.|
|[The Power of Points for Modeling Humans in Clothing](https://github.com/Songinpyo/Paper-Record/issues/11) [ICCV2021]|기존의 mesh기반, implicit surface 기반 3D reconstruction에서 pose base cloth deformation같은 Detail한 부분을 잘 나타내지 못한 것을 point cloud 기반 방법으로 realistically 구현하였다.|
|[3D Clothed Human Reconstruction in the Wild](https://github.com/Songinpyo/Paper-Record/issues/12) [ECCV2022]|기존의 data로 사용되던 데이터는 제약조건하에 촬영된 3D rendered images를 사용하였기 때문에 in-the-wild images를 데이터로 사용하는 것과 큰 domain gap이 존재한다. 이처럼 3D 대신 2D를 target으로 하는 weakly supervising에서 발생하는 depth ambiguity 문제 해결을 위해서 DensePose based loss를 도입한다. 해당 model은 SMPL과 SMPLicit을 기반으로 clothed human mesh를 복원한다.|
|[HMR : End-to-end Recovery of Human Shape and Pose](https://github.com/Songinpyo/Paper-Record/issues/17) [CVPR 2018]|3D annotation이 없는 In-the-wild image를 direct 방식으로 3D mesh reconstruction에서 사용할 수 있게 하였다. GAN의 adversarial training method를 차용하여 discriminator를 통해 사실적인 reconstruction이 가능하게 하였다.|
|[SPIN : Learning to Reconstruct 3D Human Pose and Shape via Model-fitting in the Loop](https://github.com/Songinpyo/Paper-Record/issues/18) [ICCV 2019]|Optimization과 Regression을 상호보완적으로 사용하여 Regression은 Optimization에게 좋은 initialization을 제공하고, 그렇게 얻어진 Optimization은 Regression의 좋은 Supervision이 될 수 있다. 스스로 Supervision을 생성하기 때문에 별도의 3D annoation없이 2D annotation만 있는 In-the-wild image에서도 사용가능하다.|
|[VIBE: Video Inference for Human Body Pose and Shape Estimation](https://github.com/Songinpyo/Paper-Record/issues/19) [CVPR 2020]|비디오에서 temporal information을 이용해 정확하게 3D Motion 을 예측하는 것을 목적으로 한 논문으로서 RNN architecture의 사용으로 information을 over time propagate 하였다. AMASS dataset을 이용하여 motion sequence를 학습시킨 discriminator를 제안한다. Discriminator에 self-attention을 적용하여 human motion에 중요한 temporal structure에 집중하도록 한다.|

### ○ Vision
|제목|핵심 내용|
|------|---|
|[Deep Residual Learning for Image Recognition](https://github.com/Songinpyo/Paper-Record/issues/4) [IEEE2016]|Residual learning을 통해 deeper network를 쉽게 최적화 시키고, deeper layer가 유발하는 문제를 해결한다. Residual block, Bottleneck block|
|[Feature Pyramid Networks for Object Detection](https://github.com/Songinpyo/Paper-Record/issues/5) [CVPR2017]|Deep Convolution Network에 Feature pyraimd 구조를 사용한다. Low resolution High feature를 up-conv하여 하위 layer의 feature들과 더하는 방법으로 feature를 추출해낸다.|
|[Learning Transferable Visual Models From Natural Language Supervision](https://github.com/Songinpyo/Paper-Record/issues/13) [OpenAI2021]|Text와 Image를 동시에 학습시키는 방식을 통해서 Classification task에서 좋은 성능을 보여주었다. Training에는 대량의 raw data Inference는 Zero-shot으로 진행되는 특징이 있다.|

### ○ Temporal
|제목|핵심 내용|
|------|---|
|[TF-Blender: Temporal Feature Blender for Video Object Detection](https://github.com/Songinpyo/Paper-Record/issues/9) [ICCV2021]|Multi frame 사용시 모든 프레임이 상호간 영향을 주고 받음으로써 feature dgrading 문제를 해결하였다. 현재 프레임과 주변 프레임간의 관계를 이용한 adaptive weight, 현재 프레임을 제외한 주변 프레임간의 관계를 이용한 featrue adjustment의 사용으로 어느 모델에나 적용가능한 irrelevent한 feature를 생성한다.|
|[FlowNet: Learning Optical Flow with Convolutional Networks](https://github.com/Songinpyo/Paper-Record/issues/8) [IEEE2015]|Optical flow에 대한 간략한 설명과, Optical flow를 구하는데 CNN을 사용한 모델을 제시한다.|

### ○ Transformer
|제목|핵심 내용|
|------|---|
|[AN IMAGE IS WORTH 16X16 WORDS:TRANSFORMERS FOR IMAGE RECOGNITION AT SCALE](https://github.com/Songinpyo/Paper-Record/issues/6) [ICLR2021]|CNN을 전혀 사용하지 않고 Transformer만을 이용한 Image classifier를 만든다. 이미지를 패치로 나누고 linear projection으로 패치의 차원을 변환하여 패치 임베딩을 구축한다. 패치 임베딩과 위치 임베딩을 Transformer Encoder에 넣어 feature representation을 추출하고 이를 MLP head에 넣어 최종적으로 class를 분류한다.|
|[Swin Transformer: Hierarchical Vision Transformer using Shifted Windows](https://github.com/Songinpyo/Paper-Record/issues/14) [ICCV2021]|Local Window를 적용하여 inductive bias 증가, Patch Merging을 통해 Hierarchical 구조 형성 보다 작은 물체도 인지 가능, 이미지의 특성을 고려한 Transformer 구조|
|[Vision Transformer with Deformable Attention](https://github.com/Songinpyo/Paper-Record/issues/15) [CVPR2022]|Deformable Attention Module을 이용하여 특정 query에 대해 attention을 집중시킬 수 있으며, Swin에서 사용된 W-MSA, SW-MSA 를 이용하여 연산량을 줄였다. Object detection, Segmentation에 보다 적합한 Backbone으로 사용될 수 있다.|

# Paper I'll read ✏️

### ○ Human Pose Estimation
|제목|기한|
|------|---|

### ○ Vision
|제목|기한|
|------|---|
|Solving ImageNet: a Unified Scheme for Training any Backbone to Top Results [Alibaba]|22.06.25|
|DeiT: Training Data-Efficient Image Transformer & Distillation through Attention|22.06.30|
