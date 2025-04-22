# Ollama Docker Compose 

[Ollama](https://ollama.com/) is an open-source software platform that enables users to run large language models (LLMs) locally on their computers. 

### Run Ollama

```
docker-compose -p ollama up -d 
```

### View the logs 

```
docker logs -f ollama
```

### Set up an alias for the ollama command

```
alias ollama="docker exec -it ollama ollama"
```

### Add the command to your rc file to run the ollama command in other terminal sessions. 

1. Run the command below;

```
vim ~/.bashrc
```

2. Append the lines below to the bottom of the file 

```
# Ollama Alias
alias ollama="docker exec -it ollama ollama"
```

3. Save and exit, then run this command; `source ~/.bashrc`

### Test Ollama Alias

```
ollama -v
```

### Install a model 

```
ollama run llama3.2
```

## Model library

Ollama supports a list of models available on [ollama.com/library](https://ollama.com/library 'ollama model library')

Here are some example models that can be downloaded:

| Model              | Parameters | Size  | Download                         |
| ------------------ | ---------- | ----- | -------------------------------- |
| Gemma 3            | 1B         | 815MB | `ollama run gemma3:1b`           |
| Gemma 3            | 4B         | 3.3GB | `ollama run gemma3`              |
| DeepSeek-R1        | 7B         | 4.7GB | `ollama run deepseek-r1`         |
| Llama 3.2          | 3B         | 2.0GB | `ollama run llama3.2`            |
| Llama 3.2          | 1B         | 1.3GB | `ollama run llama3.2:1b`         |
| Llama 3.1          | 8B         | 4.7GB | `ollama run llama3.1`            |
| Phi 4 Mini         | 3.8B       | 2.5GB | `ollama run phi4-mini`           |
| Mistral            | 7B         | 4.1GB | `ollama run mistral`             |
| Moondream 2        | 1.4B       | 829MB | `ollama run moondream`           |
| Neural Chat        | 7B         | 4.1GB | `ollama run neural-chat`         |
| Starling           | 7B         | 4.1GB | `ollama run starling-lm`         |
| Code Llama         | 7B         | 3.8GB | `ollama run codellama`           |
| Llama 2 Uncensored | 7B         | 3.8GB | `ollama run llama2-uncensored`   |
| LLaVA              | 7B         | 4.5GB | `ollama run llava`               |
| Granite-3.2        | 8B         | 4.9GB | `ollama run granite3.2`          |
