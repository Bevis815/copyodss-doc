# CopyOdds 문서

CopyOdds는 [Polymarket](https://polymarket.com) 기반의 **스마트 머니 분석 + 자동 카피 트레이딩** 플랫폼입니다. 뛰어난 실적을 가진 예측 시장 트레이더를 찾아내고, 그들의 체결을 수탁형 거래 계정에서 자동으로 따라 할 수 있습니다.

이 문서는 현재 앱(`app.copyodds.io`)의 인터페이스와 흐름을 반영합니다. 버튼과 메뉴 이름은 앱의 영어 UI와 동일합니다.

## 네 단계로 시작하기

1. **로그인 / 회원가입** — 이메일 인증 코드, Passkey 또는 Telegram
2. **입금** — Polygon 또는 BSC 네트워크의 USDC / USDT를 수탁형 주소로 전송
3. **플랫폼 Gas 구매** — 자동 카피 트레이딩용 서비스 수수료 크레딧 (온체인 MATIC이 아님)
4. **카피** — **Leaderboard** 또는 **Smart money**에서 트레이더 선택 → **Follow** (팔로우) 탭 → 카피 모드 선택 (기본값: **Ratio**) → 규칙 저장

어디서부터 시작해야 할지 모르겠다면 [앱 둘러보기](getting-started/app-tour.md)부터 시작하세요.

## 카피를 시작하기 전에

| 항목 | 요구 사항 |
|------|-------------|
| 플랫폼 Gas | **0보다 커야 함** (그렇지 않으면 카피를 활성화할 수 없으며, Gas가 소진되면 매수가 건너뛰어집니다) |
| USDC 잔액 | 실제 매수를 위해 최소 약 **$1** 이상 권장 |
| 거래 계정 | 보통 로그인 후 자동으로 개설됨 |

## 주요 진입점 (앱 내비게이션 기준)

| 기능 | 경로 / 내비게이션 |
|---------|-------------------|
| 리더보드 (카피 풀 일일 수익) | **Leaderboard** → `/` (홈 페이지) |
| 스마트 머니 | **Smart money** → `/smart-money` |
| 내 카피 | **My copy trading** → `/copy-rules` |
| 카피 활동 | **Copy activity** → `/feed` |
| 시뮬레이션 카피 트레이딩 | **Simulation copy trading** → `/copy-trading/simulation` |
| 내 포지션 | **My positions** → `/executions/positions` |
| 거래 내역 / 손익 | **Executions** → `/executions/records`, `/executions/daily-pnl` |
| 플랫폼 Gas 스토어 | **Store** → `/store` |
| 제휴 프로그램 | **Affiliation** → `/affiliate` |
| 입금 / 출금 | **Deposit / Withdraw** → `/wallets/deposit`, `/wallets/withdraw` |
| 프로필 (자산 개요) | **Profile** → `/profile` |
| 거래 기록 | **Transaction history** → `/wallets/ledger` |
| 설정 및 보안 | **Settings** → `/settings` |
| 기기 및 Passkey | **Settings → Devices** → `/settings/devices` |
| 모바일 다운로드 | **Mobile App** → `/mobile-app` |
| 사용자 가이드 | **User guide** → `/help` |

## 권장 읽기 순서

1. **시작하기** (소개 → 빠른 시작 → 앱 둘러보기)
2. **리더보드 / 스마트 머니** (트레이더 선택, 점수와 낙폭 확인)
3. **카피 트레이딩** (카피 시작, 관리 및 확인 방법)
4. **지갑** (입금, Gas, 출금, 거래 기록)
5. **계정 및 설정, 보안** (계정을 안전하게 유지)
6. **제휴** (공유를 통해 수익을 얻고 싶을 때)

## 이 문서에 대하여

- 이 문서는 제품 사용 방법만을 설명하며 **투자 조언이 아닙니다**.
- 인터페이스는 지속적으로 업데이트됩니다. 스크린샷이 사용 중인 버전과 약간 다르다면 앱에 표시되는 내용을 기준으로 하세요.

## 고객 지원 문의

다음 정보를 준비해 주세요: 가입한 이메일, 작업 시각, 오류 스크린샷, 그리고 **Trade history**의 관련 ID / 상태 / 온체인 해시.
