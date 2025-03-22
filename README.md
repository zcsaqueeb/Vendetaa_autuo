
# Vendetta Auto Bot

**Referral Link:** [Vendetta Game](https://vendettagame.xyz/quest?refercode=Z20dIPluUM6v)  
Join the Vendetta game using this link and earn rewards while completing quests!

## Overview
An automation bot designed to enhance your experience in the Vendetta game. Automatically complete quests, earn points, and climb the leaderboard with ease. Supports various proxy types, ensuring seamless performance.

## Features
- Effortlessly complete all available quests:
  - Regular quests
  - Riddle quests with pre-filled answers
  - Series quests with pre-filled answers
- Manage multiple wallets in a single session
- Proxy compatibility (HTTP, HTTPS, SOCKS4, SOCKS5)
- Detailed logs for tracking progress
- Monitor wallet profile updates with points and leaderboard rank

## Requirements
- Node.js (v16+ recommended)
- NPM or Yarn

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/airdropinsiders/Vendetta-Auto-Bot.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Vendetta-Auto-Bot
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Add your wallet addresses to a `.env` file:
   ```plaintext
   WALLETS=["0xWALLETADDRESS1","0xWALLETADDRESS2"]
   ```
5. (Optional) Set up a `proxies.txt` file for proxy usage:
   ```plaintext
   http://username:password@host:port
   socks5://username:password@host:port
   host:port
   host:port:username:password
   ```

## Proxy Support
Compatible formats include:
- `protocol://username:password@host:port`
- `host:port` or `host:port:username:password`
  
Supported protocols:
- HTTP
- HTTPS
- SOCKS4
- SOCKS5

Default protocol: HTTP (if unspecified).

## Usage
Run the bot:
```bash
npm start
```

Workflow:
1. Load proxies from `proxies.txt` (if available)
2. Rotate proxies for each wallet (round-robin)
3. Retrieve initial profile information for each wallet
4. Complete all quests
5. Fetch updated profile information
6. Display quest completion summary with points earned

## Configuration
Customize the `QUESTS` array in `index.js` to:
- Add or remove specific quests
- Update riddle/series answers as needed

## Example Output
```plaintext
Vendetta Auto Task - Airdrop Insiders
-------------------------------------
Found 2 wallets in .env
Loaded 5 proxies from proxies.txt

[1/2] Processing wallet...

🔹 Wallet: BwXKxH5n8Rx6B...
🔹 Proxy: http://123.45.67.89:8080

Initial Profile Info:
✅ Total Points: 0
✅ Rank: 10245

Quests Completed:
✅ Quest: 67a0d816790b534bfa5e9c75

Updated Profile Info:
✅ Total Points: 675
✅ Rank: 3211
...
```

## Notes
- Operates via the Vendetta game API—changes may occur without notice.
- Exercise caution and adhere to the game's terms of service.
- Consider using proxies to minimize rate-limiting risks.

## License
MIT License

## Disclaimer
This tool is for educational purposes only. The authors are not responsible for misuse or consequences arising from its use.

