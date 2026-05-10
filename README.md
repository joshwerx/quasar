# quasar
A multi-blockchain trading platform with Pump.fun, LetsBonk, Ethereum, XRP, Solana, Binance, and more coming!  Automated per block-chain signal scoring, fast execution, RPC health, hot/cold paths, fast exits, and operator dashboards.  And so much more!

# Trading Platform Feature, Strategy, Entry, Exit, Gate, and Platform Breakdown

## Executive Summary

The trading platform is a Solana-based launch-trading system focused on pump.fun, BONK, PumpPortal, Yellowstone/Geyser, Helius, and fast token lifecycle management.

The platform combines real-time token discovery, multi-provider feed ingestion, automated entry and exit strategies, risk gates, execution routing, paper/live/shadow trading modes, reconciliation, dashboard visibility, and operator controls.

Its core value is:

speed + explainability + risk controls + execution routing + reconciliation + operator visibility

The system is best understood as a trading control plane rather than a single-purpose trading bot.

---

# 1. Platform Overview

## Core Platform Capabilities

- Real-time token intake
- Pump.fun token launch monitoring
- BONK launch monitoring
- PumpPortal WebSocket integration
- Yellowstone/Geyser feed integration
- PumpSwap monitoring
- Bonding-curve trade monitoring
- Account trade monitoring
- Token trade monitoring
- Migration/graduation tracking
- Paper trading
- Shadow trading
- Dry-run mode
- Live trading mode
- Automated buy execution
- Automated sell execution
- Strategy scoring
- Entry-gate evaluation
- Exit-gate evaluation
- Position tracking
- Trade journaling
- Runtime configuration
- Dashboard controls
- Audit logging
- Decision receipts
- Multi-route execution support
- Feed health monitoring
- Operator mission-control dashboard

---

# 2. Main Platform Layers

## Feed Layer

The feed layer receives market and token events from external providers.

### Feed Sources

- PumpPortal WebSocket
- PumpPortal Data API
- PumpSwap Data API
- Yellowstone/Geyser feed
- Helius RPC
- Helius Sender
- Solana RPC
- Jupiter route data
- Raydium/PumpSwap route data
- Pump.fun launch data
- BONK launch data

### Feed Events

- New token creation
- Token buy trades
- Token sell trades
- Account trades
- Token-specific trade stream
- Bonding-curve updates
- PumpSwap trade events
- Migration events
- Graduation events
- Creator activity
- Wallet activity
- Price movement
- Volume movement
- Unique trader activity
- Liquidity movement

---

# 3. Strategy Layer

The strategy layer evaluates whether a token is worth trading.

## Strategy Families

### 1. ML Graduation Strategy

A strategy focused on identifying tokens with a higher probability of graduation or meaningful early movement.

### Signals Used

- Trade count
- Unique buyer count
- Unique wallet count
- Price momentum
- Buy/sell ratio
- Total SOL volume
- Priority-fee activity
- Bribe/Jito activity
- MEV protection ratio
- Creator activity
- Bonding-curve progression
- Top-buyer concentration
- Holder concentration
- Early liquidity behavior

---

### 2. Momentum Ignition Strategy

A fast-entry strategy focused on early launch momentum.

### Signals Used

- Rapid buy activity
- Buy burst velocity
- Early price acceleration
- Rising unique buyer count
- Increasing trade frequency
- Expanding volume
- Low early sell pressure
- Strong short-window order flow

---

### 3. Velocity Compression Breakout Strategy

A strategy that looks for a token to compress, stabilize, and then break out with renewed flow.

### Signals Used

- Price compression
- Reduced short-term volatility
- VWAP reclaim
- Buy-side continuation
- Volume expansion after compression
- Higher trade quality
- Improved buyer participation
- Cleaner continuation structure

---

### 4. Microscalper Strategy

A fast in-and-out trading strategy designed for short-lived opportunities.

### Signals Used

