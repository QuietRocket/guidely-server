## Vast.AI Configuration
- Find a server with a decent CUDA capable graphics card (ie. RTX 3090+)
- Set docker image to `pytorch:latest`
    - Tested on `pytorch/pytorch:2.0.1-cuda11.7-cudnn8-runtime`
- Expose port via by adding `-p 1337:1337` to Docker options
- Either SSH into instance or use JupyerLabs

## Machine Configuration
- `apt install build-essential`
- Clone repository and change directory into repository
- Install dependencies: `pip install -r requirements.txt`
- Start the server: `uvicorn --host 0.0.0.0 --port 1337 server:app`
    - Note: First time running will be slower since you need to download the model
- Copy Vast.ai instance IP and port corresponding to 1337