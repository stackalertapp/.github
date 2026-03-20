<p align="center">
  <img src="https://raw.githubusercontent.com/stackalertapp/.github/main/profile/logo.svg" width="120" alt="StackAlert">
</p>

<h1 align="center">StackAlert</h1>

<p align="center">
  <strong>Open-source AWS cost spike detection.</strong><br>
  Get Telegram alerts when your cloud spending jumps unexpectedly.
</p>

<p align="center">
  <a href="https://aws-finops-small-teams.pages.dev">Website</a> &bull;
  <a href="https://github.com/stackalertapp/stackalert-lambda">Lambda</a> &bull;
  <a href="https://github.com/stackalertapp/stackalert-terraform">Terraform</a> &bull;
  <a href="https://github.com/stackalertapp/stackalert-cdk">CDK</a> &bull;
  <a href="https://github.com/stackalertapp/stackalert-pulumi">Pulumi</a>
</p>

---

## What is StackAlert?

A lightweight Rust Lambda that monitors your AWS costs and alerts you via Telegram when spending spikes. Deploy in minutes with Terraform, CDK, or Pulumi.

**Perfect for:**
- Small teams monitoring their own AWS costs
- Anyone giving AI agents (Claude Code, Cursor, Devin) AWS access and wanting cost spike alerts

## Repositories

| Repository | Description |
|---|---|
| [stackalert-lambda](https://github.com/stackalertapp/stackalert-lambda) | Rust Lambda — cost spike detection engine |
| [stackalert-terraform](https://github.com/stackalertapp/stackalert-terraform) | Terraform module for deployment |
| [stackalert-cdk](https://github.com/stackalertapp/stackalert-cdk) | AWS CDK construct (TypeScript) |
| [stackalert-pulumi](https://github.com/stackalertapp/stackalert-pulumi) | Pulumi component (TypeScript) |

## How It Works

```
EventBridge (every 6h) → Lambda → Cost Explorer → Spike Detection → Telegram Alert
```

The Lambda queries AWS Cost Explorer, compares today's spend against a 7-day rolling average, and sends a Telegram alert if any service exceeds the threshold (default: 50% above average).

## License

All repositories are licensed under [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).
