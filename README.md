# RL Swarm Node Run Full Guide (PC and VPS and Mac)

### Offical Docs Guide - https://github.com/gensyn-ai/rl-swarm?tab=readme-ov-file

### Dashboard (check ur points) - https://dashboard.gensyn.ai/

1️⃣ Dependencies for WINDOWS & LINUX & Mac

For WSL
```
sudo apt update && sudo apt upgrade -y
```
```
sudo apt install -y curl git wget nano tmux htop nvme-cli lz4 jq make gcc clang build-essential autoconf automake pkg-config libssl-dev libleveldb-dev libgbm1 bsdmainutils ncdu unzip tar
```
For Mac
```
brew install git curl wget nano tmux htop jq make gcc autoconf automake pkg-config openssl leveldb lz4 coreutils
```

2️⃣ Install Python & Node Js & Yarn & NPM & Pip & Dev. tool

For WSL
```
sudo apt-get install python3 python3-pip python3-venv python3-dev -y
```
```
sudo apt-get update && curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash - && sudo apt-get install -y nodejs && node -v && npm -v && sudo npm install -g yarn && yarn -v
```
```
sudo apt install -y python3 && sudo apt install -y python3-pip && python3 --version && pip3 --version
```
```
sudo apt install python3-dev python3-venv build-essential -y
```
```
sudo apt-get update && sudo apt-get install -y curl gnupg apt-transport-https && curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add - && echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list && sudo apt-get update && sudo apt-get install -y yarn && yarn --version
```
For Mac
```
brew install python3 node yarn
```

3️⃣ Hugging Face Access Token (Optional)

- Not Needed

4️⃣ Download Some Files
```
git clone https://github.com/gensyn-ai/rl-swarm/
cd rl-swarm
```

5️⃣ Install and Run RL Swarm
```
python3 -m venv .venv
source .venv/bin/activate
./run_rl_swarm.sh
```
Put answer 'Y' (just press enter)

Wait till you see waiting for UserData.json to be created

Then open Browser and Input & Login by Google - http://localhost:3000/

![1_qkd1ND0PxngzkxE4Z6VqBQ](https://github.com/user-attachments/assets/19ceac2c-b3ff-47d6-8a7c-f4f584288241)

Now It will promt Would you like to push models you train in the RL swarm to the Hugging Face Hub? [y/N] Enter N

![1_zs7VHm5Fv_ZeFTsZdBGo9g](https://github.com/user-attachments/assets/123acf42-08bc-492b-aa13-d27359af9ce3)

![429398341-3ac0514c-a7cc-4743-8389-f3246d5888a0](https://github.com/user-attachments/assets/7a1bb7ff-f77e-45bd-b3a2-f46139d35f3f)

Take note of Username


## Open Another Window for WSL to save ur Swarm File

1️⃣ Save your `swarm.pem` file to your Desktop screen on your PC from WSL (Open WSL)
- username has no spaces
```
cp ~/rl-swarm/swarm.pem /mnt/c/Users/YourUsername/Desktop/
```
- username has spaces
```
cp ~/rl-swarm/swarm.pem "/mnt/c/Users/Your Username/Desktop/"
```
Replace YourUsername or Your Username with your actual Windows username

3️⃣ To check your Windows username
- Through Command Prompt or Powershell
```
echo %USERNAME%
```

4️⃣ Save your `swarm.pem` file to your Desktop screen on your Mac from HomeBrew
```
cp ~/rl-swarm/swarm.pem ~/Desktop/
```

## 🔶For Next Day Run This Command (Windows or Mac)

#1 Open WSL or HomeBrew and Put this Command 
```
cd rl-swarm
```
```
python3 -m venv .venv
source .venv/bin/activate
./run_rl_swarm.sh
```

## Delete Node File
```
rm -rf ~/rl-swarm
```

## Backup your Key
```
cat ~/rl-swarm/modal-login/temp-data/userApiKey.json
```
```
cat ~/rl-swarm/modal-login/temp-data/userData.json
```
