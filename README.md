# n8n-fridge-friend-bot

Telegram bot workflow built with n8n that detects ingredients from food photos using Gemini and suggests matching recipes using Spoonacular.

## Overview
This project allows users to send a food photo through Telegram and receive recipe suggestions based on the visible ingredients in the image. The workflow uses Gemini to analyze the uploaded photo, extract ingredient names, and then uses Spoonacular to search for recipes that best match those ingredients. The bot finally returns recipe suggestions and cooking steps directly in Telegram.

## Features
- Accepts food photo uploads from Telegram
- Detects visible ingredients using Gemini
- Cleans, formats, and deduplicates detected ingredients
- Searches Spoonacular for recipe matches
- Prioritizes recipes that use more of the detected ingredients
- Fetches recipe instructions for multiple recipe results
- Sends ingredient summaries, recipe suggestions, and cooking steps back to Telegram

## Workflow Process
1. User sends a food photo in Telegram
2. The bot checks whether the message contains an image
3. Telegram retrieves the uploaded file
4. Gemini analyzes the image and identifies visible ingredients
5. Ingredient names are cleaned and processed
6. The detected ingredient list is sent back to the user
7. Spoonacular is queried for matching recipes
8. Recipes are ranked based on ingredient usage
9. Recipe steps are retrieved
10. Final formatted recipe suggestions are sent back to Telegram

## Demo
Watch the project demo below.
https://github.com/user-attachments/assets/6a134f7d-555e-41dd-8feb-af31ba532f1e

## Preview
You can add screenshots below to show the bot flow, such as:
- Telegram bot receiving a food photo
- Detected ingredients message
- Recipe suggestions and cooking steps
- n8n workflow overview

## Requirements
- n8n
- Telegram Bot credentials
- Google Gemini API credentials
- Spoonacular API key

## Setup
1. Clone or download this repository
2. Import the workflow JSON file into n8n
3. Reconnect your Telegram credentials in n8n
4. Reconnect your Google Gemini credentials in n8n
5. Add your own Spoonacular API key
6. Test the workflow using a Telegram food photo
7. Activate the workflow

## Files
- `fridge-friend-workflow.json` — main n8n workflow export
- `README.md` — project documentation

## Notes
- This repository contains a cleaned workflow export
- Secrets, credential IDs, webhook IDs, and private values should be removed before uploading to GitHub
- Replace all placeholder credentials with your own before running the workflow
- Remove pinned sample data if it contains personal, test, or sensitive information

## Example Use Case
A user sends a photo of ingredients such as eggs, mushrooms, and corn. The bot detects the visible ingredients, searches for matching recipes, and replies with recipe suggestions together with cooking steps.

## Future Improvements
- Add support for text-based ingredient input
- Improve ingredient detection accuracy
- Improve recipe matching logic
- Add fallback handling when recipe steps are unavailable
- Support more recipe filters such as vegetarian, high-protein, or low-calorie


