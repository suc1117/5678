# 5678
## 간단 소개
 상명대학교 스마트정보통신공학과 임베디드시스템설계 '5678'조의 프로젝트입니다. <br>
 주제는 'YOLO기반의 도로 낙하물 보조감지 시스템' 입니다. <br>
 프로젝트의 목표는 주행중 도로상의 낙하물을 감지하여 신속하게 처리할 수 있도록 보조하는 시스템을 구현하는 것입니다. <br>
 또한 낙하물이 처리되기 전에 그 도로를 통과하는 차량들에게 경고해줄 수 있는 시스템을 구현합니다. <br>
 따라서 2차 피해를 방지하는 시스템을 구현하는것이 궁극적 목표입니다. <br>
 
## 프로젝트 저장소들
* [Serial-Communication](https://github.com/HyeokJinYun/Serial-Communication "Serial-Communication")
* [Android Application "WutchOut"](https://github.com/suc1117/WutchOut "WutchOut")
* [FTP C++](https://github.com/suc1117/FTP "FTP C++")
* [Raspberry Pi Map](https://github.com/kimjinhong2/maps "map")

## 시각화
  <img src="https://user-images.githubusercontent.com/48272857/70411781-7a731380-1a96-11ea-8de9-a4944178e6f8.png" width=550px>
  낙하물이 감지되었을 때, 위와 같이 라즈베리파이에서 GPS 정보를 COMPUTER로 시리얼 통신으로 전송하고 <br>
  촬영된 낙하물이미지에 시간정보와 위치정보를 포함시켜서 FTP 서버로 전송합니다. 그리하여 신속한 낙하물 처리를 돕습니다.
  <br>
  <img src="https://user-images.githubusercontent.com/48272857/70412298-d12d1d00-1a97-11ea-8ae5-c62f21bdd435.png" width=250px>
  보조감지 시스템을 사용하는 다른 사용자들은 어플을 구동하고 있을 시 (백그라운드 포함)<br> 낙하물의 일정 반경에 들어오게 되면 위험 경고를 받을 수 있습니다. <br>
  <br>
  <img src="https://user-images.githubusercontent.com/48272857/70411821-924a9780-1a96-11ea-99f2-8add16524ffe.png" width=600px>
  전체적인 동작 과정은 다음과 같습니다. <br>
  차량에 부착된 카메라를 통해 영상을 입력받습니다. 입력받는 영상은 YOLO를 통해 처리합니다. <br>
  그 과정에서 YOLO가 낙하물이라고 감지하게 되면 FTP 서버에 시간정보와 위치정보를 낙하물 이미지 파일에 포함시켜서 전송합니다. <br>
  그 뒤에 진행중인 차량들에게 2차 사고를 방지하기 위해 어플리케이션으로 경고를 받아서 회피하도록 돕습니다.<br>
  <br>
  <img src="https://user-images.githubusercontent.com/48272857/70411822-92e32e00-1a96-11ea-8407-a109873a0dbf.png" width=600px>
  낙하물 처리 차량은 FTP서버에 업로드되어있는 정보를 토대로 신속하게 업무를 진행하도록 돕습니다. <br>
  
## 사용된 기술들
Project is created with:
* Visual Studio 2017
* [CUDA 10.0](https://developer.nvidia.com/cuda-10.0-download-archive?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exenetwork "CUDA 10.0")
* [cuDNN](https://developer.nvidia.com/cudnn "cuDNN")
* [YOLO](https://github.com/AlexeyAB/darknet "YOLO") <br>
  tool: [YOLO_mark](https://github.com/AlexeyAB/Yolo_mark "YOLO mark")
  
  
