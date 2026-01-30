# App Store Products Configuration

This document confirms the App Store Connect product configuration for ITHAC Premium subscriptions.

## Product IDs (App Store Connect)

All products are configured as **Auto-Renewable Subscriptions**:

1. **ITHAC Premium Annual**
   - Product ID: `com.itac.premium.annual`
   - Type: Auto-Renewable Subscription
   - Billing: Annual (1 year)

2. **ITHAC Premium Monthly**
   - Product ID: `com.itac.premium.monthly.` (Note: trailing period)
   - Type: Auto-Renewable Subscription
   - Billing: Monthly (1 month)

3. **ITHAC Premium Quarterly**
   - Product ID: `com.itac.premium.quarterly`
   - Type: Auto-Renewable Subscription
   - Billing: Quarterly (3 months)

## Configuration Files

### 1. `config/revenuecat.ts`
Production configuration with product IDs:
```typescript
productIds: {
  monthly: 'com.itac.premium.monthly.', // With trailing period
  quarterly: 'com.itac.premium.quarterly',
  annual: 'com.itac.premium.annual',
  lifetime: 'com.itac.premium.platinum',
}
```

### 2. `config/pricing.ts`
Pricing plans using the product IDs:
- **Annual**: `com.itac.premium.annual` - $839.88/year
- **Monthly**: `com.itac.premium.monthly.` - $89.99/month
- **Quarterly**: `com.itac.premium.quarterly` - $224.97/quarter

### 3. `ios/Products.storekit`
StoreKit configuration file for local testing:
- All three products configured with correct IDs
- Prices match production pricing
- Subscription groups configured

### 4. `services/subscription.ts`
Product ID to RevenueCat package mapping:
- `com.itac.premium.monthly.` → `$rc_monthly`
- `com.itac.premium.quarterly` → `$rc_lifetime`
- `com.itac.premium.annual` → `$rc_annual`

## Verification Checklist

- [x] Product IDs match App Store Connect exactly
- [x] Monthly product ID includes trailing period (`com.itac.premium.monthly.`)
- [x] All products configured as Auto-Renewable Subscriptions
- [x] Pricing configuration matches App Store Connect
- [x] StoreKit file updated for local testing
- [x] RevenueCat mapping configured correctly

## Important Notes

1. **Trailing Period**: The monthly product ID has a trailing period (`com.itac.premium.monthly.`). The code handles both with and without the period for compatibility.

2. **RevenueCat Mapping**: Ensure these product IDs are linked to the correct entitlements in RevenueCat Dashboard:
   - Monthly → `$rc_monthly` entitlement
   - Quarterly → `$rc_lifetime` entitlement
   - Annual → `$rc_annual` entitlement

3. **App Store Connect**: Products must be:
   - Created in App Store Connect
   - Approved and available
   - Linked to the same subscription group
   - Configured with correct pricing

4. **Testing**: Use the `ios/Products.storekit` file for local testing in Xcode.

## Next Steps

1. Verify products in App Store Connect match these IDs exactly
2. Ensure products are approved and available
3. Link products to RevenueCat entitlements
4. Test purchases in TestFlight before production release

