한국인공지능연구소에서 진행하는 AI 오픈랩의 8기 활동을 기록한 레포지토리입니다.

주간기록 : [https://www.ai-lab.kr/opens/600fff86f578eb231e8c3922](https://www.ai-lab.kr/opens/600fff86f578eb231e8c3922)




# 1주차

* 팀빌딩 및 주제선정
  * real-time object detection 논문 리뷰 및 실시간으로 마스크 착용 여부를 탐지하는 모델 구축
  * 2주차 ~ 6주차 : rcnn, yolo 논문 리뷰
  * 7주차 ~ 12주차 : 데이터 수집, 모델 선정 및 구축



# 2주차

* 선정논문 발표

  * [RCNN (Rich feature hierarchies for accurate object detection and semantic segmentation Tech report (v5))](https://arxiv.org/pdf/1311.2524v5.pdf)

  * 발표자 : 이재욱

  * [Fast R-CNN](https://arxiv.org/pdf/1504.08083.pdf) [정리본](./week2/Fast R-CNN.md)

    * 발표자 : 이정수

    

* 피드백 사항 : 논문 리뷰 중 어려운 내용이 나오면 다같이 공유하기



# 3주차

* 선정논문 발표

  * [Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks](https://arxiv.org/pdf/1506.01497.pdf)

    * 발표자 : 이유진

  * [You Only Look Once: Unified, Real-Time Object Detection](https://arxiv.org/pdf/1506.02640.pdf)

    * 발표자 : 이재욱

    

* 기존의 RCNN 흐름에서 accuracy와 inference latency의 trade-off로 실용성을 꾀한 모델이 Yolo

* 최신 모델까지 편리하게 API가 제공되는 yolo 모델을 이후 프로젝트에 사용하는 것으로 잠정 결정

* 마스크 Dataset

  * https://public.roboflow.com/object-detection/mask-wearing/4

  * https://www.kaggle.com/andrewmvd/face-mask-detection

    

# 4주차

* 추석 연휴

  

# 5주차

* 선정논문 발표
  * [YOLO9000: Better, Faster, Stronger](https://arxiv.org/pdf/1612.08242.pdf)
    * 발표자 : 이정수



# 6주차

* 선정논문 발표

  * [Single-Shot Refinement Neural Network for Object Detection](https://arxiv.org/pdf/1711.06897.pdf)

    * 발표자 : 이유진

      

* 차주 중간발표 예정으로 논문 리뷰를 마치고 개발 명세 작성 및 계획

* 03.03

  * 중간발표내용 : 지금까지 했던 논문리뷰 내용 정리 + 발표날 전까지 계획한 사항 + 앞으로 진행할 사항
    1. PPT 작성 및 발표 : 이재욱
    2. YOLO 모델 프로토타입 테스트 : 이유진
    3. 이미지 전처리 : 전창삼
    4. 데이터셋 자료 및 훈련 가능한 YOLO 관련 API 조사 : 이정수
  * 목표 : 마스크 착용 유/무 감지



# 7주차

* 중간발표

  * 수집했던 데이터셋을 yolo v5에 적용하여 실행한 결과, 마스크를 쓴 사람은 마스크를 쓴 것으로 잘 판단하지만, 마스크를 쓰지 않은 사람도 마스크를 썼다고 판단하는 결과가 다수 검출.

    -> Class imbalance로 인한 오차로 예상되어 마스크를 쓰지 않은 데이터셋을 더 확보하는 방향으로 결정

  * 마스크 착용 유무만 판단하는 모델은 충분히 가능할것으로 판단하고 추가적으로 입만 가리는 코스크, 턱에 걸치는 턱스크 등의 클래스도 판단하는 모델 구축, 모델 경량화 등 개선 방안 확립

  

# 8주차

* 개인 일정으로 불참
* 수집한 데이터들을 현재 사용하는 yolo data format으로 변환하는 작업 필요



# 9주차

* 부족했던 마스크 미착용 데이터 보충
* 현재 Task가 단순하다 판단하여 코스크, 턱스크 등 불완전하게 마스크를 착용하는 경우에 대한 classification 고려



# 10주차

* 코스크, 턱스크 등 incorrect data를 확보 및 labeling 작업중
* Yolo v5를 사용하는것으로 결정, 차후 모델 테스트 결과에 따라 tiny yolo 등 경량화 모델 사용 고려
* data class가 imbalance하기 때문에 이를 적절히 augmentation하거나 split할 방법 고려



# 11주차

* incorrect data에 대한 학습 결과 수치상 overfitting의 가능성이 있음
