# n8n-fridge-friend-bot

Telegram bot workflow built with n8n that detects ingredients from food photos using Gemini and suggests recipes with Spoonacular.

## Features
- Accepts food photo uploads from Telegram
- Detects visible ingredients using Gemini
- Finds recipes using Spoonacular
- Returns recipe suggestions and steps to Telegram

## Requirements
- n8n
- Telegram Bot credentials
- Google Gemini API credentials
- Spoonacular API key

## Setup
1. Download or clone this repository
2. Import `fridge-friend-workflow.json` into n8n
3. Reconnect your credentials in n8n
4. Add your own Spoonacular API key
5. Activate the workflow

## Notes
- This repository contains a cleaned workflow export
- Secrets, credential IDs, webhook IDs, and sample pinned data were removed before upload