- Small profit windows
- Short hold periods
- Fee-aware net-profit checks
- Take-profit levels
- Stop-loss levels
- Price movement over seconds
- Realized spread
- Priority-fee cost
- Network fee cost
- PumpPortal fee cost
- Slippage-adjusted profit

---

### 5. Burn-Centered Underwriting Strategy

A strategy that uses token burn behavior as a core quality signal.

### Signals Used

- Burn event timing
- Burn within early launch window
- Price band
- Priority-fee ceiling
- Early creator commitment
- Early launch structure
- Liquidity behavior
- Token maturity

---

### 6. MiroFish-Style Swarm Strategy

A multi-agent style strategy that evaluates a token from several independent perspectives.

### Agent Perspectives

- Narrative agent
- Order-flow agent
- Liquidity agent
- Maturity agent
- Crowd-participation agent
- Microstructure agent
- Fragility/risk agent

### Outputs

- Consensus score
- Entry score
- Exit pressure score
- Confidence level
- Veto signal
- Per-token memory
- Strategy recommendation

---

### 7. VWAP Reclaim Strategy

A strategy that looks for price to reclaim a meaningful average level with supporting flow.

### Signals Used

- Price reclaim above VWAP
- Buyer confirmation
- Volume confirmation
- Pullback quality
- Price continuation
- Reduced sell pressure
- Short-term trend recovery

---

### 8. Shadow Strategy Mode

A non-executing strategy mode that scores tokens and records outcomes without placing trades.

### Uses

- Strategy testing
- Signal comparison
- Paper/live comparison
- Model training
- Performance observation
- Decision quality review

---

### 9. Paper Strategy Mode

A simulated trading mode that follows the trading lifecycle without live funds.

### Uses

- Simulated entries
- Simulated exits
- Strategy validation
- Fee-aware simulation
- Position lifecycle testing
- Dashboard performance review
- Trade journal population

---

# 4. Entry System

The entry system determines when the platform should open a position.

## Entry Flow

New token detected
↓
Token state initialized
↓
Market data collected
↓
Feature snapshot created
↓
Strategy score calculated
↓
Entry gates evaluated
↓
Risk sizing calculated
↓
Execution route selected
↓
Buy submitted
↓
Buy confirmed
↓
Position opened
↓
Position monitored

---

## Entry Features

### Token Launch Features

- Token age
- Mint creation time
- Creator wallet
- Creator activity
- Token name
- Token symbol
- Launch source
- Bonding-curve state
- Pump.fun pool state
- BONK pool state
- Migration status
- Graduation status

### Market Features

- Current price
- Entry price
- Price momentum
- Price acceleration
- Volume momentum
- Trade velocity
- Buy velocity
- Sell velocity
- Total trade count
- Buy count
- Sell count
- Buy/sell ratio
- Net order flow
- Total SOL volume
- Short-window volume
- Liquidity score
- Price impact estimate
- Slippage estimate

### Trader Features

- Unique buyer count
- Unique wallet count
- Fresh wallet count
- Repeat buyer count
- Top buyer concentration
- Top holder concentration
- Whale participation
- Whale sell activity
- Buyer distribution
- Holder distribution

### Execution Features

- Priority fee
- Jito/bribe activity
- Network fee estimate
- Route availability
- Pool type
- Execution rail
- Expected slippage
- Expected fill quality
- Fee-adjusted entry quality

### Quality Features

- Minimum trade count
- Minimum unique traders
- Minimum volume
- Minimum liquidity
- Minimum momentum
- Maximum concentration
- Valid price band
- Valid pool
- Valid route
- Valid token metadata
- Valid launch source

---

# 5. Entry Gates

Entry gates are rules that determine whether a token is eligible for a buy.

## Token Gates

- Token age gate
- Minimum age gate
- Launch source gate
- Mint validity gate
- Metadata validity gate
- Token name gate
- Token symbol gate
- Suspicious title/name gate
- Pool validity gate
- Bonding-curve state gate
- Migration state gate
- Graduation state gate

