---
order: 3
---

# 이성 사용 (Combat)

## 일반 설정

- `이성 사용`의 일반 설정에있는 `이성 회복제 사용 + 순오리지늄 사용`과 `횟수 제한` 및 `드롭 제한` 세 가지 옵션은 하나만 만족해도 종료가 됩니다.

  - `이성 회복제` 는 특정 횟수의 이성 회족제를 사용해 이성을 회복합니다. (연속으로 이성회복제 사용이 가능합니다)
  - `순오리지늄` 은 특정 횟수의 순오리지늄을 사용하며, 이성 회복제가 남아있을 경우 사용되지 않습니다.
  - `횟수 제한` 은 선택한 스테이지를 몇번 클리어 할 지 정합니다. (예시: 15번 클리어 후 정지)
  - `드롭 제한` 은 특정 재화를 몇개 획득할 지 정합니다. (5개의 장치 획득 후 정지)

- `드롭 제한`과 `스테이지 선택`은 연관되어 있지 않습니다. `드롭 제한`은 재료의 개수를 기준으로 작업을 종료하는 스위치일 뿐 재료를 지정한다고 해서 스테이지를 자동으로 설정해주는 것은 아닙니다.
- `순오리지늄`은 `이성 회복제` 이후에만 판단하므로 MAA는 이성 회복제가 없는 경우에만 이성을 보충합니다. 그래서 `순오리지늄`을 선택한 경우, `이성 회복제`의 사용 횟수를 보유하고 있는 `이성 회복제`보다 더 많이 설정해야 합니다!

::: details 예시
| 이성 회복제 | 순오리지늄 | 횟수 제한 | 드롭 제한 | 결과 |
| :---------: | :--------: | :-------: | :-------: | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| | | | | 보유한 이성을 소모하고 정지합니다. |
| 2 | | | | 현재 이성을 소모한 후, 이성 회복제를 `2`회 소모하고 정지합니다. |
| _999_ | 2 | | | 현재 이성을 소모한 후, 이성 회복제를 소모하고, 순오리지늄을 `2`회 사용 후 정지합니다. |
| | | 2 | | 지정한 스테이지를 `2`회 반복하고 정지합니다. |
| | | | 2 | 특정 재화를 `2`개 획득하면 정지합니다. |
| 2 | | 4 | | 작전을 `4`회 시도하며, 이성이 부족하면 최대 `2`개의 이성 회복제를 사용합니다.  |
| 2 | | | 4 | 특정 재화를 `4`개 획득하면 정지하며, 이성이 부족하면 최대 `2`개의 이성 회복제를 사용합니다. |
| 2 | | 4 | 8 | 작전을 `4`회 시도하며, 작전이 전부 끝나기전에 재화를 `8`개를 획득하면 정지합니다. 이성이 부족하면 최대 `2`개의 이성 회복제를 사용합니다. |
| _999_ | 4 | 8 | 16 | 모든 이성 회복제를 사용하며, `4`개의 순오리지늄을 사용합니다. 단, `8`회의 작전을 끝내면 정지하며, 그 이전에 `16`개의 재화를 획득하면 정지합니다. |
|  | 2 | | | `2`개의 순오리지늄을 사용하며, 이성을 전부 소모하면 정지합니다.     |
| 2 | 4 | | | `2`개의 이성 회복제를 사용하며, 이후 `4`개의 순오리지늄을 사용합니다. 이성을 전부 소모하면 정지합니다. |
:::

### 작전 개시 (이성 사용)

