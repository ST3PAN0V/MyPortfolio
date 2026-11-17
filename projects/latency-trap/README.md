# Latency Trap

### Marketplace price-validation retrospective

**Context:** Historical marketplace incident  
**Focus:** Payment integrity · Defensive validation

## What happened

While using sniping software, we observed a final debit that differed from an earlier listing quote. Our investigation identified a gap between the price used to make a purchase decision and the amount presented for final confirmation. Some third-party bots confirmed payment forms without comparing the updated amount with the previously accepted price.

The episode included deliberately repriced listings and real marketplace transactions. This retrospective documents the resulting validation failure and the engineering lessons from it.

## Outcome

According to our original retrospective, some affected tool authors corrected their price validation after community discussions.

## Defensive engineering lessons

- Treat a listing quote as provisional. Use the payment form's authoritative amount to verify the pending charge.
- Revalidate the item, amount and currency against the user's approved terms immediately before confirmation.
- Abort mismatches; obtain fresh authorization before accepting changed terms.
- Log the quoted price, confirmed amount and transaction identity for investigation.
- Test changed-price, stale-quote and mismatched-currency cases, including the period between selection and confirmation.

## Supporting image

![Marketplace sale notification](../../assets/latency-trap/sale-notification.png)

*A sale notification from the incident, showing the sale amount and the Stars credited to the account. It is an interface record, not a latency benchmark or a net-profit calculation.*

[← Back to portfolio](../../README.md)

