# Local-LLM (Linux Environment)
This is a introduction page for downloading ollama and webui (the interactive interface) locally.

## steps

### Step 1. Download Ollama in your local machine. 
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### step 2. to ensure ollama is installed, you can run it locally
```bash
ollama run llama 3
```

### Note: 
If you run into issues with step 1 or step2, check the [ollama](https://github.com/ollama/ollama) github link to debug!

This step ensures that your laptop actually installed  ollama.

### step3. Install the front end in your machine with one docker command. 
```bash
docker run -d --network=host -v open-webui:/app/backend/data -e OLLAMA_BASE_URL=http://127.0.0.1:11434 --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```

### Step 4. Open the webui for the user interface (before running this please make sure that 8080 port is not run by other apps). 
The default URL is http://localhost:8080/

### Note:
if you run into issues of using webui, check the offical github [here](https://github.com/open-webui/open-webui)


This is just an example of how you can download the LLM locally, there are many more ways to do it, and congrats! now you have your local LLM installed in your local machine and start to chat with it!
