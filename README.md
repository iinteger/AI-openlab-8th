한국인공지능연구소에서 진행하는 AI 오픈랩의 8기 활동을 기록한 레포지토리입니다.





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

* 21. 03.03
      * 중간발표내용 : 지금까지 했던 논문리뷰 내용 정리 + 발표날 전까지 계획한 사항 + 앞으로 진행할 사항
        1. PPT 작성 및 발표 : 이재욱
        2. YOLO 모델 프로토타입 테스트 : 이유진
        3. 이미지 전처리 : 전창삼
        4. 데이터셋 자료 및 훈련 가능한 YOLO 관련 API 조사 : 이정수
      * 목표 : 마스크 착용 유//무 감지

