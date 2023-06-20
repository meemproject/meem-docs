# React SDK

We've created some handy react-specific tools that make interacting with Meem contracts a breeze!

To deploy your first contract you can head over to [https://clubs.link](https://clubs.link). Once you've deployed your contract, you can build custom experiences interacting with it.

### Connect a Wallet (Metamask / WalletConnect)

This will pop up a modal asking the user to select MetaMask or WalletConnect

```tsx
import { useWallet } from '@meemproject/react'
import React from 'react'

export const ConnectWallet: React.FC = () => {
    const { connectWallet } = useWallet()
    
    return (
        <button onClick={() => connectWallet()}>Connect Wallet</button>
    )
}
```

![When connectWallet() is called](<../.gitbook/assets/Screen Shot 2022-05-26 at 4.14.23 PM.png>)

