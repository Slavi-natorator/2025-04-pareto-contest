# Pareto USP, a credit-backed synthetic dollar contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the **Issues** page in your private contest repo (label issues as **Medium** or **High**)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Q&A

### Q: On what chains are the smart contracts going to be deployed?
Ethereum
___

### Q: If you are integrating tokens, are you allowing only whitelisted tokens to work with the codebase or any complying with the standard? Are they assumed to have certain properties, e.g. be non-reentrant? Are there any types of [weird tokens](https://github.com/d-xo/weird-erc20) you want to integrate?
No wierd tokens. Collaterals tokens will only be "big" ERC20 stablecoins, USDC, USDT, USDS, DAI, potentially USDe
___

### Q: Are there any limitations on values set by admins (or other roles) in the codebase, including restrictions on array lengths?
Owner/Pauser is trusted.
Manager role for the queue contract is trusted too but in general he should not be able to run with the money as functions that he can call and parameters are restricted
___

### Q: Are there any limitations on values set by admins (or other roles) in protocols you integrate with, including restrictions on array lengths?
No
___

### Q: Is the codebase expected to comply with any specific EIPs?
ParetoDollarStaking.sol should ERC4626 compliant so that it can be easily integrated in other Defi protocols
___

### Q: Are there any off-chain mechanisms involved in the protocol (e.g., keeper bots, arbitrage bots, etc.)? We assume these mechanisms will not misbehave, delay, or go offline unless otherwise specified.
No
___

### Q: What properties/invariants do you want to hold even if breaking them has a low/unknown impact?
No
___

### Q: Please discuss any design choices you made.
Nothing special I would, some 'issues' have been marked as acknowledged in prev audits that we did so this issues should not be reported as long as there are no new findings around those
___

### Q: Please provide links to previous audits (if any).
- https://github.com/sherlock-audit/2025-04-pareto-contest/blob/main/USP/_attachements/Pareto-Security-Review.pdf
- https://github.com/sherlock-audit/2025-04-pareto-contest/blob/main/USP/_attachements/USP_Review.pdf
___

### Q: Please list any relevant protocol resources.
Further documentation can be found at: https://github.com/sherlock-audit/2025-04-pareto-contest/blob/main/USP/_attachements/doc.md
___

### Q: Additional audit information.
Main area of focus should be eventual loss of funds for the users, locked/unrecoverable funds, serious misbehaviour of the protocol.

Additional information for Pareto Credit vaults used as yield sources for USP can be found here https://docs.pareto.credit/product/credit-vaults


# Audit scope

[USP @ ea295f0a712ac23eb02308f05d8891850db938af](https://github.com/pareto-credit/USP/tree/ea295f0a712ac23eb02308f05d8891850db938af)
- [USP/src/Constants.sol](USP/src/Constants.sol)
- [USP/src/EmergencyUtils.sol](USP/src/EmergencyUtils.sol)
- [USP/src/ParetoDollar.sol](USP/src/ParetoDollar.sol)
- [USP/src/ParetoDollarQueue.sol](USP/src/ParetoDollarQueue.sol)
- [USP/src/ParetoDollarStaking.sol](USP/src/ParetoDollarStaking.sol)
- [USP/src/interfaces/IParetoDollar.sol](USP/src/interfaces/IParetoDollar.sol)
- [USP/src/interfaces/IParetoDollarQueue.sol](USP/src/interfaces/IParetoDollarQueue.sol)
- [USP/src/interfaces/IParetoDollarStaking.sol](USP/src/interfaces/IParetoDollarStaking.sol)


