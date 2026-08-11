# PDA Rent-Payer

This examples demonstrates how to use a PDA to pay the rent for the creation of a new account.

The key here is accounts on Solana are automatically created under ownership of the System Program when you transfer lamports to them. So, you can just transfer lamports from your PDA to the new account's public key!

> [!IMPORTANT]
> This example intentionally focuses on PDA signing and does not restrict who may ask the shared rent vault to fund a new account. Production programs should add authorization or scope the vault to the intended funder/caller; requiring only the newly created account to sign does not protect a shared vault.