## Market Gates

- Minimum liquidity gate
- Minimum volume gate
- Minimum trade count gate
- Minimum buy count gate
- Minimum unique buyer gate
- Minimum unique wallet gate
- Minimum buy/sell ratio gate
- Minimum price momentum gate
- Price band gate
- Maximum slippage gate
- Maximum price impact gate
- Maximum volatility gate
- Liquidity quality gate

## Wallet / Holder Gates

- Holder concentration gate
- Top buyer concentration gate
- Whale sell gate
- Wallet distribution gate
- Fresh buyer gate
- Creator wallet gate
- New creator gate
- Creator history gate

## Flow Gates

- Buy burst gate
- Trade velocity gate
- Volume acceleration gate
- Unique buyer acceleration gate
- Sell pressure gate
- Microstructure quality gate
- Signal strength gate
- Momentum confirmation gate
- VWAP reclaim gate
- Compression breakout gate

## Fee / Execution Gates

- Priority-fee ceiling gate
- Route availability gate
- Execution rail gate
- Slippage gate
- Fee-adjusted profitability gate
- Pool compatibility gate
- Live-mode gate
- Dry-run gate
- Paper-mode gate

## Strategy Gates

- ML confidence gate
- Graduation probability gate
- Momentum ignition gate
- Velocity compression gate
- Burn confirmation gate
- MiroFish consensus gate
- Strategy score threshold gate
- Signal detector gate
- Quality score gate

---

# 6. Exit System

The exit system determines when the platform should close a position.

## Exit Flow

Position opened
↓
Live price monitored
↓
Order flow monitored
↓
PnL calculated
↓
Fees calculated
↓
Exit strategy evaluated
↓
Exit gates evaluated
↓
Sell intent created
↓
Sell route selected
↓
Sell submitted
↓
Sell confirmed
↓
Balance reconciled
↓
Position closed
↓
Trade journal updated

---

## Exit Types

### Profit Exits

- Hard take-profit exit
- Fee-aware take-profit exit
- Net-profit exit
- Green exit
- Staged take-profit exit
- Trailing-profit exit
- Sustained-profit exit

### Loss Protection Exits

- Hard stop-loss exit
- Catastrophic drop exit
- Emergency exit
- Maximum drawdown exit
- Price breakdown exit

### Time-Based Exits

- Minimum hold timer
- Maximum hold timer
- Timed position close
- Stale position close
- Short-hold scalper exit

### Flow-Based Exits

- Sell pressure exit
- Whale sell exit
- Buy/sell ratio weakening exit
- Unique buyer slowdown exit
- Volume fading exit
- Trade frequency decline exit
- Microstructure weakening exit

### Technical Exits

- VWAP loss exit
- Failed continuation exit
- Oscillation exit
- Compression failure exit
- Momentum exhaustion exit
- Curve-risk exit
- Graduation-risk exit

### Operator Exits

- Manual sell
- Dashboard-triggered sell
- Emergency liquidation
- Strategy override sell

---

# 7. Exit Signals

## Profit / Loss Signals

- Current PnL percentage
- Net PnL after fees
- Gross proceeds
- Net proceeds
- Entry price
- Current price
- Fee-adjusted price
- Slippage-adjusted price
- Realized profit
- Unrealized profit
- Profit persistence duration

## Fee Signals

- PumpPortal fee
- Pump.fun fee
- Network fee
- Priority fee
- Jito tip
- Slippage cost
- Route cost
- Total execution cost
- Net profit after all costs

## Time Signals

- Position age
- Time since entry
- Minimum hold time
- Maximum hold time
- Time above profit threshold
- Time since last buy
- Time since last sell
- Time since last trade
- Time since migration/graduation event

## Market Signals

- Price movement
- Price velocity
- Price acceleration
- Volume movement
- Buy/sell ratio
- Buy pressure
- Sell pressure
- Whale sell count
- Large sell notional
- Liquidity movement
- Holder movement
- Curve progression
- Pool movement