- 만약 여러분이 원하는 스테이지가 목록에 없다면 MAA에서 `현재/최근`을 선택한 다음 게임 내에서 수동으로 스테이지를 찾으세요.
스테이지 이름, 정보, 소모 이성이 뜨고 오른쪽 하단에 대리지휘와 시작 버튼이 표시된 화면으로 가세요.
- 해당 화면이 아닌 경우 `현재/이전`은 자동으로 가장 최근에 실행한 스테이지로 이동합니다.
- 또는 작업 `설정` - `이성 사용` - `고급 설정`에서 `스테이지 코드 수동 입력`을 체크해 스테이지 코드를 직접 입력할 수 있습니다. 현재 내비게이션할 수 있는 스테이지는 다음과 같습니다:
  - 모든 메인 스토리 스테이지. 표준 또는 어려움 난이도를 전환하려면 스테이지 코드 뒤에 -NORMAL 또는 -HARD를 추가하세요.
  - 용문폐 혹은 작전 기록의 5/6스테이지는 `CE-6`/`LS-6`를 입력해야 합니다. MAA는 6 스테이지가 대리 지휘가 불가능할 경우자동으로 5 스테이지로 전환합니다.
  - 스킬 북, 구매 증명서, 카본 부품 5스테이지는 `CA-5`/`AP-5`/`SK-5`를 입력해야 합니다.
  - 모든 칩 스테이지. 완전한 스테이지 코드를 입력해야 합니다. 예: `PR-A-1`.
  - 섬멸 작전. `Annihilation`을 입력해야 합니다.
  - 상시 개방 이벤트의 경우 `OF-1`/`OF-F3`/`GT-5`와 같이 입력합니다.
  - 현재 개방된 사이드 스토리 이벤트의 세 개의 스테이지입니다. [API](https://ota.maa.plus/MaaAssistantArknights/api/gui/StageActivity.json)에서 업데이트를 자동으로 다운로드 한 후 화면 하단에 표시됩니다. 
  - 재개방된 사이드 스토리 이벤트. `SSReopen-<스테이지 접두사>`를 입력하면 XX-1~XX-9 스테이지를 한 번에 완료할 수 있습니다. 예: `SSReopen-IC`.

::: details 예시 화면
![Image](https://github.com/MaaAssistantArknights/MaaAssistantArknights/assets/128385247/c57fc9ed-42be-4df3-8056-64be2e2d4652)
:::

### 섬멸 작전

  - MAA는 현재 게임에서 전투 시작 페이지로 이동하기 위해 오른쪽 상단의 핀을 사용합니다. 현재 기간의 섬멸이 `전권 위임`으로 설정되어 있으며 `PRTS 섬멸 작전 대리권`을 충분히 가지고 있어야합니다.
  - 현재 섬멸 작전에서 400킬을 한 독타들만 MAA가 자동으로 진행합니다.

## 고급 설정

### 대체 스테이지

그날 그날의 개방 여부에 따라 선택된 스테이지가 전투되는지 여부를 결정합니다. 즉, 첫 번째 개방된 스테이지를 전투합니다.

1. 용문폐, 1-7, 작전기록 스테이지 순으로 선택하세요:
  - 용문폐, 1-7, 작전기록 스테이지가 모두 열려있는 경우 용문폐 스테이지를 실행하고 1-7/작전기록 스테이지는 실행되지 않습니다. 이때 플레이어가 용문폐 스테이지 대리를 개방하지 않은 경우 작업이 실패합니다
  - 1-7, 작전기록 스테이지가 열려있는 경우 1-7을 실행하고 작전기록 스테이지는 실행되지 않습니다. 이때 플레이어가 1-7 대리를 개방하지 않은 경우 작업이 실패합니다.
2. 섬멸 작전, 용문폐, 1-7 스테이지를 차례로 선택하면 섬멸을 먼저 시도하고 후속 로직이 이전과 같이 실행됩니다. 섬멸 전투 결과는 다른 예비 스테이지의 필터링 로직에 영향을주지 않습니다.

### 남은 이성

`이성 사용`이 종료된 후에 시작되며, 이성 회복제 사용, 순오리지늄 사용, 횟수 제한, 드롭 제한, 연속 전투 횟수 등의 제어를 받지 않고, 이성을 모두 소비하면 종료됩니다.

- 스테이지 개시 시 이성이 부족한 경우, 남은 이성 스테이지로 이동하여 "나머지" 이성을 소모합니다. (예: 1-7)
- 이성이  부족하여 연속 전투 횟수가 너무 높게 설정된 경우에도 자동으로 단일 전투 횟수로 선택되어 이성을 모두 소비합니다(예: 1-7을 6회 연속 전투 설정하지만, 이성이 30밖에 되지 않는 경우, 자동으로 연속 전투 없는 1-7로 전환됩니다).
- 여전히 이성이 부족하면 작업을 중지합니다.(예: 6 이하의 이성)
- 남은 이성 선택 스테이지가 개방되지 않은 스테이지인 경우, 이성 사용에 실패합니다.

### 연속 전투 횟수

- 현재 MAA는 사용자가 설정한 횟수만큼 연속 전투를 진행하며, 최대 연속 전투 횟수를 자동으로 인식하는 기능은 아직 지원되지 않습니다.
- 설정된 횟수가 많지만 이성이 부족한 경우, MAA는 직접적으로 `이성 회복제 사용` 또는 `순오리지늄 사용`을 수행하고 계속해서 연속 전투를 시도합니다.
- 만약 `이성 회복제 사용` 또는 `순오리지늄 사용`이 설정되어 있지 않은 경우, MAA는 이성이 부족하다고 판단하고 이성 사용을 종료합니다. 만약 `남은 이성`이 설정되어 있다면, MAA는 바로 `남은 이성` 스테이지를 시작합니다.

### 드롭 인식

- 자동으로 자재 드롭을 인식하고 통계를 내며 [펭귄 물류](https://penguin-stats.cn/) 및 [Yituliu](https://ark.yituliu.cn/)로 자동으로 업로드 합니다.
- 수동으로 펭귄물류 ID를 설정할 수 있습니다.

## 비정상 상황 감지 (대처)

- `대리 지휘`가 선택되지 않는 경우에도 자동으로 선택해줍니다.
-  연결이 끊어진 후 또는 새벽 4시에 끊어진 후 자동으로 재연결되어 게임에서 마지막으로 선택한 스테이지를 계속해서 플레이할 수 있습니다. 다음 날로 넘어가려면 마지막 스테이지 선택을 확인하세요.
- 레벨 업 상황은 자동으로 처리되며, 미션 실패 시에는 해당 작업이 중단됩니다.