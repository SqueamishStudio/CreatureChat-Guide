# Installing CreatureChat using Ollama


## Step 1: Install Ollama

1. Visit the Ollama website [Ollama Website](https://ollama.com)
2. Follow the installation instructions for **Windows**, **macOS**, or **Linux**.


## Step 2: Open Command Prompt or Terminal

- **Windows**: Run **Command Prompt** or **PowerShell** as administrator.
- **macOS/Linux**: Open the **Terminal** application.


## Step 3: Pull Ollama Model
In the terminal, type the following command to download the Qwen2 model:

```bash
ollama pull qwen2
```
In this example it is pulling the qwen2 model but you can use any model you like. Some examples of other models are:

**Llama3:** The most popular model on Ollama, it requires a powerful computer but has good results.
```bash
ollama pull llama3
```
**TinyLama:** From my testing TinyLlama ran the fastest but unfortunately gave bad results.
```bash
ollama pull tinyllama
```
**Mistral:** This model runs slower than TinyLlama but offers good results.
```bash
ollama pull mistral
```
If you want to install other models you can find them here: [ollama library](https://ollama.com/library)


## Step 4: Run Ollama Model
Next you will need to run the model. This can be done by running the following in the terminal.
```bash
ollama run [model name]
```
For example using Qwen2, write.
```bash
ollama run qwen2
```
This step is where you are most likely to pickup errors. If you get past this you have completed the hardest part.


## Step 5: CreatureChat Setup

1. Launch Fabric (or Forge) Minecraft with the CreatureChat mod installed. For those on low-end devices I also recommend installing *Sodium*, *Lithium*, and other performance mods to free up your devices resources for running the model.
2. Next create a new Minecraft world and write in the following:
```bash
/creaturechat url set "http://localhost:11434/v1/chat/completions"
```
This tells CreatureChat which port to lissend commands to, it may vary depending on the way your ports are setup.
```bash
/creaturechat model set [model name]
```
Insert the name of the model you just installed. For example:
```bash
/creaturechat model set qwen2
```
Lastestly set the timeout to 0.
```bash
/creaturechat timeout set 0
```


## Step 6: Stopping Ollama Model and Uninstalling

Stopping the model is very simple. Close the terminal or go CTRL + C inside the terminal.

Uninstalling the model is also a easy task. If you have decided you want to use another model or don't need it anymore just type.
```bash
ollama rm [model name]
```
For example using qwen2 type:
```bash
Ollama rm qwen2
```

## Conclusion

That's it! You should be able to talk to any mob and get them to reply. It may take between 1 to 5 minutes depending on your computers hardware. If you run into any error feel free to create an issue on the [repo](https://github.com/SqueamishStudio/CreatureChat-Guide/issues) and I will try my best to help out when I have time.

Good luck running a Local LLMs!

Ollie from Squeamish Studio