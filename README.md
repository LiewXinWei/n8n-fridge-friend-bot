# n8n-fridge-friend-bot

Telegram bot workflow built with n8n that detects ingredients from food photos using Gemini and suggests matching recipes using Spoonacular.

## Overview
This workflow lets users send a food photo through Telegram. It analyzes the image with Gemini, extracts visible ingredients, searches for recipes using Spoonacular, and sends recipe suggestions with steps back to the user on Telegram.

## Features
- Accepts food photo uploads from Telegram
- Detects visible ingredients from the image using Gemini
- Cleans and processes detected ingredient names
- Searches Spoonacular for matching recipes
- Prioritizes recipes that use more of the detected ingredients
- Fetches recipe instructions for multiple recipe results
- Sends ingredient list, recipe suggestions, and steps back to Telegram

## Workflow Process
1. User sends a food photo in Telegram
2. Bot detects whether the message contains an image
3. Telegram file is retrieved
4. Gemini analyzes the image and identifies visible ingredients
5. Ingredients are cleaned, deduplicated, and formatted
6. Bot sends the detected ingredients back to the user
7. Spoonacular is queried for recipe matches
8. Matching recipes are ranked and prepared
9. Recipe instructions are fetched
10. Final recipe messages are formatted and sent to Telegram

## Requirements
- n8n
- Telegram Bot credentials
- Google Gemini API credentials
- Spoonacular API key

## Setup
1. Clone or download this repository
2. Import the workflow JSON file into n8n
3. Reconnect your Telegram and Gemini credentials
4. Add your own Spoonacular API key
5. Test the workflow with a Telegram photo
6. Activate the workflow

## Files
- `fridge-friend-workflow.json` — main n8n workflow export
- `README.md` — project documentation

## Notes
- This repository contains a cleaned workflow export
- Secrets, credential IDs, webhook IDs, and private values should be removed before uploading to GitHub
- Replace all placeholder credentials with your own before running the workflow
- Sample pinned data should also be removed if it contains personal or test information

## Example Use Case
A user sends a photo of ingredients such as eggs, mushrooms, and corn. The bot detects the ingredients, searches for recipes that match them, and replies with recipe ideas and cooking steps.

## Future Improvements
- Add support for text-based ingredient input
- Improve ingredient matching accuracy
- Add fallback recipe formatting for missing instructions
- Support more recipe filtering options such as vegetarian or low-calorie
