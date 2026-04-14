# Dismissal Shop Prototype

브라우저에서 **5가지 서로 다른 팝업 해제(dismissal) 인터랙션**을 순차적으로 체험하는 쇼핑몰 프로토타입입니다.

## 실행 방법

- `dismissal-shop-prototype/index.html` 파일을 브라우저로 열면 됩니다.
- 콘솔(`DevTools → Console`)에서 이벤트 트래킹 로그를 확인할 수 있습니다.

## 시나리오 흐름

상단의 **실험 시작** 버튼을 누르면 5단계가 순차 진행됩니다.

- **Scroll-to-dismiss**: 팝업 내부를 아래로 스크롤(160px 이상)하면 닫힘
- **Swipe-to-dismiss**: 팝업 카드 자체를 드래그해 임계값(120px) 이상 이동하면 날아가며 닫힘
- **Backdrop tap**: 팝업 바깥(딤드 영역) 탭하면 닫힘
- **Close button tap**: 오른쪽 위 × 버튼만 닫힘 (배경 탭은 무효)
- **Auto-dismissal**: 5초 후 자동 닫힘 + 진행률 바 표시

## 이벤트 트래킹

콘솔에 다음이 출력됩니다.

- `[popup_open]`: 팝업 오픈 시각/단계/방식
- `[invalid_attempt]`: 해당 단계에서 유효하지 않은 조작 시도(누적)
- `[popup_dismiss]`: 닫힘 사유 + 소요시간 + 무효 시도 카운트
- `[scenario_complete]`: 5단계 완료

