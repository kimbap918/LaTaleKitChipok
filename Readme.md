<h1 align="center">LaTale Data Toolkit</h1>

<p align="center">
  <img src="https://i.imgur.com/44WtkiW.png" alt="LaTale Character" width="300"/>
</p>


<br>

## 개요


**LaTale Data Toolkit**은 온라인 게임 *LaTale*의 클라이언트 내부 리소스를 추출하기 위한 도구입니다.  
이 도구는 게임 리소스 파일인 `.SPF`, `.TBL`, `.LDT` 파일을 처리합니다.

> ⚠️ **본 프로그램은 오직 데이터 분석 및 연구 목적에 한해 사용되어야 하며, 민감한 자료의 유출 및 악용, 역공학(Reverse Engineering)은 금지됩니다.**

<br>

## 주요 기능

| 기능 항목          | 설명                                                    |
|-------------------|---------------------------------------------------------|
| **SPF 파일 처리** | LaTale 리소스 아카이브 파일을 추출                     |
| **TBL 파일 처리** | 스프라이트 이미지 테이블 파일을 Excel로 변환           |
| **LDT 파일 처리** | 커스텀 테이블 파일을 Excel로 변환 (엑셀 유사 포맷)     |

<br>

## 사용 방법

1. 프로그램을 실행합니다.
2. 처리할 파일 형식에 해당하는 버튼을 클릭합니다.
3. 파일 선택 창에서 원하는 파일을 선택합니다:
   - `.SPF`, `.TBL`, `.LDT` 파일 모두 다중 선택 가능
4. 게임 설치 경로에서 `.SPF` 파일을 찾을 수 있습니다.
5. 예시 흐름:
   - `ROWID.SPF` 추출 → 다수의 `.LDT` 파일 획득(ROWID.SPF 추출시 LDT파일을 얻을수 있습니다.)
   - `.LDT` 처리 → 각각 Excel 파일로 변환

<br>

### 예시 스크린샷

- SPF 파일 위치  
  ![](https://i.imgur.com/LvH6wNU.png)

- ROWID.SPF -> LDT 파일 추출
  ![](https://i.imgur.com/tonDf5a.png)
  ![](https://i.imgur.com/pI4jZ0k.png)
  ![](https://i.imgur.com/ssyp91D.png)

- LDT -> Excel로 변환된 결과  
  ![](https://i.imgur.com/Y0pGHCR.png)

<br>

## 출력 구조

### 1. SPF 파일 처리

- 결과 경로: `SPF_Output/`
- 예시 구조:
구조 예시:

```
SPF_Output/
├── ROWID/
│   └── (ROWID.SPF에서 추출된 파일들)
└── ITEM/
    └── (ITEM.SPF에서 추출된 파일들)
```

<br>

### 2. TBL 파일 처리

- 결과 경로: 선택한 TBL 파일의 디렉토리 내 `TBL_Output/` 폴더
- 각 TBL 파일은 Excel 형식으로 저장

<br>

### 3. LDT 파일 처리

- 결과 파일: 입력된 `.LDT` 파일과 동일한 이름의 `.xlsx` 파일 생성
- 예: `ITEM.LDT` → `ITEM.xlsx`

<br>

## 주의사항

- SPF 파일은 각각 개별 폴더로 추출됩니다.
- 대용량 파일의 경우 처리에 시간이 소요될 수 있습니다.
- 처리 중 오류가 발생하면 로그 창에 메시지가 출력됩니다.

<br>

## 시스템 요구사항

- 운영체제: **Windows 10 이상**
- 런타임: **.NET 6.0 Runtime**
- 메모리: **최소 4GB RAM 권장**
- 저장공간: **충분한 여유 공간 확보 (파일 크기에 비례)**

<br>

## 문의

**개발자:** chipok(kimbap918)
**버전:** 1.0.0

![](https://i.imgur.com/KLPKxB1.png)
