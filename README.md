# Solidity Troubleshooting Guide

**A quick guide for both beginner and novice developers- because blockchain is hard.**

### First steps (start here)

Ordered most-to-least common.

1.  Are you on the right network?
2.  Are you on the right account?
3.  Are you trying to access the right contract?
4.  Are you the owner of the contract?
5.  Do you have ETH in your account?
6.  Are you using the correct ABI for this contract?
7.  Are the permissions and requirements for the contract met?
8.  Are you formatting the arguments correctly?
9.  Is the method payable? Does it require payment? [Read more](https://solidity.readthedocs.io/en/develop/miscellaneous.html?highlight=pure#modifiers)

> When in doubt, [read the Solidity docs](https://solidity.readthedocs.io/en/v0.4.24/index.html)!

### Common Error Messages

| Issue                     | Details                                                                                                   | Solution                                                                                                                    |
| ------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Gas estimation failed     | The transaction execution will likely fail. Do you want to force sending?                                 | Check your permission for the transaction. Check that the require statements are satisfied.                                 |
| Error encoding arguments  | Error: types/values length mismatch.                                                                      | Use quotes "" for strings and addresses                                                                                     |
| Invalid JSON RPC response | You likely do not have permission to access this method, or the 'require' statements are being satisfied. | Solution: Check that the contract owner and your account match. Check that the conditions of the transaction are satisfied. |

### Other Errors

Importing from another contract? If it's a local file, check that it's saved in remix. If importing a contract from a Github URL, and you're at a hackathon or workshop, Github may be blocking your IP to prevent a DDOS scenario. In this case, you should save a copy of contract locally instead. The Giuthub contract may change without notice, so this is good practice.

If all else fails, you can use the [debugger in Remix](https://remix.readthedocs.io/en/latest/tutorial_debug.html)

### Using Remix locally

As you transition to develop your DApp frontend, don't feel like you need to leave Remix behind. Consider using [RemixD](https://remix.readthedocs.io/en/latest/tutorial_remixd_filesystem.html) to access local files on your PC within Remix.

### Additional resources

**Security**

- [Smart contract best practices](https://consensys.github.io/smart-contract-best-practices/) from ConsenSys
- [Latest Security Considerations](https://solidity.readthedocs.io/en/latest/security-considerations.html)
- Another curated resource: [Awesome Ethereum Security](https://github.com/trailofbits/awesome-ethereum-security#learning)

### Contribute

Open to contributions!

Questions? Contact [Patrick](https://twitter.com/pi0neerpat)
