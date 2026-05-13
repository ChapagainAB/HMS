# HMS - Gemini Strategy Paper Tester

This project is a lightweight browser-based prototype to test and improve trading strategies with Gemini, then report results through Telegram.

## What it does

- Paper-tests strategy text on sample market data for:
  - `BTCUSDT`
  - `ETHUSDT`
  - `XAUUSD` (gold)
  - `XAGUSD` (silver)
- Calculates run metrics (accuracy, captured/missed opportunities, estimated PnL)
- Requests strategy improvements from Gemini API after each run
- Stores run logs in browser `localStorage`
- Sends run results + improvements through Telegram bot
- Pulls Telegram commands with format:
  - `/test BTCUSDT your strategy text here`

## Configure

1. Open `index.html` in a browser.
2. Add:
   - Gemini API Key
   - Gemini Model (default: `gemini-1.5-flash`)
   - Telegram Bot Token
   - Telegram Chat ID
3. Click **Save Settings**.

## Usage

1. Choose market and enter strategy.
2. Click **Run Paper Test**.
3. Review:
   - Latest metrics
   - Gemini improvement text
   - Stored logs
4. Click **Send Latest Result to Telegram** to notify your chat.
5. Click **Fetch /test From Telegram** to process the latest Telegram strategy command.

## Notes

- This is paper testing only; no real order execution is performed.
- API keys are stored locally in the browser for this prototype.
- Telegram Bot API tokens are used directly by client-side requests in this prototype, so use a dedicated bot token and rotate it regularly.
