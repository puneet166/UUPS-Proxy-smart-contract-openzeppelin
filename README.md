# UUPS-Proxy-Smart-Contract-OpenZeppelin

This project demonstrates the use of UUPS (Universal Upgradeable Proxy Standard) proxies based on OpenZeppelin. The steps below guide you through deploying, testing, and upgrading a smart contract using UUPS proxies.

## Deployment and Usage

### Step 1: Deploy V1 Smart Contract with Proxy

1. **Deploy V1 Implementation with Proxy Smart Contracts:**
   - Deploy the implementation smart contract (V1).
   - Select Deploy with proxy.
   - These two transactions happen simultaneously one for proxy&mapping the imeplentation address with proxy and second for implementation .

### Step 2: Interact with the Proxy Smart Contract

1. **Read and Write Data:**
   - Use the proxy smart contract to read and write data.
   - The proxy smart contract will use the logic of the implementation smart contract (V1) and maintain its own state variables.
   - Do your testing properly and use the state variable and go to step 3.

### Step 3: Upgrade to V2 Smart Contract

1. **Modify the Contract:**
   - Add a new function and a new state variable in the V2 implementation smart contract.

### Step 4: Deploy V2 Smart Contract and Upgrade Proxy

1. **Deploy V2 Implementation and Upgrade Proxy:**
   - Deploy the V2 implementation smart contract.
   - Select "Upgrade with Proxy" to upgrade the proxy to use the V2 implementation and put the address of proxy address which is deployed step 1.
   - Again, two smart contracts will be involved:
     - The V2 implementation smart contract.
     - The same proxy smart contract will use for v2 implementation smart contract.

### Step 5: Interact with the Upgraded Proxy

1. **Read and Write Updated State Variables:**
   - Use the upgrade proxy smart contract to read and write state variables.
   - You will see the new functions and state variables in proxy smart contract.
   - Note that the proxy smart contract remains the same; only the implementation has been upgraded.

## Summary

By following these steps, you can successfully deploy, test, and upgrade a smart contract using the UUPS proxy pattern. The proxy contract remains consistent, while the implementation contract can be upgraded to introduce new functionalities and state variables.