## Microstructure Signals

- Trade frequency
- Trade quality
- Buyer distribution
- Seller distribution
- Spread behavior
- Slippage behavior
- Price impact
- Failed continuation
- Choppy movement
- Momentum exhaustion

---

# 8. Exit Gates

Exit gates determine whether a sell is eligible to execute.

## Position Gates

- Valid open position gate
- Position ownership gate
- Paper/live mode gate
- Position age gate
- Minimum hold gate
- Maximum hold gate
- Position size gate
- Token balance gate

## Profit Gates

- Take-profit gate
- Net-profit gate
- Fee-aware profitability gate
- Sustained-profit gate
- Green-exit gate
- Trailing-profit gate

## Loss Gates

- Stop-loss gate
- Catastrophic drop gate
- Drawdown gate
- Emergency exit gate
- Failed-continuation gate

## Flow Gates

- Whale sell gate
- Sell pressure gate
- Volume fade gate
- Buyer slowdown gate
- Microstructure weakness gate
- Buy/sell ratio deterioration gate

## Execution Gates

- Sell route gate
- Slippage gate
- Pool compatibility gate
- Signature gate
- Pending-sell dedupe gate
- Reconciliation gate
- Confirmation gate
- Balance check gate

---

# 9. Risk Management

## Trading Risk Controls

- Maximum position size
- Minimum position size
- Max open positions
- Per-token exposure limit
- Per-strategy exposure limit
- Max daily loss limit
- Consecutive loss protection
- Entry cooldown
- Exit cooldown
- Token cooldown
- Strategy cooldown
- Stop-loss protection
- Take-profit protection
- Fee-aware trade filtering
- Slippage protection
- Liquidity protection
- Holder concentration protection
- Whale sell protection

## Execution Risk Controls

- Priority-fee cap
- Jito-tip cap
- Slippage cap
- Route validation
- Pool validation
- Signature validation
- Confirmation check
- Balance reconciliation
- Duplicate sell prevention
- Pending-sell tracking
- Execution report logging
- Route fallback support

## Feed Risk Controls

- Feed heartbeat tracking
- WebSocket health checks
- Event freshness checks
- Subscription state tracking
- Reconnect logic
- Intake monitoring
- Token stream monitoring
- Account stream monitoring
- Trade stream monitoring

## Operator Risk Controls

- Dry-run mode
- Paper mode
- Shadow mode
- Explicit live-mode controls
- Dashboard runtime configuration
- Audit records
- Decision receipts
- Trade journal
- Gate visibility
- Strategy snapshot visibility
- Config-state visibility

---

# 10. Execution Layer

The execution layer routes buy and sell actions through supported providers.

## Execution Routes

- PumpPortal Lightning API
- PumpPortal local transaction API
- Helius Sender
- Jito bundle route
- Jupiter swap route
- Raydium route
- PumpSwap route
- Paper executor
- Dry-run executor
- Shadow executor

## Execution Features

- Buy execution
- Sell execution
- Paper buy execution
- Paper sell execution
- Dry-run simulation
- Route selection
- Route fallback
- Transaction creation
- Local signing support
- Hosted wallet support
- Priority-fee configuration
- Slippage configuration
- Jito tip configuration
- Signature handling
- Confirmation polling
- Token balance verification
- Execution reporting
- Trade reconciliation

---

# 11. Position Management

## Position Features

- Open position tracking
- Closed position tracking
- Paper position tracking
- Live position tracking
- Entry price tracking
- Current price tracking
- Token balance tracking
- PnL tracking
- Fee-adjusted PnL tracking
- Position age tracking
- Strategy attribution
- Entry reason tracking
- Exit reason tracking
- Sell intent tracking
- Reconciliation status tracking
- Trade journal linkage

## Position Lifecycle

Token selected
↓
Entry gates passed
↓
Buy submitted
↓
Buy confirmed
↓
Position opened
↓
Position monitored
↓
Exit condition triggered
↓
Sell submitted
↓
Sell confirmed
↓
Position closed
↓
Trade journal updated

