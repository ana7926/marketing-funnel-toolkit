# 🚀 Google Sheets Business Toolkit 📊💼

[This bad boy](https://docs.google.com/spreadsheets/d/1WQeCAfbRjIPxgSVgwQHFGvEazNcwzVSTiosd9x9fu4Q/edit?usp=sharing) is a **Swiss Army spreadsheet** 🧰 built in Google Sheets, designed to help businesses clean their mess across **Marketing**, **Finance**, and **Payroll** (yes, even Jeff in accounting is impressed).

![dashboard](/assets/main_dashboard.gif)

## 📚 Table of Contents

- [Project Structure](#project-structure)
- [The Project](#the-project)
- [Financial Analysis — The Control Center of Your Business](#financial-analysis--the-control-center-of-your-business)
- [How Did We Start?](#how-did-we-start)
- [Step 1: Digitalize the Great Ol’ Notebook](#step-1-digitalize-the-great-ol-notebook)
- [Step 2: Connect It to the Mothership](#step-2-connect-it-to-the-mothership)
- [Step 3: Build the Cashflow Sheet Like a Pro](#step-3-build-the-cashflow-sheet-like-a-pro)
- [Step 4: Build That P&L Sheet Like a Financial Wizard](#step-4-build-that-pl-sheet-like-a-financial-wizard)
- [Step 5: Crunch the Numbers for Income](#step-5-crunch-the-numbers-for-income)
- [Step 6: Add Other Incomes](#step-6-add-other-incomes)
- [Step 7: Add Other P&L Expenses](#step-7-add-other-pl-expenses)
- [Conclusion](#conclusion)
- [Closing Thoughts](#closing-thoughts)

## Project Structure

The toolkit is divided into three powerful parts:

### 1. 🎯 Marketing Funnels

[Here is the description](/marketing_funnel/README.MD)

Because throwing money at ads and hoping for the best is *so 2020*. This section helps you:

- Analyze the performance of different marketing channels like a data ninja 🥷  
- Identify which channels are killing it 🏆 and deserve more ad spend  
- Call out the budget black holes 🕳️ that need to be fixed, fast  

### 2. 📈 Financial Analysis

All the money stuff, minus the tears:

- Assess income, expenses, and profitability like a Wall Street wizard 🧙‍♂️  
- Track vital business metrics to make sure your company stays alive (and thriving) 💪  
- Make financial decisions that *won’t* require a magic 8-ball 🎱  

### 3. 💰 Salary Widget

Because payroll math shouldn’t feel like rocket science:

- Calculate employee salaries, taxes, and bonuses without a headache 🧾  
- Show employees their **KPI performance** in real-time 📊  
- Clearly display what they need to do to level up that paycheck 💸 (because who doesn’t love a good salary boost?)

---

It’s like a business analyst and a spreadsheet had a baby... and that baby is a genius 👶📈.

---


# The Project

> ⚠️ **Quick Heads-Up!**  
> I'm not gonna bore you with all the implementation magic 🪄 (because, let’s be honest, 99.8% of readers would rather wrestle a bear than read that).  
> **BUT** — if you're the 0.2% who lives for spreadsheets and formulas — here’s your golden ticket 🎟️:  
> [👉 Click to explore the sheet](https://docs.google.com/spreadsheets/d/1WQeCAfbRjIPxgSVgwQHFGvEazNcwzVSTiosd9x9fu4Q/edit?usp=sharing) (viewer access only, no breaking stuff please 🛑).

---

## Financial Analysis — The Control Center of Your Business

Originally built with ❤️ for **Fitness Studios**, especially the ones using ERPs that *try* to do it all… but kinda flop when it comes to:

- ❌ Counting Cash Flow  
- ❌ Generating a real Profit & Loss Statement (P&L)

Why does that matter? Well… (*drum roll please*) 🥁  
> Just because the bank account has money in it doesn't mean it’s yours.  
> At best? Maybe a quarter of it is actually yours. Maybe. 😅

And if you don't figure that out quick... well, let’s just say your business might end up doing burpees it didn’t sign up for. 🏋️‍♂️💸

---

## How Did We Start?

We rolled up our sleeves and asked the magic question:  
**What data do we *already* have?** 🕵️‍♀️

Here’s what we found:

1. ✅ The client’s ERP had **sales data** — memberships, pricing, all that jazz  
2. 📝 A good ol’ **physical notebook** with *expenses scribbled in like pirate treasure maps* 🏴‍☠️

And that was it…

💬 *Not great, not terrible.* But hey — you gotta start somewhere, right?

---

And so, with a few formulas, a dream, and possibly way too much coffee ☕ — **we began.**

## Step 1: Digitalize the Great Ol’ Notebook

It was time to retire that legendary expense notebook 📒 (RIP, old friend) and build something cleaner:  
✨ **The Transaction Log.**

[👉 Check it out here](https://docs.google.com/spreadsheets/d/1c7hDcup_u0AhyK11zYkaLzEZFhTqEgNo5fVgM8VUo5M/edit?usp=sharing)

![Transaction Log](/assets/Transaction%20Log.png)

Now, what clients *used to scribble down* in the notebook, they just enter into this sheet.  
This became the **first brick** in building our financial basement 🧱💰 — and trust me, this basement has *good bones*.

---

## Step 2: Connect It to the Mothership

With our shiny new Transaction Log in place, we had to beam that data over to the **Control Center** (aka the fancy dashboard table 🎛️).

Enter this trusty import spell:

```excel
=IMPORTRANGE("https://docs.google.com/spreadsheets/d/1c7hDcup_u0AhyK11zYkaLzEZFhTqEgNo5fVgM8VUo5M/edit?gid=593220343#gid=593220343","TRANSACTION_LOG_WHOLE")
```

## Step 3: Build the Cashflow Sheet Like a Pro

Now that the data was flowing into our system like good karma, it was time to turn that raw info into something *actually useful* — **Cashflow**.

![cashflow_overview](/assets/cashflow_overview.gif)

We pulled the data from the Transaction Log using this formula:

```excel
=SUMIFS(I_TL_EXPENCE,I_TL_CATEGORY,$E25,I_TL_PAYMENT_DATE,F$3,I_TL_BRANCH,'❌ Configuration'!$A$2)
```
Yup, we’re using Named Ranges. A lot. Like, get comfy with them because they’re gonna be your new besties. 🧑‍🤝‍🧑

> 🧠 Pro Tip: Named ranges make your formulas 99% more readable and 1000% less rage-inducing.

Boom — we’ve got a clean, dynamic cashflow tracker that doesn’t make you want to flip a table. 🙌💼

## Step 4: Build That P&L Sheet Like a Financial Wizard

Alright, time to put on our accountant hats 🧙‍♂️ — we’re diving into the magical world of **Profit & Loss** (P&L). But don’t worry, we made it fun. Or at least… tolerable. 😅

We already knew the ERP our client uses logs:
1. 🧍‍♂️ Check-ins  
2. 🚫 Missed workouts  
3. ⌛ Expired memberships  

So we dove into the ERP data like Sherlock Spreadsheet 🕵️‍♀️

We created a new sheet called `Exports` and dumped all the data from the client’s ERP into it. Think of it as the central vault 💾 where all the membership check-ins, missed workouts, and expired subs now live.

>Want to take a peek inside the vault?  
>👉 [Here’s the table](https://docs.google.com/spreadsheets/d/1RNFbm5Liwbc_MEqer1T12WhgvPUN8cYNNmecbcPuHgg/edit?gid=288172794#gid=288172794)

> If you want to see the data samples - [click here](/data_samples/)

![integration_exports](/assets//integration_exports.gif)

---

## Step 5: Crunch the Numbers for Income

From the "Integration" sheet, we piped the numbers into the income part of our P&L sheet, **grouped by membership names and dates** — perfect for A/B testing, performance insights, or just feeling smugly organized. 🧠📅

Here’s the *Frankenstein monster* formula we used to do that:

```excel
=SUMIFS(I_E_CHECK_INS_AMOUNT,I_E_CHECK_INS_DATE,PNL_DATE,I_E_CHECK_INS_MEMBERSHIP_NAME_IN_TABLE,$E9, I_E_CHECK_INS_BRANCH,'❌ Configuration'!$A$2)+SUMIFS(I_E_EXPIRED_MONEY_REMAINS,I_E_EXPIRED_MEMBERSHIP,$E9,I_E_EXPIRED_DATE, PNL_DATE,I_E_EXPIRED_BRANCH_1,'❌ Configuration'!$A$2)+SUMIFS(I_E_MISSED_AMOUNT,I_E_MISSED_DATE,PNL_DATE,I_E_MISSED_BRANCH,'❌ Configuration'!$A$2,I_E_MISSED_NAME_AS_IN_TABLE,$E9)
```
> 💡 $E9 = Membership Name

![P&L_overview](/assets/P&L_overview.gif)

So now we’ve got income from memberships — awesome! BUT WAIT, there’s more…

## Step 6: Add other incomes

Our clients also rent out studio time ⏰ and take a percentage of deposits 💸. We track this too — and yep, we pull it from our old pal, the [Transaction Log](https://docs.google.com/spreadsheets/d/1c7hDcup_u0AhyK11zYkaLzEZFhTqEgNo5fVgM8VUo5M/edit?gid=593220343#gid=593220343)

We used this formula to bring rental/deposit-based income into the fold:

```excel
=IFERROR(SUMIFS(I_TL_DAILY_INCOME,I_TL_CATEGORY,$E6,I_TL_BRANCH,'❌ Configuration'!$A$2,I_TL_START_DATE,"<="&PNL_DATE,I_TL_END_DATE,">="&PNL_DATE),0)
```
> 📌 $E6 = Income Category (like “Renting out studios” or “% of Deposit”)

## Step 7: Add Other P&L Expenses

Now, here’s the thing — pulling **every** expense from the Transaction Log with just one formula?  
Yeah... not gonna happen. That’s like trying to make a protein shake with a fork. 🥴

So, we broke it down into specific categories that we prefer to handle automatically:

1. 👩‍💼 Salaries  
2. 📣 Ad Budget  
3. 💳 Transaction Fees  
4. 🏚️ Depreciation of Assets

Each one had its own little drama and spreadsheet magic. But instead of boring you with every twist and turn (99.8% of people are already asleep 😴)...

Let’s just say:  
> ✅ **They’re all automated**  
> 💪 **They work smoothly**  
> 🤓 **You can absolutely geek out over the formulas if you want to**

If you're one of the beautiful 0.2% Data Nerds who live for this kind of thing —  
👉 [here’s the spreadsheet with all the juicy logic](https://docs.google.com/spreadsheets/d/1WQeCAfbRjIPxgSVgwQHFGvEazNcwzVSTiosd9x9fu4Q/edit?gid=2127869173#gid=2127869173)

Go ahead, click it. You know you want to. 😏📊

---

# Conclusion

Let’s take a breath and admire the journey:

✅ We started with a physical notebook that looked like it’d survived a pirate raid 🏴‍☠️  
✅ We built a transaction system that would make your accountant cry tears of joy 😭  
✅ We wrangled ERP exports like data cowboys 🤠  
✅ We summoned formulas from the Excel underworld 👻  
✅ And we made Cashflow and P&L sheets that *actually make sense*

All while keeping the chaos under control... mostly. 😅

# Closing Thoughts

This toolkit isn't just a spreadsheet. It’s a:
- 🧠 Business brain
- 💵 Finance fairy godmother
- 📊 Data dashboard on caffeine

Whether you're a founder trying to make payroll, a marketer tracking ROI, or a spreadsheet nerd who just loves a good `SUMIFS`, this toolkit has your back.

So go ahead — duplicate it, test it, break it (gently), and make it your own.  
And if all else fails… blame Jeff in accounting. 😉📉

---

> 💌 Got questions? Spot a bug? Want to send coffee money?  
> Ping me via [LinkedIn](https://www.linkedin.com/in/stacy-lockwood/) or toss a star ⭐ on GitHub if this made your life 1% easier.

Stay analytical, stay caffeinated — and never trust a clean whiteboard.  
Peace ✌️ and spreadsheets 📄🧠

