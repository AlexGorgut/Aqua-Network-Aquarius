# Aqua Network: Aquarius Audit Findings Summary

This repository contains security audit findings for the Aqua Network Aquarius project, a DeFi liquidity protocol. The audit identified one vulnerability during the security assessment.

## Findings

### 1. LiquidityPoolRouter Parameter Order Vulnerability
**([Low](https://cantina.xyz/competitions/990ce947-05da-443e-b397-be38a65f0bff) Severity)**

Parameter order inconsistency between AdminInterface trait and its implementation in LiquidityPoolRouter causes pool creation fees to be swapped. This results in stable pools costing 90% less and standard pools costing 900% more than intended.

- **Impact**: Complete reversal of the protocol's economic model leading to revenue loss and user overpayment
- **Root Cause**: Mismatched parameter order between interface declaration and implementation in configure_init_pool_payment function

## Summary Statistics
- **Total Findings**: 1
- **High Severity Findings**: 0
- **Medium Severity Findings**: 0
- **Low Severity Findings**: 1