---

# 12. Gate Truth / Audit System

The Gate Truth system explains why trades were allowed or blocked.

## Gate Truth Features

- Gate registry
- Active gate list
- Disabled gate list
- Effective gate state
- Strategy snapshot
- Strategy hash
- Decision receipts
- Entry receipt
- Exit receipt
- Pass/fail explanation
- Gate decision history
- Dashboard audit page
- Operator review tools
- Trade-level explainability
- Strategy-level explainability

## Decision Receipt Contents

- Token mint
- Strategy used
- Entry score
- Exit score
- Gate results
- Passed gates
- Blocked gates
- Feature snapshot
- Runtime config state
- Execution route
- Trade mode
- Timestamp
- Reason summary

---

# 13. Dashboard / Operator Console

The dashboard acts as the mission-control interface for the trading platform.

## Dashboard Areas

- Mission Control
- Overview
- Trades
- Orders
- Positions
- Gate Truth
- Audit
- Trade Journal
- Strategy Debugger
- Decision Debugger
- Runtime Config
- Execution Timeline
- Health Panel
- Paper Trading View
- Live Trading View
- Shadow Trading View
- Export Tools

## Dashboard Features

- Live status display
- Trading mode display
- Open positions view
- Closed positions view
- Trade history
- Order history
- Execution reports
- Gate pass/fail view
- Strategy score view
- Entry reason view
- Exit reason view
- PnL view
- Fee view
- Position timeline
- Runtime controls
- Strategy controls
- Export to CSV
- Export to JSON
- Audit visibility
- Health indicators

---

# 14. Trade Journal

The trade journal records the lifecycle of each trade.

## Trade Journal Fields

- Token mint
- Token name
- Token symbol
- Entry time
- Exit time
- Entry price
- Exit price
- Position size
- Gross PnL
- Net PnL
- Fees
- Slippage
- Strategy used
- Entry reason
- Exit reason
- Entry score
- Exit score
- Gates passed
- Gates blocked
- Execution route
- Transaction signature
- Confirmation status
- Reconciliation status
- Paper/live/shadow mode

---

# 15. Runtime Configuration

The runtime configuration system controls strategy behavior, execution settings, and risk limits.

## Config Categories

### Trading Mode

- Dry-run mode
- Paper mode
- Shadow mode
- Live mode

### Strategy Config

- Active strategy
- Entry score threshold
- Exit score threshold
- ML confidence threshold
- Momentum thresholds
- Burn confirmation settings
- Graduation settings
- Scalper settings
- VWAP reclaim settings
- Compression breakout settings

### Risk Config

- Max position size
- Min position size
- Max open positions
- Stop-loss threshold
- Take-profit threshold
- Trailing stop settings
- Max hold time
- Min hold time
- Daily loss limit
- Slippage cap
- Priority-fee cap

### Execution Config

- Primary execution route
- Backup execution route
- PumpPortal settings
- Helius settings
- Jito settings
- Jupiter settings
- Raydium settings
- PumpSwap settings
- Priority fee
- Jito tip
- Slippage tolerance

### Gate Config

- Token age gate
- Liquidity gate
- Title/name gate
- Creator gate
- Burn gate
- Whale gate
- Holder concentration gate
- Signal detector gate
- Quality gate
- Strategy gate
- Fee gate
- Execution gate

---

# 16. Storage / Persistence

The platform stores trading, execution, and audit information in SQLite.

## Stored Data Areas

- Pump events
- Token events
- Token subscriptions
- Trade events
- Open positions
- Closed positions
- Paper positions
- Live positions
- Execution reports
- Decision ledger
- Intent ledger
- Gate decision receipts
- Runtime config
- Strategy snapshots
- Pending sells
- Sell reconciliation
- Trade journal records
- Training samples
- Performance records

---

# 17. Machine Learning / Training Layer

The platform includes a foundation for model-assisted decisioning and strategy improvement.

