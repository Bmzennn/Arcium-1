# Arcium-1
A simple guide to arcium. 
I'll be documenting my journey with arcium, Its more of a personal thing but feel free to tag along. I'll be documenting everything I do. For best practicies, I recommend you have a notepad file to store data you may need later on. (At least thats what I do) .

### INSTALLING REQUIREMENTS

You can easily install these on your terminal 

### -Rust
 ```
 curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
you should receive a ```Welcome to Rust``` message, continue to ```proceed with standard installation```

To verify the installation succeeded, check the Rust version:
```
rustc --version
```
You should see the output like the following 
<pre> rustc 1.86.0 (05f9846f8 2025-03-31) </pre>

### -NPM 

You can either get this from the official node.js website ```https://nodejs.org``` or Install it directly from your terminal using ```nvm``` 
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

```
Reload terminal
```
source ~/.bashrc
```
Install Node.js (which includes npm):
```
nvm install --lts
```
If succesful, should receive ```Now using node v22.15.1 (npm v10.9.2)```


### -Yarn
```
npm install -g corepack
yarn set version stable
yarn install
```



### -Solana

You'll need to install Solana and then run ```solana-keygen``` new to create a keypair at the default location. Arcium uses this keypair to run your program tests.

```
curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash
```

After installation, you should see output like the following:

<pre>Installed Versions:
Rust: rustc 1.86.0 (05f9846f8 2025-03-31)
Solana CLI: solana-cli 2.2.12 (src:0315eb6a; feat:1522022101, client:Agave)
Anchor CLI: anchor-cli 0.31.1
Node.js: v23.11.0
Yarn: 1.22.1 </pre>








