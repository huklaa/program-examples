# PDA Rent-Payer

This examples demonstrates how to use a PDA to pay the rent for the creation of a new account.

The key here is accounts on Solana are automatically created under ownership of the System Program when you transfer lamports to them. So, you can just transfer lamports from your PDA to the new account's public key!

## Security note

This example intentionally focuses on how a PDA can pay rent and does not restrict who may request an account creation. The shared `rent_vault` PDA can therefore be spent by any caller that satisfies the example's account requirements.

Do not copy this authorization model into a production rent-payer. Add an explicit authorization policy, such as an admin recorded in program state, seeds that bind the vault to an authorized funder, or another application-specific limit. A standalone `Signer` account is not sufficient because any caller can sign with a keypair they control.

See [`basics/checking-accounts`](../checking-accounts/) for examples of validating account relationships and signers.
