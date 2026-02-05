## 🧇 Waffle

**Waffle**은 P2P 기반의 탈중앙화 AI 코드 수정 마켓플레이스입니다.
사용자는 코드 수정을 요청하고, *Baker*라 불리는 프로바이더는 AI를 활용해 코드를 수정한 뒤
그 대가로 **SYRUP 토큰**을 보상받습니다.

---

## ✨ Key Features

* 🔗 **P2P 탈중앙화 구조** — 중앙 서버 없이 사용자와 Baker 직접 연결
* 🔐 **블록체인 에스크로우** — 안전한 결제 및 환급 보장
* 🤖 **AI 기반 코드 수정** — Google Gemini API 활용
* 🧑‍💻 **CLI 중심 UX** — 어디서든 빠르게 사용 가능
* 🌍 **Permissionless** — 누구나 Baker로 참여 가능

---

## 🛠 Tech Stack

### Backend

| Category       | Technology        | Description                      |
| -------------- | ----------------- | -------------------------------- |
| Language       | Go 1.25           | CLI 및 네트워크 로직 구현                 |
| P2P Networking | libp2p            | mDNS 기반 피어 발견 및 통신               |
| AI Engine      | Google Gemini API | AI 코드 수정 처리 (`gemini-2.5-flash`) |

---

### Blockchain

| Category       | Technology           | Description         |
| -------------- | -------------------- | ------------------- |
| Network        | Base Sepolia Testnet | Ethereum L2 기반 테스트넷 |
| Smart Contract | Solidity ^0.8.20     | 요청 관리 및 에스크로우       |
| Token Standard | ERC-20               | SYRUP 토큰            |
| Security       | OpenZeppelin         | ReentrancyGuard 적용  |

---

### Interface / UX

| Category      | Technology                 | Description  |
| ------------- | -------------------------- | ------------ |
| CLI Framework | Cobra                      | 명령어 구조 및 파싱  |
| TUI           | Charmbracelet (Bubble Tea) | 인터랙티브 터미널 UI |

---

### Infra & Tooling

| Category             | Technology          | Description     |
| -------------------- | ------------------- | --------------- |
| Gas Relay            | Custom Relay Server | 가스리스 트랜잭션 처리    |
| Package Distribution | Go Install          | 단일 명령 설치        |
| Peer Discovery       | mDNS                | 로컬 P2P 노드 자동 탐색 |

---

## 🏗 Architecture

```text
waffle/
├── cmd/waffle/        # CLI commands
├── internal/
│   ├── p2p/           # P2P networking
│   ├── ai/            # Gemini AI integration
│   ├── contracts/     # Blockchain interaction
│   ├── wallet/        # Wallet management
│   └── ui/            # TUI components
├── contracts/         # Solidity smart contracts
└── relay/             # Gasless relay server
```

---

## 🚀 Getting Started

```bash
# Install
go install github.com/waffle-studio/waffle@latest

# Get testnet tokens
waffle faucet

# Check balance
waffle balance

# Create a code modification request
waffle bake
```

---

## 📜 License

MIT License
