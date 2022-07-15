# 유니티 버전 업그레이드
### 1. Graphics API 우선순위를 변경했을 경우에 대한 안정성
---
## 현재 개발 플레이어 세팅

### Unity Version : 2019.4.36f1

### Android 
#### Graphics API : **Auto Graphics API (Disable => Priority : OpenGL ES 2.0(1st), OpenGL ES 3.0(2nd), Vulkan(Disable))**
#### Minimum API Level : **Android 5.0 (API 21)**
#### Target API Level : **Android 11.0 (API 30)**
---
### iOS
#### Graphics API : Auto Graphics API (Enable => Metal)
#### Target Device : iPhone + iPad
#### Target SDK : Device SDK
#### Target Minimum iOS Version : 11.0
---
### Unity의 Graphics API의 우선순위의 따른 결과
![image](https://user-images.githubusercontent.com/57660360/179161419-0a75703f-5ef8-4eaa-a65a-3be4a001788a.png)

---
![image](https://user-images.githubusercontent.com/57660360/179161072-b4b64f9e-43c1-491b-8d7a-b1fc4096cc83.png)
#### 현재 개발 세팅의 우선순위는 위와 같이 Android는 2.0, 3.0 순서이다.
#### 맨 위의 API(OpenGLES 2.0)를 실행하여 가능한 기기라면 해당 API(OpenGLES 2.0)를 실행하고,
#### 불가능한 기기라면 두 번째의 API(OpenGLES 3.0)를 실행하여 가능 여부를 판별하는 식
#### 즉, 현재 문제는 2.0과 3.0을 모두 실행가능 한 기기에서는 3.0을 사용하는 것이 좋지만 2.0의 우선순위가 높기 때문에 2.0을 사용하고 있다.
#### 또한, Auto Graphics API를 활성화 하면 API 리스트를 자동으로 선별하여 해당 기기에 맞는 API를 지정해준다.
#### 특별한 이유가 있는 것이 아니라면 해당 기능을 활성화 하는 것을 추천
---

### 2. 유니티 LTS 버전에 따른 Android, iOS 모바일 기기 권장사양
---
|Unity Version| Android | iOS |
|---|---|---|
|[2019.4](https://docs.unity3d.com/kr/2019.4/Manual/system-requirements.html)|**Android 4.4 (API 19)+ **, ARMv7(32bit), ARM64, **OpenGL ES 2.0 +, 3.0 +, Vulkan**, 하드웨어가 Android OS를 네이티브로 실행해야함 컨테이너 또는 에뮬레이터 내 Android는 지원xAndroid SDK(9/ API 28), Android NDK(r19)|**iOS 10+, A6/A6X SoC+, Metal, OpenGL ES 2.0, 3.0(지원 중단)**, macOS 10.12.6 및 Xcode 9.4 이상의 Mac 컴퓨터가 필요함|
|[2020.3](https://docs.unity3d.com/kr/2020.3/Manual/system-requirements.html)|**Android 4.4 (API 19)+ **, ARMv7, ARM64, **OpenGL ES 2.0 +, 3.0 +, Vulkan**, 하드웨어가 Android OS를 네이티브로 실행해야함 컨테이너 또는 에뮬레이터 내 Android는 지원x **개발용 Android SDK(10/API 29)**, Android NDK(r19)|**iOS 11+, A7 SoC Metal**, macOS 10.12.6 및 Xcode 9.4 이상의 Mac 컴퓨터가 필요함|
|[2021.3](https://docs.unity3d.com/kr/2021.3/Manual/system-requirements.html)|<span style="color:red">** Android 5.1 (API 22)+ **</span> , ARMv7(32bit), ARM64, <span style="color:red">**OpenGL ES 3.0 +, Vulkan**</span>, 하드웨어가 Android OS를 네이티브로 실행해야함, **Chrome OS 용 Android 외**에 컨테이너 또는 에뮬레이터 내 Android는 지원x, <span style="color:red">**Android SDK(10/ API 29), Android NDK(r21d)**</span>|**iOS 12+, A7 SoC+**, Metal|

#### 현재 프로젝트의 세팅과 관련하여 Unity 2021.3 LTS 버전은 OpenGLES 2.0을 지원 하지 않으며, Android API, SDK 및 NDK의 버전 업과 iOS 12+ 타겟이므로 적합하지 않음
#### 그에 반해 Unity 2020.3 LTS 버전은 설정된 조건들을 모두 수용할 수 있으므로 2020.3 LTS 버전으로 업그레이드 하는 것이 더 안정적

#### [Android API 9(Pie) 지원 기기](https://namu.wiki/w/%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C%20%ED%8C%8C%EC%9D%B4#s-4.1.1) VS [Android API 10 지원 기기](https://namu.wiki/w/%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C%2010)
#### [iOS 10+ 지원 기기](https://support.apple.com/ko-kr/HT209547) VS [iOS 11+ 지원 기기](https://support.apple.com/ko-kr/HT209574)

