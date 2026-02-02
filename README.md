# ElliottBotPro-HMS
Motor de trading hierárquico multi-timeframe baseado em direção macro, impulso micro e gatilhos de execução com controle rígido de risco.

# HierarchicalMarketEngine

A hierarchical, rule-based trading engine built in MQL5, designed to operate only when market conditions offer statistical advantage.

This project follows a strict operational principle:

> **Macro direction defines bias (4H),  
> Micro timeframes define impulse (1M–3M),  
> Execution timeframes define entry (5M).**  
> If one layer is misaligned, no trade is taken.

---

## 🧠 Core Philosophy

This system does not chase signals.  
It evaluates **market structure, momentum, and phase** before allowing any trade.

The engine prioritizes:
- Capital preservation
- High-quality setups
- Multi-timeframe confluence
- Deterministic decision-making

---

## 🏗️ System Architecture

The engine is divided into independent logical layers:

### 1. Macro Context (24H / 4H)
- RSI-based global bias
- Strong trend vs consolidation detection
- Absolute blocking of trades against macro direction

### 2. Micro Impulse Engine (1M / 2M / 3M)
- ADX-based momentum classification
- Sequential impulse validation
- Lateral market detection (no-trade zones)

### 3. Execution Trigger (5M)
- MACD histogram confirmation
- RSI safety zones
- Structural patterns (Quasimodo / Elliott)

### 4. Market Phase State Machine
- Active trend
- Exhaustion
- Loss of strength
- Breakout
- Confirmation

Phases must occur sequentially. No jumps are allowed.

---

## 🚦 Signal Classification

Every evaluation results in a deterministic classification:

- 🟢 **Confirmed Signal** — Trade allowed
- 🟡 **Alert Signal** — Waiting state
- 🔴 **Danger Signal** — Trade blocked

Each decision is logged with explicit reasons.

---

## 🛡️ Risk & Trade Management

- Dynamic Stop Loss and Take Profit
- Minimum Risk/Reward enforcement
- RSI-based exhaustion exits
- Consecutive loss protection
- Daily performance monitoring

---

## 📊 Logging & Transparency

All decisions are fully logged, including:
- Multi-timeframe alignment
- Market phase
- Signal score
- Probability estimation
- Final decision and reason

This allows full auditability and strategy validation.

---

## ⚠️ Important Notes

- This system trades **infrequently by design**
- It avoids sideways and low-quality markets
- Missing trades is preferred over bad trades

---

## 🧪 Status

🚧 Active development  
🔬 Strategy research & refinement  
📈 Backtesting and forward testing in progress

---

## 📄 License

This project is shared for educational and research purposes.
Use at your own risk.