## ML Features

- Feature snapshot generation
- Training sample storage
- Graduation probability scoring
- Entry probability scoring
- Exit pressure scoring
- Trade outcome labeling
- Strategy comparison
- Shadow-mode learning
- Paper-mode outcome review
- Probability model support
- Heuristic + ML hybrid scoring

## Example Feature Categories

- Trade count
- Unique wallet count
- Unique buyer count
- Buy/sell ratio
- Volume
- Price momentum
- Priority fees
- MEV protection
- Bribe/Jito signal
- Top buyer concentration
- Holder concentration
- Creator behavior
- Liquidity score
- Curve progression
- Graduation status

---

# 18. Security Layer

## Security Features

- API-key separation
- Private-key handling
- Secret redaction
- Local signing support
- Hosted wallet support
- Dashboard access control direction
- Dry-run default support
- Explicit live-mode support
- Runtime safety checks
- Audit logging
- Execution logging
- Sensitive value protection
- Password-derived encryption design option
- Session-based secret unlocking design option

## Secret Protection Model

User password
↓
Key derivation function
↓
Session encryption key
↓
Encrypted API keys and private keys
↓
Session-only unlock
↓
Runtime execution access

---

# 19. Compliance / Governance Features

## Governance Features

- Audit logs
- Decision receipts
- Execution records
- Trade journal
- Paper/live labeling
- Strategy attribution
- Gate attribution
- Operator visibility
- Config-state records
- Exportable history
- Reconciliation records

## Compliance-Aware Design Areas

- Market activity logging
- Strategy explainability
- Trade decision records
- API usage tracking
- Provider terms awareness
- Paper/live separation
- Performance record clarity
- Transaction confirmation records
- User fund handling controls
- Tax-reporting support data

---

# 20. Business/Product Positioning

The platform can be positioned as:

An automated Solana launch-trading control plane with real-time token discovery, multi-strategy scoring, risk gates, execution routing, paper/live trading modes, reconciliation, and operator-grade dashboards.

## Product Value

- Faster token discovery
- Better trade explainability
- Configurable strategy logic
- Safer execution control
- Paper/live testing support
- Multi-provider feed support
- Multi-route execution support
- Fee-aware PnL tracking
- Reconciliation-first accounting
- Operator dashboard visibility
- Trade journal and audit records
- Strategy extensibility
- ML-ready training data

---

# 21. Major Feature Inventory

## Feed Features

- PumpPortal WebSocket listener
- PumpPortal token trade subscription
- PumpPortal account trade subscription
- PumpPortal migration subscription
- PumpPortal new token subscription
- PumpSwap trade stream support
- Yellowstone feed support
- Geyser feed support
- Helius RPC support
- Helius Sender support
- Single WebSocket multiplexing
- Subscription tracking
- Feed heartbeat
- Event freshness tracking
- Reconnect logic
- Token state initialization

## Strategy Features

- ML graduation strategy
- Momentum ignition strategy
- Velocity compression breakout strategy
- Microscalper strategy
- Burn-centered strategy
- MiroFish-style swarm strategy
- VWAP reclaim strategy
- Intraday plugin strategy structure
- Heuristic scoring
- Weighted scoring
- Shadow scoring
- Paper scoring
- Strategy snapshotting
- Entry confidence scoring
- Exit pressure scoring

## Entry Features

- New token detection
- Token state creation
- Feature snapshot
- Entry scoring
- Entry gates
- Position sizing
- Execution route selection
- Buy intent creation
- Buy submission
- Buy confirmation
- Position creation
- Trade journal entry

## Exit Features

- Open position monitoring
- PnL calculation
- Fee-aware PnL calculation
- Take-profit exit
- Stop-loss exit
- Timed exit
- Green exit
- Trailing exit
- Whale sell exit
- Microstructure exit
- Catastrophic drop exit
- Curve-risk exit
- Graduation-risk exit
- Manual exit
- Emergency exit
- Sell intent creation
- Sell submission
- Sell confirmation
- Balance reconciliation
- Position close
- Trade journal update

