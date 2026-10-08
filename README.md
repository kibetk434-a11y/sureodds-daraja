# SureOdds Daraja Sandbox Starter

A realistic sportsbook-style frontend plus Node/Express backend prepared for Safaricom Daraja sandbox M-Pesa Express (STK Push).

## Important
- This project is a sandbox/testing starter. It does NOT contain real Daraja credentials.
- Never put Consumer Secret, Passkey, database passwords, or M-Pesa PINs in frontend code.
- For production real-money betting, use the required Kenyan gambling licence and approved Safaricom business payment setup.

## Structure
- frontend/ — responsive sportsbook UI
- backend/ — Express API and Daraja integration
- backend/.env.example — configuration template

## Main flow
Deposit -> backend /api/payments/stkpush -> Daraja -> callback -> verified transaction -> wallet ledger.

The wallet is credited only from a successful callback, not merely when an STK request is created.

## Run locally
1. Backend:
   cd backend
   npm install
   copy .env.example to .env
   npm start

2. Frontend:
   cd frontend
   npm install
   npm run dev

The frontend uses http://localhost:5173 and backend http://localhost:5000 by default.

## Daraja setup
Create a sandbox app on the official Daraja portal, obtain sandbox consumer credentials, and configure the sandbox shortcode/passkey supplied by Daraja.

Official portal: https://developer.safaricom.co.ke/
