# AI Customer Support Chatbot

A customer support chatbot for a business website, powered by Claude (Anthropic API) and hosted on Netlify.
The API key stays on the server inside a Netlify Function, so it is never exposed in the browser.

## Run locally
1. Install Node.js 18 or newer.
2. `npm install -g netlify-cli`
3. Copy `.env.example` to `.env` and add your `ANTHROPIC_API_KEY`.
4. `netlify dev`
5. Open http://localhost:8888

## Customize for a client
Edit `netlify/functions/knowledge.js` with the client's hours, prices, FAQs and policies.

## Deploy
Push to GitHub, import the repo in Netlify, and add `ANTHROPIC_API_KEY` under Site configuration, Environment variables.

## Files
- `index.html`: chat interface
- `netlify/functions/chat.js`: secure API call to Claude
- `netlify/functions/knowledge.js`: business knowledge base