## Gate Features

- Token age gate
- Liquidity gate
- Price gate
- Title/name gate
- Creator gate
- Burn gate
- Whale gate
- Holder concentration gate
- Quality gate
- Signal detector gate
- Runtime config gate
- Execution gate
- Live-mode gate
- Paper-mode gate
- Dry-run gate
- Fee gate
- Slippage gate
- Route gate
- Confirmation gate
- Reconciliation gate

## Execution Features

- PumpPortal Lightning execution
- PumpPortal local transaction execution
- Helius Sender execution
- Jito bundle execution
- Jupiter fallback execution
- Raydium route execution
- PumpSwap route execution
- Paper executor
- Dry-run executor
- Shadow executor
- Priority-fee support
- Jito-tip support
- Slippage support
- Signature handling
- Confirmation polling
- Reconciliation
- Execution reports

## Dashboard Features

- Mission Control
- Overview page
- Trades page
- Orders page
- Positions page
- Gate Truth page
- Audit page
- Trade Journal page
- Strategy Debugger
- Decision Debugger
- Execution Timeline
- Runtime Config page
- Health indicators
- Paper/live filters
- Shadow-mode view
- CSV export
- JSON export
- PnL display
- Fee display
- Gate decision display
- Strategy score display

## Storage Features

- SQLite persistence
- Pump event storage
- Trade storage
- Position storage
- Runtime config storage
- Decision ledger
- Intent ledger
- Gate receipt storage
- Execution report storage
- Pending sell storage
- Sell reconciliation storage
- Trade journal storage
- Training sample storage
- Strategy snapshot storage

---

# 22. Clean One-Paragraph Description

This platform is a Solana-based automated launch-trading control plane designed for pump.fun, BONK, PumpPortal, Yellowstone/Geyser, Helius, and related liquidity routes. It discovers new tokens in real time, builds market and wallet feature snapshots, scores opportunities through multiple strategies, applies configurable entry and exit gates, executes trades through supported execution rails, tracks positions, reconciles transaction results, records decision receipts, and gives operators a mission-control dashboard for paper, shadow, dry-run, and live trading modes.

---

# 23. 150-Character Description

Solana launch-trading control plane with real-time token discovery, strategy scoring, risk gates, execution routing, and dashboard visibility.

---

# 24. Description

A Solana-based launch-trading platform for pump.fun, BONK, PumpPortal, Yellowstone/Geyser, Helius, and related execution routes. It monitors new tokens in real time, scores opportunities using strategy logic and market features, applies configurable entry and exit gates, executes paper or live trades, reconciles results, tracks positions, records decision receipts, and gives operators a dashboard for strategy, risk, execution, and performance visibility.

---

# 25. Product-Style Feature Summary

The platform includes:

- Real-time token discovery
- Multi-provider Solana feed ingestion
- Pump.fun and BONK launch support
- PumpPortal WebSocket integration
- Yellowstone/Geyser support
- PumpSwap monitoring
- ML graduation scoring
- Momentum ignition strategy
- Velocity compression breakout strategy
- Microscalper strategy
- Burn-centered underwriting strategy
- MiroFish-style multi-agent scoring
- VWAP reclaim logic
- Entry gates
- Exit gates
- Fee-aware PnL
- Take-profit exits
- Stop-loss exits
- Timed exits
- Whale sell exits
- Microstructure exits
- Paper trading
- Shadow trading
- Dry-run mode
- Live trading mode
- PumpPortal execution
- Helius Sender execution
- Jito bundle support
- Jupiter/Raydium/PumpSwap route support
- Position tracking
- Trade reconciliation
- Trade journal
- Gate Truth audit system
- Decision receipts
- Runtime configuration
- Mission-control dashboard
- Strategy debugger
- Execution timeline
- CSV/JSON exports
- Secret-handling support
- Operator-grade auditability
