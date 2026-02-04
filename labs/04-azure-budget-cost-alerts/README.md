# Lab 04: Azure Budget + Cost Alerts

## Objective
Create an Azure budget at the subscription level and configure cost alerts to monitor spending and receive email notifications when usage reaches defined thresholds.

## Resources Created
- Azure Budget
- Cost alert thresholds

## Prerequisites
- Existing Azure tenant + subscription
- Contributor or Cost Management Contributor permissions

## Naming Used (Examples)
- Budget Name: monthly-budget
- Scope: Subscription

---

## Build Steps (Azure Portal)

### Navigate to Budgets

1. In the Azure Portal, search for and select **Subscriptions**.
2. Choose your subscription.
3. From the left-hand menu, under **Cost Management**, select **Budgets**.
4. Click **Add**.

---

### Budget Configuration

5. On the **Create a budget** screen, configure:

- Name: monthly-budget (example)
- Reset period: Monthly  
- Creation date: Today  
- Expiration date: Optional  
- Budget amount: Example $50 (adjust based on your lab usage)

6. Click **Next** to move to **Set alerts**.

---

### Alert Configuration

7. Under **Alert conditions**, configure:

- Type: Actual
- Percentage of budget: 80% (example early warning)

Optional:
- Add additional thresholds (for example 100%)

8. Under **Alert recipients**, enter your email address.

9. Click **Create**.

---

## Validation

- Confirm the budget appears in the Budgets blade.
- Verify the budget amount displays correctly.
- Confirm the spending progress bar reflects current usage (often 0% for new subscriptions).
- Ensure alert thresholds are listed.

---

## Screenshots to Capture

- Budget configuration screen → 01-budget-config.png  
- Alert conditions setup → 02-budget-alert-config.png  
- Final budget overview → 03-budget-validation.png  

---

## Cleanup (Optional)

After completing the lab:

1. Navigate to **Subscriptions**.
2. Select your subscription.
3. Open **Budgets**.
4. Click the ellipsis (...) next to the budget.
5. Select **Delete** and confirm.

---

## Notes / What I Learned

- Budgets provide visibility into spending but do not automatically stop resources.
- Alert thresholds can be configured at multiple percentages (for example 80% and 100%).
- Email alerts are the simplest notification method; Action Groups enable automation.
- Cost Analysis provides detailed charge breakdowns once usage data is available.
- Budgets can be configured with monthly, quarterly, or annual reset periods.

---

## Next Steps

- Monitor Cost Analysis as additional resources are deployed.
- Remove the budget once it’s no longer needed for this lab series.
