# TracArena ⚔️ — P2P Duel Gaming on Intercom

> A peer-to-peer gaming arena built on top of [Intercom](https://github.com/Trac-Systems/intercom) by Trac Systems.

![TracArena](https://img.shields.io/badge/Intercom-Fork-00ffe7?style=flat-square)
![Status](https://img.shields.io/badge/status-live-00ffe7?style=flat-square)

---
<img width="1010" height="832" alt="image" src="https://github.com/user-attachments/assets/724f74da-ccbd-4156-83b1-8f1a6b88dbf1" />

## 🎮 What is TracArena?

TracArena is a **P2P duel gaming platform** that uses Intercom sidechannels for real-time challenge negotiation between peers and a replicated-state leaderboard layer for persistent rankings.

Players can:
- **Challenge** other Trac peers to on-chain duels (Rock · Paper · Scissors)
- **Earn XP** for wins, tracked on a shared global leaderboard
- **Receive TNK rewards** each epoch based on leaderboard ranking
- **Connect Trac wallet** to register identity and receive payouts

All coordination happens through Intercom's P2P sidechannel protocol — no centralized server needed.

---

## 🚀 How to Run

```bash
# Clone this repo
git clone https://github.com/YOUR_USERNAME/TracArena

# Open the app
open index.html
# or serve locally:
npx serve .
```

No build step required. Pure HTML/CSS/JS.

---

## 📸 Proof of Concept

The app is fully functional in `index.html`:
- Live P2P feed simulation via Intercom sidechannel messages
- Real-time duel with animated result states (WIN / LOSE / DRAW)
- Global XP leaderboard that updates after each duel
- Trac wallet connection UI
- Challenge other peers by Trac address

---

## 🏗 Architecture

```
Player A ──[Intercom sidechannel]──► Player B
    │                                    │
    └──── RPS move encrypted & sent ─────┘
                    │
            ┌───────▼────────┐
            │ Replicated     │
            │ State Layer    │
            │ (Leaderboard)  │
            └────────────────┘
```

- **Sidechannel layer**: Fast P2P move negotiation (sub-second)
- **State layer**: Durable leaderboard synced across peers
- **TNK reward pool**: Distributed each epoch to top-ranked players

---

## 💳 Trac Address (for TNK payout)

```
trac1kcskf0tca4k7jv0xatkr7ypgu0hg46eeegk0982d2v8a5flpffjqdhlyh0
```

> Replace the above with your actual Trac address before submitting.

---

## 📋 Skills File

See [`SKILL.md`](./SKILL.md) for agent instructions on how to interact with TracArena via Intercom.

---

## 🔗 Links

- Upstream: [Trac-Systems/intercom](https://github.com/Trac-Systems/intercom)
- Awesome list: [Trac-Systems/awesome-intercom](https://github.com/Trac-Systems/awesome-intercom)

---

Built with ❤️ on the Trac Network.
