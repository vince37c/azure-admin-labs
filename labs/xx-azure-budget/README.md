# Lab: Create an Azure Budget

## Objective
Create an Azure budget at the subscription level to monitor costs and configure an email alert when spending reaches a defined threshold.

## Resources Created
- Azure Budget

## Prerequisites
- Existing Azure tenant + subscription
- Contributor or Cost Management Contributor permissions

## Naming Used (Examples)
- Budget Name: monthly-budget

## Build Steps (Azure Portal)

1. In the Azure Portal, navigate to **Subscriptions**.
2. Select your subscription.
3. From the left-hand menu, under **Cost Management**, select **Budgets**.
4. Click **Add**.

### Budget Configuration

5. On the **Create a budget** screen, configure:

- Name: monthly-budget (example)
- Reset period: Monthly
- Budget amount: Example $50 (adjust based on your lab usage)

6. Click **Next** to move to **Set alerts**.

### Alert Configuration

7. Under **Alert conditions**, configure:

- Type: Actual
- Percentage of budget: 80% (example)
- Alert recipients: Add your email address

8. Click **Create**.

---

## Validation

- Confirm the budget appears in the Budgets blade.
- Verify the budget amount displays correctly.
- Confirm the spending progress bar reflects current usage (typically 0% for new subscriptions).

---

## Screenshots to Capture

- Budget configuration screen → 01-budget-config.png  
- Alert conditions setup → 02-budget-alert-config.png  
- Final budget overview → 03-budget-validation.png  

---

## Cleanup

Optional after completing the lab:

1. Navigate to **Subscriptions**.
2. Select your subscription.
3. Open **Budgets**.
4. Click the ellipsis (...) next to the budget.
5. Select **Delete** and confirm.

---

## Notes / What I Learned

- Budgets provide visibility into spending but do not automatically stop resources.
- Alert thresholds can be configured at multiple percentages (for example 80% and 100%).
- Cost Analysis offers detailed charge breakdowns once usage data is available.
- Email alerts are the simplest notification method, but Action Groups can be used for automation.
- Budgets can be configured with monthly, quarterly, or annual reset periods.

---

## Next Steps

- Monitor Cost Analysis as additional resources are deployed.
- Remove the budget once it’s no longer needed for this lab series.
