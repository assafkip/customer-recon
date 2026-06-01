# Customer Recon — setup

This one reads real Reddit threads, so it needs a real Reddit connection. That means a little more setup than a copy-paste prompt. Four steps, one time. After that it is one command.

Why the setup: a plain chat cannot actually read Reddit, so it guesses what your market thinks and you cannot tell. This connects to real threads and links every quote. The setup is the price of not making things up.

---

## Setup (one time, about 10 minutes)

1. **Get Claude Code.** Download the desktop app from claude.ai and sign in. Free or paid Claude both work.

2. **Open it. It will ask you to open a folder.** This is the step nobody expects. Make a new empty folder on your Desktop, name it anything like "recon", and pick it. That folder is where your reports get saved.

3. **Install uv.** This is the small helper that connects to Reddit. Open the Terminal app and paste one line:
   - Mac: `curl -LsSf https://astral.sh/uv/install.sh | sh`
   - Windows (PowerShell): `powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"`
   If you have never opened Terminal: on Mac, press Cmd+Space, type "Terminal", hit enter, paste the line, hit enter.

4. **Install the tool.** In Claude Code, paste this and hit enter:
   ```
   /plugin install github:assafkip/customer-recon
   ```

That is the setup. You only do it once.

---

## Use it

In Claude Code, type:

```
/customer-recon
```

It asks about your market, finds where your buyers gather on Reddit, pulls real threads, and writes you a report: the pains ranked, real quotes with links, the competitor gaps, and the words your buyers actually use. Every quote links to a real thread. If it cannot find something, it tells you.

---

## Want this done for you, or wired into your GTM?

I build custom AI systems for founders and small teams. This is the free, lighter version of the work I do paid. If you want the full thing, or a different operational problem an AI system should be handling, that is the consulting.

Reach me: assaf@askconsulting.io
