### Environment Setup
1. Install Rust from https://rustup.rs/
2. Install Solana from https://docs.solana.com/cli/install-solana-cli-tools#use-solanas-install-tool

### Build and test for program compiled natively
```
$ cargo build
$ cargo test
```

### Build and test the program compiled for BPF
```
$ cargo build-bpf
$ cargo test-bpf
```


### Deploying your program on localnet

 - First, use the cargo build-bpf command to compile your program to a file with the so file extension.
 - Run solana-keygen new to create and save a solana keypair locally. 

 ```bash
solana-test-validator
 ```

 - Then, use the solana deploy command to deploy the program to localnet. The path to the program will have been printed by cargo build-bpf

 ```bash
solana program deploy <PATH_TO_YOUR_PROGRAM>
 ```

 - The deploy command should print the program id which you can now paste into the UI above