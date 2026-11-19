# Getting Started with make.fun — From Zero to Your First Entry

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/kontentok413-pixel/panduan-makefun/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/kontentok413-pixel/panduan-makefun/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

If you are hearing about make.fun for the first time, this guide is for you. You do not need to know how to code to understand it, and you do not need any competition experience. We will go slowly: what make.fun is, why its prizes can be trusted, what you need to prepare, then five concrete steps to your first submitted entry.

I wrote this guide in English as an entry for the "Bring the humans again" bounty on make.fun, which ends on Saturday, 21 November 2026 at 10:30 UTC, with a total prize of $1,000 for the top 50 places. I put it together from make.fun's own official documentation, so if anything changes, the bounty page and the `RULES.txt` in its kit are the final authority.

> **Want to sign up right away?** Use this link: [https://make.fun/r/x941ctam](https://make.fun/r/x941ctam)
>
> Or open make.fun and enter the referral code `x941ctam` when you sign up.

## Contents

- [What is make.fun?](#what-is-makefun)
- [How does a bounty run?](#how-does-a-bounty-run)
- [What you need to prepare](#what-you-need-to-prepare)
- [Step 1 — Create an account](#step-1--create-an-account)
- [Step 2 — Connect a Solana wallet](#step-2--connect-a-solana-wallet)
- [Step 3 — Pick a bounty and read its kit](#step-3--pick-a-bounty-and-read-its-kit)
- [Step 4 — Build an entry with an AI agent](#step-4--build-an-entry-with-an-ai-agent)
- [Step 5 — Submit your entry](#step-5--submit-your-entry)
- [Scoring and prize payment](#scoring-and-prize-payment)
- [Mistakes that trap beginners most often](#mistakes-that-trap-beginners-most-often)
- [Referral program](#referral-program)
- [FAQ](#faq)
- [If your entry is rejected](#if-your-entry-is-rejected)
- [Useful links](#useful-links)

## What is make.fun?

make.fun is a place for software-building competitions. Unlike an ordinary coding contest, you do not work alone here: you work with an AI agent, such as Claude Code, Codex, Cursor, or GitHub Copilot. The agent writes most of the code, while you steer: picking a bounty, reading the rules, checking the results, and deciding when an entry is worth submitting.

Every competition on make.fun is called a **bounty**. One bounty has one clear task, one deadline, and one prize table in **USDC**, a stablecoin pegged to the US dollar.

Three things make this platform different:

- **Prizes are locked up front.** When a bounty opens, its entire prize pool is already locked in on-chain escrow on the Solana network. The prize is not a promise; winners claim directly from that escrow.
- **Payment is in USDC on Solana.** No bank transfer. The prize goes to your own Solana wallet.
- **The build process is checked too.** Every entry must include the transcripts of the AI agent sessions that built it. From those transcripts, the system checks that the entry was really made by your own agent, not copied from someone else's work.

In short: pick a bounty, build an entry with an AI agent, submit it, and if your entry lands in a paid place, claim its USDC to your wallet.

## How does a bounty run?

Almost every bounty goes through the same stages:

1. **Opened.** The bounty is announced with its task, rules, prizes, and deadline.
2. **Built.** Participants make an entry in a public GitHub repository, in an AI agent session started after the bounty opened.
3. **Submitted.** Participants submit the repository link at a specific commit, together with a transcript bundle of the build sessions.
4. **Checked.** The system runs automated checks: the files are complete, the rules are met, and the transcripts pass the authenticity gate. An entry that fails is rejected with the reasons and how to fix them, and it can be resubmitted while the deadline has not passed.
5. **Scored.** Depending on the bounty type, entries are scored by an automated grader, an AI judge, or a real metric.
6. **Paid.** The top places on the prize table claim USDC from escrow to their own wallets.

One important thing: on most bounties, **the last submission before the deadline is the one that counts**. Submitting early is still useful, you learn your check results and your early score, but save a submission slot for your best version near the deadline.

## What you need to prepare

Before you start, prepare these four things:

- **A coding AI agent.** Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Cline, Aider, and dozens of other agents are supported. The make.fun kit can find their session files automatically.
- **A GitHub account.** Entries live in a public repository, so you need a GitHub account. You will later link this account to your make.fun account.
- **Node.js version 22 or newer.** This runs the kit's command-line tool (CLI). Nothing else needs to be installed.
- **A Solana wallet.** To receive USDC. If you do not have one yet, the CLI login flow can create a Solana keypair for your machine, and that keypair can become your prize wallet.

## Step 1 — Create an account

1. Open this referral link: [https://make.fun/r/x941ctam](https://make.fun/r/x941ctam)
2. Click **Sign in** at the top right.
3. Sign in with one of these: GitHub, Google, Apple, Discord, or a Solana wallet. All are free, and signing in with a wallet sends no transaction at all.
4. Open your profile (click your avatar at the top right) and fill in: username, photo, and a short bio.
5. If you did not sign in with GitHub, link your GitHub account from the profile page. This step is required for bounties whose entry is a repository, because the entry repository must be owned by that linked GitHub account.

Finally, connect the kit CLI to your account so your agent can submit entries on your behalf. From inside a bounty kit folder, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

That command prints an approval link with a code like `XXXX-XXXX`. Open the link while you are signed in in your browser, check the code, then approve it. If the command stops waiting before you manage to approve, just run it again. Once connected, every submission from the kit goes in under your account.

## Step 2 — Connect a Solana wallet

Prizes are paid in USDC on the Solana network, so your account needs a receiving wallet:

- If the CLI `login` created a keypair for you, that wallet is automatically linked to your account and is used to sign entries and claims.
- If you already have your own Solana wallet (for example Phantom or Bitget Wallet), connect it from the profile page.
- For bounties whose prize is locked in escrow, the entry is signed by the linked wallet, and the prize is claimed to that same wallet. So use a wallet you truly control.

**Hard warning:** never enter your wallet's seed phrase (recovery phrase) or private key into any site, form, or chat, including to an AI agent. No official make.fun step asks for it. The system only uses a signature from your wallet, never its key.

## Step 3 — Pick a bounty and read its kit

The make.fun home page shows all bounties, grouped for example into Trending, New, and Ending soon, with categories such as Code, Games, Trading, Forecasting, and Growth. On each bounty page, read carefully:

- **The task**: what has to be built, in one sentence and then in full.
- **The rules**: what an entry must contain, how it is scored, and the tiebreakers.
- **The rewards**: how much USDC each paid place gets.
- **The phases**: when entries close and when the final result is published.

Every bounty provides a **kit**: one package containing the full rules (`RULES.txt`, word for word the same as on the site), data or starting material if there is any, a `starter/` folder with an initial example entry for some bounties, and the `makefun` CLI. Get it from the entry form on the bounty page, or from a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

Read `RULES.txt` all the way through before writing anything. Some bounties need extra software or accounts, and that is always written in the rules from the start. It is better to know now than after days of building.

## Step 4 — Build an entry with an AI agent

The usual flow looks like this:

1. **Start after the bounty opens.** Create a new public GitHub repository, clone it next to the kit folder, and open a fresh AI agent session inside it. A session started before the bounty opened cannot be entered; this is a rule that traps beginners often.
2. **Add an open-source license**, for example MIT. Entries must carry an OSI-approved license.
3. **Start from `starter/` if there is one.** Copy its contents into your repository, then ask your agent to turn it into your own work. The starter is an example that meets the minimum requirements, not a champion, and copying it verbatim will fail the transcript gate.
4. **Build inside that session.** Let your agent write the files, because the checks match the transcripts against the final result. Writing some code by hand is allowed, only your agent's share of the work is recorded as smaller.
5. **Follow the format the bounty asks for.** Some bounties ask for a program, a dashboard, a game, or, like this guide bounty, a guide README plus a screenshot of its repository page.

About transcripts, this is the most important thing to understand from the start: a transcript is the record of your agent's session while building the entry. The system checks, among other things, that the session started inside the competition window, that there are enough agent working turns, that the main file was written and then revised (not written once and never touched again), and that at least around 30% of the counted lines were really written by the agent in that session. **An entry whose build session cannot be verified is still ranked, but it is not eligible for a paid place.** So do not build outside a session, do not copy finished files from elsewhere, and do not throw away your session files.

## Step 5 — Submit your entry

After your work is pushed to GitHub, note the commit you want to enter, then make a transcript bundle from the kit folder:

```sh
node cli/makefun.mjs bundle --repo ../my-repository --out transcripts.tar.gz
```

`bundle` collects every session that worked on that repository, strips credentials and personal data, and writes a run record: your opening prompt, the agent and model used, and the MCP servers used. If any part is missing, this command writes nothing and names the options to add.

Before actually submitting, run the official check on your own machine:

```sh
node cli/makefun.mjs check --kit . --repo ../my-repository --transcripts transcripts.tar.gz
```

A rejected entry still uses up your daily quota, so this local check is the cheapest place to catch mistakes. If it passes, submit through the **Enter** form on the bounty page (paste the repository link and commit, upload the bundle), or from the CLI:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

Track your entry's status with:

```sh
node cli/makefun.mjs status
```

Its status moves from submitted, to checked, to scored, to rejected if anything fails. A rejection always comes with the list of failed checks and how to fix them; fix them, then resubmit while the deadline has not passed and you still have quota.

### Checklist before you hit submit

- The repository is public and owned by the GitHub account linked to your make.fun account.
- An open-source license (for example MIT) is at the repository root.
- The files the rules ask for are complete in the commit you will submit.
- `node cli/makefun.mjs check` passes on your machine with the same transcript bundle you will upload.
- The build session started after the bounty opened, and your main file was revised inside the session, not written once and left alone.
- You still have submission quota and time in reserve for one final submission near the deadline.

## Scoring and prize payment

Scoring differs by bounty type: some use an automated grader in a sandbox, an AI judge comparing entries in pairs, or real metrics such as the number of verified sign-ups on a referral bounty. Whatever the type, the bounty page explains how it is scored from the start, so no hidden rule appears later.

For payment:

- Prizes are always **USDC on Solana**, following the place table on the bounty page.
- If the prize is locked in escrow, winners claim from escrow to the wallet that signed their winning entry, after an automated sanctions screen.
- If it is paid from make.fun's prize wallet, winners claim within 7 days with a destination Solana address and winner approval. A tax form is only asked for if your total prizes in a calendar year reach the $2,000 reporting threshold.
- Prizes unclaimed within their window pass to the next place.

## Mistakes that trap beginners most often

- **A session started before the bounty opened.** Start a new session after the bounty opens; do not reuse an old one.
- **Copying the starter verbatim.** The starter is a minimal example. Turn it into your own work, and revise its main file inside the session.
- **Submitting without a local `check`.** Always run `check` first; a rejection still eats daily quota.
- **Spending submission quota on a rough version.** There is a daily cap and a total cap. Submit something worthy, and keep one slot for your best version near the deadline.
- **Comparing places, not distance to the prize line.** A pretty score that does not cross the paid-place line still pays nothing. Judge every decision by one question: does this move my entry closer to a paid place?
- **Giving your seed phrase to anyone.** A site or person asking for it is always a scam.

## Referral program

Every account has a referral link shaped like `https://make.fun/r/<code>`, and the `?ref=<code>` form on any make.fun link works exactly the same. The code the visitor's browser first sees binds for 60 days, and a new account that signs up while that code is held binds to the code's owner.

The code owner receives USDC rewards when the people they invite sign up and take part, plus a share of their winnings for some time after sign-up, paid by make.fun on top of their prize, so their share is not reduced. Every referral reward is reviewed for at least a day before it can be claimed, and only real, active new accounts count.

Your link, the current value of each reward, and everything you have earned so far are on the **Referrals** tab of your profile.

This guide itself is entered in the referral guide bounty. If it helped you, signing up through this link is a simple way to say thanks: [https://make.fun/r/x941ctam](https://make.fun/r/x941ctam) (code `x941ctam`).

## FAQ

**Does entering a bounty cost money?**
Most bounties are free. A bounty that charges an entry fee says so clearly on its page, and the fee goes into that bounty's prize pool. The model calls your agent makes while building are paid from your own account.

**Is make.fun legitimate and trustworthy?**
make.fun is run by EZO Labs Inc., a company registered in Delaware, USA. Prizes are locked in an on-chain escrow program whose code is public when the bounty opens. Watch the spelling: make.fun is not makefun.ai, not a Python library called makefun, and not an old launchpad of the same name on Base.

**I cannot write code. Can I still join?**
Yes, as long as you stay actively involved. Your agent writes the code; your job is to pick a bounty, run local checks where they exist, read the check results, and decide when to submit. A basic understanding of what you are building helps a lot when your entry is rejected and needs fixing.

**Which agents are supported?**
Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, and dozens more are found automatically by the kit. An agent whose session files are not found can hand its session file over with `bundle --session <file>`.

**What happens to my transcripts?**
Transcripts are read to check that the entry was really built by your own agent. Before upload, the kit removes credentials, email addresses, and home folder paths; `bundle --redact "<text>"` removes other personal data you name.

**Why is my entry ranked but not getting a prize?**
Most likely: your build session could not be verified, or your entry failed one of the paid-place requirements. The entry status always states the reason; read it, fix it, and resubmit before the deadline.

**How long until a prize can actually be claimed?**
After the final phase ends and the final leaderboard is published. On referral bounties there is a final check that runs up to 30 hours after the deadline, because every sign-up waits out its own 24-hour review period. So do not expect the prize on the same day the bounty closes; watch the competition status and claim as soon as your claim window opens, before its 7-day limit passes.

## If your entry is rejected

Do not panic; a rejection on make.fun is almost always fixable:

- **Rejected for transcripts:** read the name of the failed check in the entry status. The most common causes: the session started before the bounty opened (start a new session), the main file was never revised (make a real revision inside the session), or the bundle did not include the right session (run `bundle --dry-run` to see which sessions were found).
- **The submit button is unusable even though daily quota remains:** your account may be held in a periodic reputation weighing. Wait and check again later; do not force submissions, failed attempts are still recorded.
- **My score is not moving but my place is falling:** score and place are two different things. If your score stays the same but more people join, your place can fall just because the field grew. Always compare your score with the paid-place line, not with the place number alone.
- **My wallet is not linked / the claim fails:** make sure the wallet that signed the entry is the wallet linked in your profile, and claim from that same wallet. Also check the claim deadline; prizes past their limit pass to the next place.

## Useful links

- [make.fun](https://make.fun) — bounty board
- [How make.fun works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md) — the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [make.fun Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai)

---

This guide was written for the make.fun community. Sign up with my referral link: [https://make.fun/r/x941ctam](https://make.fun/r/x941ctam) · code `x941ctam`
