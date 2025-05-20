From henceforth, I'll be swithing to VSCode to make things easier for me. i

The Arcium tooling suite for writing MXEs (MPC eXecution Environments) is built on top of Anchor, so if you're familiar with Anchor, you should find Arcium to be a familiar experience, except that you're using the ```arcium``` CLI instead of ```anchor```

To initialize a new MXE project, you can therefore simply run:
```
arcium init <project-name>
```
would be naming my project `project-1` for the sake of this test
This will create a new project with the given name, and initialize it with a basic structure. 

By the way a basic anchor structure looks something like this
```
my_anchor_program/
├── programs/
│   └── my_anchor_program/
│       └── src/
│           └── lib.rs      <--- Your Solana program lives here
├── tests/
│   └── my_anchor_program.ts  <--- Test using JavaScript or TypeScript
├── Anchor.toml              <--- Config file (like package.json)
├── Cargo.toml               <--- Rust dependencies
```

The structure is the same as in an Anchor project with two differences,

- The `Arcium.toml` file, which contains the configuration for the Arcium tooling suite.

- The `encrypted-ixs` directory. This is where we write all our code that is meant to operate on encrypted data and therefore runs in MPC. This code is written using our own Rust framework called Arcis. 


