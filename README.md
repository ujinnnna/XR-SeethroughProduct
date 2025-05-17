# 🩻 XR SeeThrough Product

> **“보이지 않던 내부를 직접 보고, 만지고, 조립하는 새로운 방식의 혼합현실 체험”**

---

## 🎥 프로젝트 시연 영상

<p align="center">
  <a href="https://www.youtube.com/watch?v=hoCNiPeTAr0" target="_blank">
    <img src="https://img.youtube.com/vi/hoCNiPeTAr0/0.jpg" width="600" alt="SeeThrough XR Demo"/>
  </a>
</p>


---

## 🌐 프로젝트 개요

- **프로젝트 명**: SeeThrough XR  
- **개발 기간**: 2024.09.03 ~ 2024.11.25 (총 12주)  
- **개발 환경**: Unity URP / Meta XR SDK / Blender  
- **디바이스**: Meta Quest 3  
- **개발자**: 나우진 (1인 개발 프로젝트)

**SeeThrough XR**은 터빈 엔진과 인간 두개골의 내부 구조를 **직접 조작하며 탐험할 수 있는 XR 기반 혼합현실 애플리케이션**입니다.  
사용자는 **Passthrough 환경** 위에 실시간으로 생성되는 **시스루(See-Through) 오브젝트**를 통해 실제 공간과 가상 데이터를 자연스럽게 겹쳐보며, 평면적 정보 전달이 아닌 **몰입형 상호작용 기반 학습**을 경험합니다.

의료 시뮬레이션, 공학 학습, 제품 교육 등의 다양한 분야에 적용 가능한 인터랙션 구조를 기반으로 하며,  
혼자서 UI/UX, Shader, XR Interaction, 최적화까지 모두 직접 구현한 **기술 집약형 프로젝트**입니다.

---

## 🚀 핵심 기능 소개

### 🔍 내부 구조 투시 - SeeThrough Object
- **URP Stencil 기반** 구현
- 오브젝트를 잡아 회전시키며 내부를 자유롭게 탐색
- 현실 공간 위에서 **3D 모델의 레이어**를 가시화

### 🧠 인간 두개골 모듈 (Brain Scene)
- **Assemble 씬**: 해부학적 구조를 직접 배치하며 학습
- **Dismantle 씬**: 뇌와 두개골을 단계적으로 분리하며 이해

### ⚙️ 터빈 모듈 (Turbine Scene)
- **Assemble 씬**: 각 부품을 손으로 **집고 조립하며 기계 작동 원리**를 시각적으로 습득
- **Dismantle 씬**: **기계 내부의 동선과 연결 방식**을 분석

### 🧭 XR 인터랙션 시스템
- 손목에서 열리는 **XR Palm Menu**로 씬 전환
- **비동기 씬 로딩** 및 `AsyncOperation.progress`를 기반으로 로딩 완료 시 자동 전환
- 씬 로딩 중에는 **로딩 3D 오브젝트 출력**

### 🌙 사용자 몰입도 극대화 UI
- Coroutine 기반 **Fade In / Fade Out** 애니메이션
- 시작 Intro UI 구성 및 단계별 체험 안내
- **이벤트 기반 효과음** 삽입 (싱글톤 오디오 매니저)

---

## 🛠 기술 스택 및 구현 상세

| 구성 요소              | 세부 내용 |
|------------------------|----------|
| **Unity (URP)**         | 전체 콘텐츠 구현 및 최적화 |
| **Meta XR SDK**         | XR 인터랙션, 패스스루 환경 조성 |
| **XR Interaction Toolkit** | Grab, Select, Menu 기반 상호작용 |
| **URP Stencil**  | 오브젝트 내부 시각화 (SeeThrough) |
| **Coroutine**           | UI 전환, 씬 페이드 애니메이션 제어 |
| **Async Scene Loading** | 끊김 없는 씬 전환 및 단계별 로딩 제어 |
| **AudioManager (Singleton)** | 효과음 일괄 제어 |
| **Blender + FBX**       | **Tris, Verts 최적화** |
| **최적화 전략**         | Baked Light, Update 최소화 |

---

## 📊 최적화 전략

- Blender에서 **고폴리 모델 → 미디엄 폴리 전환** 후 FBX 재추출
- 실시간 렌더링에서 **Tris/Vets 수 분석 및 조정**
- **Update() 최소화**, FixedUpdate/Coroutine로 처리 분산
- 불필요한 DrawCall 및 Shadow Distance 줄이기

---


## 🧑‍💻 개발자 정보

- **이름**: 나우진  
- **이메일**: [uujin314@icloud.com](mailto:uujin314@icloud.com)
- **역할**: 기획 / 개발 / 디자인 / 최적화 / UI / Shader / XR 시스템 전반

---

## 💬 프로젝트 의의

> **SeeThrough XR**은 단순히 보이는 것을 넘어,  
> **보이지 않는 내부 구조를 XR 상호작용을 통해 ‘직접 탐색’하고, ‘재조립’할 수 있도록 설계된 차세대 학습형 혼합현실 콘텐츠입니다.**

기계공학 / 해부학 / 제품 설명 XR 콘텐츠로의 확장 가능성을 품고 있으며,  
본 프로젝트는 **XR 인터페이스의 몰입도와 정보 전달의 융합**을 실험한 **1인 개발 프로젝트**입니다.
