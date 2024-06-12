# Local-LLM (Linux Environment)
This is a introduction page for downloading ollama and webui (the interactive interface) locally.

## steps

### Step 1. Download Ollama in your local machine. 
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### step 2. to ensure ollama is running locally
```bash
ollama run llama 3
```

This step ensures that your laptop actually installed  ollama.

### step3. Install the front end in your machine with one docker command. 
```bash
docker run -d --network=host -v open-webui:/app/backend/data -e OLLAMA_BASE_URL=http://127.0.0.1:11434 --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```

### Step 4. Open the webui for the user interface. 
The default URL is http://localhost:8080/

Congrats, now you have your local LLM installed in your local machine and start to chat with it!
