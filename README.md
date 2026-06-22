# 랜딩기어 및 신뢰도 테스트 장비 (PLC Landing Gear Test Equipment)
> PLC와 공압 시스템으로 항공기 랜딩기어의 상승·하강을 자동 제어하고, 반복 사이클 신뢰도 테스트로 구동 내구성과 동작 안정성을 검증한 장비.

![PLC](https://img.shields.io/badge/PLC-Ladder%20Logic-0078D4?style=flat-square&logo=siemens&logoColor=white)
![Fusion 360](https://img.shields.io/badge/Fusion%20360-FF6C00?style=flat-square&logo=autodesk&logoColor=white)
![Pneumatics](https://img.shields.io/badge/Pneumatics-System-00A8E8?style=flat-square)
![Laser Cutting](https://img.shields.io/badge/Laser%20Cutting-Fabrication-E74C3C?style=flat-square)
![Automation](https://img.shields.io/badge/Automation-Control-2ECC71?style=flat-square)
![Reliability Test](https://img.shields.io/badge/Reliability-Test-9B59B6?style=flat-square)

## 📌 프로젝트 정보
| 항목 | 내용 |
|------|------|
| 개발 기간 | 2021.11 ~ 2021.12 (약 1개월) |
| 팀 구성 | 2인 팀 프로젝트 |
| 담당 역할 | 전체 설계 및 구현 |
| 시연 영상 | 준비 중 |

## 🎯 프로젝트 개요
항공기 랜딩기어의 상승·하강 동작을 PLC 시퀀스 제어와 공압 시스템으로 자동화한 테스트 장비입니다. 실제 랜딩기어 구조의 동작 메커니즘을 축소 모델로 구현하고, 리밋 스위치 기반의 위치 감지를 통해 동작 완료 조건을 판단하도록 설계했습니다. 단순 구동에 그치지 않고 수백 회 이상의 반복 사이클을 자동 수행하는 신뢰도 테스트를 통해 구동부의 내구성과 동작 안정성을 정량적으로 검증했습니다.

## ✨ 주요 기능 / 담당 업무
- **PLC 시퀀스 제어 프로그래밍**: 랜딩기어 상승·하강 자동 시퀀스를 래더 다이어그램(Ladder Logic)으로 구현하고, 리밋 스위치 신호로 동작 완료 조건을 분기 처리했습니다.
- **공압 회로 설계**: 공압 실린더와 솔레노이드 밸브 구동 회로를 설계하고 PLC 출력 신호와 연동해 정밀 제어를 구현했습니다.
- **3D CAD 모델링 및 부품 제작**: 랜딩기어 링크 구조물을 Fusion 360으로 3D 설계·도면화하고, 레이저 커터로 실제 부품을 가공·조립했습니다.
- **신뢰도 테스트**: 수백 회 이상의 반복 동작 사이클 테스트로 내구성과 안정성을 검증하고, 이상 동작 조건을 분석·개선했습니다.

## 🛠 기술 스택
### Software
- PLC 래더 다이어그램(Ladder Logic)
- 3D CAD (Fusion 360)

### Hardware
- PLC 컨트롤러
- 공압 실린더 / 솔레노이드 밸브
- 리밋 스위치
- 레이저 커터 가공 부품

## 🔀 시스템 아키텍처
```mermaid
flowchart LR
  A["리밋 스위치 입력"] --> B["PLC 시퀀스 판단"]
  B --> C["솔레노이드 밸브 제어"]
  C --> D["공압 실린더 구동"]
  D --> E["랜딩기어 상승/하강"]
  E --> F["완료 조건 감지"]
  F --> G["사이클 카운트"]
  G --> H{"반복 조건 만족?"}
  H -->|"아니오"| B
  H -->|"예"| I["테스트 종료/결과 분석"]
```
리밋 스위치 입력을 받아 PLC가 시퀀스를 판단하고 솔레노이드 밸브와 공압 실린더를 제어해 랜딩기어를 구동하며, 완료 조건 감지 후 사이클 카운트를 증가시켜 반복 신뢰도 테스트를 수행하는 흐름입니다.

## 📸 스크린샷
> `images/` 폴더에 이미지를 추가한 뒤 아래 경로를 맞춰주세요.

| 화면 | 설명 |
|------|------|
| ![화면1](images/01.png) | 랜딩기어 테스트 장비 전체 구성 |
| ![화면2](images/02.png) | PLC 래더 다이어그램 및 공압 회로 |

## 🎬 시연 영상
[![시연 영상](images/thumbnail.png)](여기에-유튜브-링크)
