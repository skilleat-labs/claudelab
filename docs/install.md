# 시작하기: 설치 (교육 첫 15분, 강사와 같이)

!!! info "4회차 첫 15분에 강사와 같이 합니다"
    미리 하지 않아도 됩니다. 교육 당일 강사가 화면으로 보여 드리면 한 단계씩 따라 하세요. 15분이면 끝납니다.

!!! warning "IT 담당자에게 미리 부탁할 것 (임원분은 링크만 전달)"
    가상화 설정(3단계)은 관리자 권한이 필요해서 교육 현장에서는 고칠 수 없습니다.
    IT 담당자가 교육 전에 노트북마다 **3단계와 4단계만** 확인해 두면 당일 막히지 않습니다. 이 페이지 링크를 IT 담당자에게 보내 주세요.

## 바로 설치

[:material-microsoft-windows: Windows용 내려받기](https://claude.ai/api/desktop/win32/x64/setup/latest/redirect){ .md-button .md-button--primary }
[:material-apple: Mac용 내려받기](https://claude.ai/api/desktop/darwin/universal/dmg/latest/redirect){ .md-button }

<small>누르면 설치 파일이 바로 내려받아집니다. Arm 프로세서 Windows 노트북(예: Snapdragon)은 [Windows Arm용](https://claude.ai/api/desktop/win32/arm64/setup/latest/redirect). 공식 페이지에서 직접 고르려면 [Claude 다운로드 페이지](https://claude.com/download){ target=_blank } · 웹에서 바로 쓰려면 [claude.ai](https://claude.ai){ target=_blank }</small>

## 한눈에 보기

- [ ] **1단계** Claude 데스크톱 앱 설치
- [ ] **2단계** 회사 계정(Team)으로 로그인
- [ ] **3단계** (Windows) 가상화가 켜져 있는지 확인
- [ ] **4단계** Cowork 준비 상태 점검
- [ ] **5단계** 앱을 한 번 열어 작업 공간 내려받기
- [ ] **6단계** 화면 확인

---

## 1단계. Claude 데스크톱 앱 설치

=== "Windows"

    [:material-download: Windows용 설치 파일 내려받기](https://claude.ai/api/desktop/win32/x64/setup/latest/redirect){ .md-button .md-button--primary }

    1. 위 버튼을 누르면 설치 파일(Claude Setup)이 내려받아집니다.
    2. 내려받은 파일을 실행합니다. (Arm 노트북은 [Windows Arm용](https://claude.ai/api/desktop/win32/arm64/setup/latest/redirect))

    !!! warning "'Trusted app installs must be enabled to install Claude' 창이 뜨면"
        Microsoft Store 밖의 앱 설치가 막혀 있다는 뜻입니다.

        1. 창에서 **예**를 누르거나, **설정 › 시스템 › 개발자용**으로 갑니다.
        2. **개발자 모드**를 **켬**으로 바꿉니다.
        3. 설치 파일을 다시 실행합니다.

        회사 노트북이라 이 설정이 잠겨 있으면 IT 담당자에게 **'신뢰할 수 있는 앱 설치 허용'**을 요청하세요.

=== "Mac"

    [:material-download: Mac용 설치 파일 내려받기](https://claude.ai/api/desktop/darwin/universal/dmg/latest/redirect){ .md-button .md-button--primary }

    1. 위 버튼을 누르면 설치 파일이 내려받아집니다.
    2. 내려받은 파일을 열고, Claude 아이콘을 **응용 프로그램(Applications)** 폴더로 끌어다 놓습니다.

    macOS 14 (Sonoma) 이상이 필요합니다. 메뉴 › 이 Mac에 관하여에서 확인할 수 있습니다.

## 2단계. 회사 계정(Team)으로 로그인

1. 메일함에서 **Claude Team 초대 메일**을 찾아 초대를 수락합니다.
2. Claude 앱을 열고 **회사 메일 주소**로 로그인합니다.
3. 앱 왼쪽 아래 프로필을 눌러 **회사(조직) 이름**이 보이는지 확인합니다.

!!! warning "개인 계정으로 로그인하지 마세요"
    개인 Gmail 계정으로 로그인하면 회사 Team 플랜 기능(Cowork, 스킬, 커넥터)이 보이지 않을 수 있습니다. 이미 개인 계정으로 들어갔다면 로그아웃 후 회사 메일로 다시 로그인하세요.

## 3단계. (Windows) 가상화가 켜져 있는지 확인 · 30초

Cowork는 PC 안에 작은 가상 컴퓨터를 띄워 그 안에서 일합니다. 그래서 가상화가 켜져 있어야 합니다. 요즘 노트북은 대부분 처음부터 켜져 있으니 **확인만** 하면 됩니다.

1. **Ctrl + Shift + Esc**로 작업 관리자를 엽니다.
2. **성능** 탭 › **CPU**를 누릅니다.
3. 오른쪽 아래 **가상화** 항목을 봅니다.

| 보이는 글자 | 할 일 |
| --- | --- |
| **가상화: 사용** | 끝. 4단계로 갑니다 |
| **가상화: 사용 안 함** | 직접 바꾸지 마세요. 화면을 사진으로 찍어 IT 담당자에게 보냅니다 |

??? info "IT 담당자용 메모 (눌러서 펼치기)"
    - BIOS(UEFI)에서 Intel VT-x 또는 AMD-V를 켭니다.
    - 관리자 PowerShell에서 Windows 기능 Virtual Machine Platform을 켜고 **다시 시작**합니다 (시스템 종료 말고).
      ```text
      Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform -All
      ```
    - 요구 사항: Windows 10 (2004 이상) 또는 11, S 모드 불가, 메모리 8GB 이상, 여유 공간 약 20GB.
    - 출처: claude.com/docs 'Installation and setup', 'Windows fleet checklist'

Mac은 이 단계를 건너뜁니다.

## 4단계. Cowork 준비 상태 점검 · 5분

Anthropic이 제공하는 점검 프로그램입니다. 설치나 로그인 없이 실행됩니다.

| 내 PC | 점검 프로그램 |
| --- | --- |
| Windows (대부분의 노트북) | [Windows x64용 내려받기](https://claude.ai/api/desktop/win32/x64/cowork-readiness-check/latest/redirect) |
| Windows (Arm 노트북) | [Windows arm64용 내려받기](https://claude.ai/api/desktop/win32/arm64/cowork-readiness-check/latest/redirect) |
| Mac | [Mac용 내려받기](https://claude.ai/api/desktop/darwin/universal/cowork-readiness-check/latest/redirect) |

!!! success "이렇게 나오면 준비 완료"
    **This computer is ready for Cowork**

빨간 항목이 있으면 그 줄을 사진으로 찍어 IT 담당자에게 보내 주세요.

## 5단계. 앱을 한 번 열어 작업 공간 내려받기

Claude 앱을 처음 열고 일을 하나 맡기면 작업 공간(1GB 이상)을 내려받습니다. 몇 분 걸릴 수 있으니 설치하자마자 바로 한 번 보내 두고, 받는 동안 6단계를 확인합니다.

1. Claude 앱 위쪽에서 **말풍선 아이콘**을 누르고, 입력창 왼쪽 아래에서 **Cowork**를 고릅니다. 선택 버튼이 없으면 이미 합쳐진 화면이니 그대로 씁니다.
2. 아래 문장을 입력하고 보냅니다.

```text
안녕. 지금 쓸 수 있는 기능을 세 줄로 알려줘.
```

3. 답이 오면 끝입니다.

## 6단계. 화면 확인

| 확인할 것 | 어디서 |
| --- | --- |
| 위쪽 **말풍선 아이콘**이 선택되어 있다 (**</>**는 개발자용 Claude Code라 쓰지 않음) | 앱 위쪽 |
| 입력창 왼쪽 아래에서 **Cowork**를 고를 수 있다 (버튼이 없으면 합쳐진 화면) | 입력창 아래 |
| 입력창에 **/** 를 치면 명령 목록이 나온다 | 입력창 |
| 모델이 **Opus 5.5**로 되어 있다 (Fable은 고르지 않기) | 입력창 모델 선택 |
| 설정 › Capabilities에서 **코드 실행 및 파일 생성**이 켜져 있다 | 설정 |

!!! warning "Chat에서 계속 대화한다고 Cowork가 되지는 않습니다"
    Chat은 묻고 답하기만 합니다. 폴더를 열고 파일을 만드는 실습은 반드시 **Cowork**에서 합니다.

!!! tip "다 됐으면"
    [4회차 실습 가이드](day4/index.md)로 갑니다. 강사가 다음 순서를 안내합니다. 화면이 조금 달라도 괜찮습니다. 2026년 9월부터 Chat과 Cowork가 하나로 합쳐지는 중이라 메뉴 이름이 다를 수 있습니다.

## 오늘 쓸 자료

실습 자료는 **실습 단계마다 그 자리에 내려받기 버튼**이 있습니다. 미리 받지 않아도 됩니다. 한꺼번에 받고 싶으면 [내려받기](downloads.md) 페이지를 쓰세요.

| 언제 | 자료 |
| --- | --- |
| 4회차 1교시 1-3 | [실습1_받은자료(정리전).zip](files/practice1-materials.zip) |
| 4회차 2교시 2-9 (막혔을 때만) | [industry-competitor-analysis.zip](files/industry-competitor-analysis.zip) |
| 4회차 3교시 3-8 (시간이 모자라면) | [value-chain-diagnosis.zip](files/value-chain-diagnosis.zip) |

## 막혔을 때

| 증상 | 해결 |
| --- | --- |
| 설치 중 'Trusted app installs must be enabled' | 1단계 경고 상자대로 개발자 모드 켜기. 잠겨 있으면 IT에 요청 |
| 'Cowork를 사용할 수 없음' 또는 작업 공간이 시작되지 않음 | 3단계 가상화 확인 → 4단계 점검 → 빨간 항목을 IT에 |
| 로그인했는데 Cowork나 스킬 메뉴가 없다 | 회사 계정인지 확인(2단계). 맞으면 관리자에게 Cowork, 스킬 사용이 켜져 있는지 요청 |
| 작업 공간 내려받기가 계속 실패 | 회사 방화벽이 막는 경우. IT에 downloads.claude.ai 허용 요청 |
