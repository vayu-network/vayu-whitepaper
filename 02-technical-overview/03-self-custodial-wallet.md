# Self-Custodial Wallet

When a user sets up their account in the Vayu app and agrees to the terms and conditions, a secure, self-custodial wallet is automatically created for them. This process is powered by the Particle Network's wallet abstraction solution.

Crucially, the wallet's seed phrase is generated and stored exclusively on the user's device; it is never transmitted and never accessible by Vayu.network. This gives the user full and sole control over their assets.

This wallet is used to manage the user's `$VAYU` token balance and to provide Web3-based consent (powered by the peaq network) for data contributions from their paired Flux device. This ensures that all data sharing is explicitly authorized by the user in a verifiable, on-chain manner.

<!-- TODO: add update details about app tech stack -->
To ensure the best performance and security, both the iOS and Android versions of the Vayu mobile app are developed natively, using Swift for iOS and Kotlin for Android, respectively. 