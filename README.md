# Running Llama 3 locally

With this brief guide, you'll be able to use LLMs even when flying! ✈️

In Mac or Windows, the `ollama` CLI must be installed through the [Ollama installable](https://ollama.com/download/) (instead of using the `curl -fsSL https://ollama.com/install.sh | sh` as in Linux). Then, you download the `MODEL` of your choice (_e.g_ `8b` or `70b`): 
```bash
ollama pull llama3:$MODEL
```
And the OpenWebUI's container can be launched running:
```bash
docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```