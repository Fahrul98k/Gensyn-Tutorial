
## Step by Step 
### Setup GPU 
1. You can use the rented GPU as you wish. In this guide, i use a Hyperbolic GPU. To set up and connect your GPU to the terminal, you can use the Hyperbolic GPU. For setup instructions, you can go here [1](https://x.com/Zun2025/status/1898037872932143591). 

>[!NOTE] 
>You can choose the PyTorch instance, dont choose the NVIDIA one. I previously used NVIDIA and got error  
>
>![[Pasted image 20250427113035.png]]]

### Setup and Run Node 
1.  Install `sudo` 
	```javascript
	apt update && apt install -y sudo
```

2. Install dependencies 
	```javascript
	sudo apt update && sudo apt install -y python3 python3-venv python3-pip curl wget screen git lsof nano unzip iproute2
```

3. Install Node.js and NPM
``` javascript
curl -sSL https://raw.githubusercontent.com/zunxbt/installation/main/node.sh | bash
```
4. Create a `screen` session 
```javascript 
screen -S gensyn
```
5. Run the swarm 
```javascript
cd $HOME && rm -rf gensyn-testnet && git clone https://github.com/zunxbt/gensyn-testnet.git && chmod +x gensyn-testnet/gensyn.sh && ./gensyn-testnet/gensyn.sh
```
- it will ask some question, write `N` 

## Useful command 

### Send Swarm file From local to Server 
```javascript
ssh -i "yourlocalfileberada" -p yourport instanceid

```
### Send Swarm file from server to local
>[!NOTE]
>if u use Termius or Vast AI there is a feature that allows you to download it manually 