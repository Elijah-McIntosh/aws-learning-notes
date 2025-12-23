# EC2 Budget Setup & Cost Management

Before launching EC2 instances, I set up billing visibility and alerts so I don’t get surprised by charges.

---

## Goal
- Monitor AWS charges clearly
- Track Free Tier usage and forecasts
- Create budgets that email me when spending starts or hits limits
- Enable IAM users/roles to view billing (Root setting)

---

## Key AWS Pages
- Billing & Cost Management
- Bills
- Free Tier
- Budgets
- IAM access to Billing information (Root account setting)

---

## 1) Enable IAM User/Role Access to Billing Information (Root Account)

### Default behavior
- Billing is **Root-only** by default
- IAM users cannot view billing tools unless enabled

### Steps
1. Sign in as the **Root** user
2. Click **Account** (top-right)
3. Scroll to **IAM access to Billing information**
4. **Activate / Enable**
5. Save changes

### Why this matters
- Allows day-to-day access with an IAM user while still monitoring costs
- Supports least privilege (Root stays locked down)
- Helps catch unexpected spend early (especially with EC2)

---

## 2) View Current Charges in the Bills Page

**Path:** Billing & Cost Management → **Bills**

### What I learned
- Bills shows current month charges and breaks them down by service and usage

### What to watch for (common EC2 cost sources)
- EC2 instance runtime
- EBS volumes (can cost even after terminating an instance)
- Snapshots
- Data transfer

---

## 3) Monitor Free Tier Usage + Forecasted Spending

**Path:** Billing & Cost Management → **Free Tier**

### What I learned
- Free Tier shows what I’ve used and what AWS forecasts I might spend
- Forecast helps catch issues before month-end

### Notes
- Free Tier is not a guarantee for every service
- If usage is trending up, I should stop/clean up resources

---

## 4) Create Budgets (Zero-Spend + Monthly Cost Budget)

**Path:** Billing & Cost Management → **Budgets** → Create budget

> Budgets notify me by email — they do **not** automatically stop resources.

### A) Zero-Spend Budget
**Purpose:** Alert me immediately if spending starts when I expect $0.

Steps:
1. Create **Cost budget** (monthly)
2. Set amount to **$0.00** (or lowest allowed)
3. Add email recipient(s)
4. Create budget

Why it’s useful:
- Catches forgotten EC2 instances and leftover resources fast

---

### B) Monthly Cost Budget
**Purpose:** Keep spend under a safe monthly cap while learning.

Example caps:
- $5 / $10 / $20 (whatever I’m comfortable with)

Steps:
1. Create **Cost budget** (monthly)
2. Set monthly limit
3. Add alert thresholds (example: 50%, 80%, 100%)
4. Add email recipient(s)
5. Create budget

Best practice:
- Use multiple thresholds so I have time to react

---

## 5) Quick Checklist After EC2 Labs
- Terminate EC2 instances I’m not using
- Delete unused EBS volumes and snapshots
- Check **Bills** to confirm spend looks normal
- Check **Free Tier** forecast to ensure nothing is trending upward

---

## Key Takeaways
- Root must enable IAM billing access
- Bills shows current charges by service
- Free Tier helps track usage + forecasts
- Budgets send alerts but don’t enforce limits
- EC2 can create surprise charges if resources aren’t cleaned up
