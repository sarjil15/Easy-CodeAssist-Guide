<h2>🌟 Overview</h2>

- **A clean and simple guide to install, configure, and run CodeAssist on both PC and Cloud VPS. Written for beginners and experts — no steps skipped.**

- **CodeAssist is a local-training coding assistant by Gensyn.
  It builds and trains a coding model on your machine using Docker, Python, UV, and HuggingFace.**

- **This guide shows how to run it smoothly on**

 ✔️ **Local PC**

 ✔️ **VPS (Ubuntu 22 / 24 / 25)**

 ✔️ **With or without RL-Swarm running**

 ✔️ **With working login via tunneling on VPS**

 <h1 align="center"><b>💻 Easy CodeAssist Guide (Local PC & VPS) 💻 </b></h1>


 <p align="center">
  <img 
    src="https://github.com/sarjil15/Easy-CodeAssist-Guide/blob/ef70c8fbc15510c7f444d590b677a162c925c483/assets/Screenshot%202025-11-30%20201256.png"
    width="90%"
    style="border: 3px solid #444; border-radius: 12px;"
  /> 
</p>
<hr>
 
<h2> Requirements🖥</h2>

- 12 GB RAM minimum (32 GB recommended)

- Stable internet connection

- At least 20 GB of available storage<br>

- Create a HuggingFace token

- Go here: https://huggingface.co/settings/tokens

✔️ Click Create new access token

✔️ Choose Write permissions

✔️ Save your token in notes <br>

# Run CodeAssist on Local PC
✅ 1. Install Docker Desktop
👉 https://docs.docker.com/get-started/<br>

✅ 2. Install CodeAssist dependencies in WSL
```
git clone https://github.com/gensyn-ai/codeassist.git
```
```
cd codeassist
```
```
curl -LsSf https://astral.sh/uv/install.sh | sh
source ~/.bashrc
```
✅ 4. Start CodeAssist
```
uv run run.py
```

During install:

- It will take a while to download Dependencies and Docker images

- And When It will ask for HuggingFace token → paste your access token → press Enter
(You will not see the token when pasting — that is normal.)

- After some time you will see:
```
A browser should have opened to http://localhost:3000
```
- Now Open this in browser👉 http://localhost:3000

- You’re ready to code.
<hr>

<h1 align="center"><b>☁️ Run CodeAssist on VPS ☁️</b></h1>

✅ 1. Install Docker (Ubuntu VPS)
```
sudo install -m 0755 -d /etc/apt/keyrings && \
sudo apt-get update && sudo apt-get install -y ca-certificates curl && \
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo tee /etc/apt/keyrings/docker.asc >/dev/null && \
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo ${UBUNTU_CODENAME:-$VERSION_CODENAME}) stable" | sudo tee /etc/apt/sources.list.d/docker.list >/dev/null && \
sudo apt-get update && \
sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
✅ 2. Clone CodeAssist
```
git clone https://github.com/gensyn-ai/codeassist.git
```
```
cd codeassist
```
✅ 3. Install UV
```
curl -LsSf https://astral.sh/uv/install.sh | sh
```
```
source ~/.bashrc
```
✅ 4. Start CodeAssist
```
uv run run.py
```




