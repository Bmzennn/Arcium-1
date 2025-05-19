# Arcium
A simple guide to arcium. 
I'll be documenting my journey with arcium, Its more of a personal thing but feel free to tag along. I'll be documenting everything I do. For best practicies, I recommend you have a notepad file to store data you may need later on. (At least thats what I do) .

### INSTALLING REQUIREMENTS

You can easily install these on your terminal, skip if you already have them.

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
### -Solana CLI 

The Solana CLI provides all the tools required to build and deploy Solana programs.
```
sh -c "$(curl -sSfL https://release.anza.xyz/stable/install)"
```
close and reopen your terminal to apply changes 

If you are using a Linux or WSL terminal, you can add the PATH environment variable to your shell configuration file by running the command logged from the installation or by restarting your terminal.
```
export PATH="$HOME/.local/share/solana/install/active_release/bin:$PATH"
```
To verify that the installation was successful, check the Solana CLI version:
```
solana --version
```
You should see output similar to the following
<pre> solana-cli 2.0.26 (src:3dccb3e7; feat:607245837, client:Agave) </pre>

### -Anchor CLI
I installed anchor using AVM (Anchor Version Manager)
Install AVM with the following command:
```
cargo install --git https://github.com/coral-xyz/anchor avm --force
```
Check that AVM was installed successfully
```
avm --version
```
Installing the latest version of Anchor CLI 
```
avm install latest
avm use latest
```
check that the installation was successful
```
anchor --version
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

### -Creating and Setting-up Wallet

To generate a keypair at the default Keypair Path, run

```
solana-keygen new
```
you should see something like this (Remember that notepad I talked about earlier? save or your details there or wherever is safe)
<pre> 
 Generating a new keypair

For added security, enter a BIP39 passphrase

NOTE! This passphrase improves security of the recovery seed phrase NOT the
keypair file itself, which is stored as insecure plain text

BIP39 Passphrase (empty for none):

Wrote new keypair to /Users/test/.config/solana/id.json
===========================================================================
pubkey: _YourPubKey
===========================================================================
Save this seed phrase and your BIP39 passphrase to recover your new keypair:
_YourSeedPhrase
===========================================================================
</pre>
To view your generated wallet address,
 ```
 solana address
 ```

### Requesting for SOL 
First configure to solana devnet and then request an airdrop of devnet SOL
```
solana config set --url devnet
solana airdrop 2
```
Check your wallet balance 
```
solana balance
```
### Local Validator Node
The Solana CLI includes a built-in test validator for local development.

In a separate terminal, run the following command to start a local validator:
```
solana-test-validator
```

![image](https://github.com/user-attachments/assets/44dfc7c8-20af-47eb-952a-f9ae88338f64)

should look a little something like this if done correctly

The local Validator node is not needed at this stage so feel free to turn it off with ``` CTRL + C ``` . 


That'll be all for now. On Arcium-2 I'll go through ```arcup``` version manager Installation 













