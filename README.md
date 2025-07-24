# Real-time camera demo for LLM services

This is a demo for real-time object detection using the SmolVLM-Instruct vision model.  The app is single HTML webpage that runs on your local computer, gets an image from your webcam, and processes the image on a remote LLM endpoint -- in this case, PACE's LiteLLM service.  You don't need to install anything on your local computer -- you just need a web browser.  

This is a (very minor) modification of an [app](https://github.com/ngxson/smolvlm-realtime-webcam) by [Xuan-Son Nguyen](https://ngxson.com/).  At time of writing, he's a software engineer at Hugging Face.  If you like his app, [buy him a coffee!](https://buymeacoffee.com/ngxson)

## How to run

1. Claim your PACE LiteLLM account and generate an API key.  See [this guide.](https://github.gatech.edu/PACE/litellm-workflows/blob/main/01_claim_account_generate_key.ipynb)
2. Open [index.html](./index.html) in your web browser.  
3. Fill out these fields on the webform
   * Base API: http://litellm-dev.pace.gatech.edu:4000
   * API Key: The key you generated in Step 1
4. Click start!

## How it works

Xuan-Son's program is an excellent example of how simple API-driven LLM programming can be.  The entire program is less than 300 lines of HTML.  The inference request is done in the function `sendChatCompletionRequest`, which uses the OpenAI API to make a request.  It easily supports any OpenAI API endpoint: his original version used a local llama.cpp endpoint, and our version can use PACE's LiteLLM endpoint.  


![demo](./demo.png)