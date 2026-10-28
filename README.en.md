# KOL Collaboration Contract Updater / KOL 合作合同更新器

[简体中文](README.md) | **English**

Create a separate copy of your Word contract, update creator/product/commission/date/address details and check for leftover data.

[Download complete project ZIP](https://github.com/hezonglinhzl-creator/varla-electric-mobility-skills-and-tools/raw/main/packages/skill-varla-kol-contract-updater.zip) · [All projects](https://github.com/hezonglinhzl-creator/varla-electric-mobility-skills-and-tools)

## Features

- Preserve DOCX layout
- Write a separate output copy
- Review deliverables and replaced details

## What is included

| Part | Location |
| --- | --- |
| Skill instructions | [SKILL.md](skill/varla-kol-contract-updater/SKILL.md) |

This project is a Codex skill/workflow with its own instructions or scripts; it has no separate app server to launch.

## Download and extract

1. Open this repository, choose **Code → Download ZIP**, or use the complete-project download above.
2. Right-click the downloaded ZIP and choose **Extract All**. Open the extracted folder containing this README.
3. Keep the whole folder together. Start the program first using the next section, then install/use its skill.

Installation also writes PACKAGE-LOCATION.json beside the installed SKILL.md, mapping the bundled programs to their actual extracted directories. Keep the full extracted folder; rerun the installer after moving it. Existing Skill content is preserved by default while paths are refreshed.

## 1. Set up the program first

No app installation is required. Prepare Codex and the input listed below. If the skill includes Python scripts, install the stated script dependency before running them.

## 2. Install the Skill

1. At the extracted project's root, double-click `安装Skill.cmd` on Windows.
2. The installer copies `skill/varla-kol-contract-updater` to `%USERPROFILE%\.codex\skills\varla-kol-contract-updater`. Existing same-name skills are skipped; check the displayed result.
3. Reopen Codex and start a new chat. Use the exact skill name shown below.
4. If scripts cannot run under your organization policy, open install.ps1 for review or copy the skill directory manually to the same destination.

## 3. First task

| Prepare | Details |
| --- | --- |
| Input | Your DOCX template and confirmed agreement fields. |
| Output | A new DOCX; PDF export needs Word/WPS/LibreOffice or a separate conversion step. |

```text
Use varla-kol-contract-updater to inspect replaceable fields and generate a preview copy using synthetic details while preserving my template.
```

## Contract script

Run inside `skill/varla-kol-contract-updater`. Example details are synthetic; supply your own DOCX template.

```powershell
python -m pip install python-docx
python scripts/update_contract.py --input C:/path/template.docx --output C:/path/preview.docx --name "Sample Creator" --email creator@example.com
```

## Limits and troubleshooting

Requires python-docx. Real contracts/signatures are excluded, and commercial terms must come from confirmed inputs.

| Problem | Next step |
| --- | --- |
| Skill not visible | Check the installer output and destination SKILL.md, reopen Codex and start a new chat. |
| Program fails to start | Open its directory in PowerShell and run the documented command so the error remains visible; check that program's README. |
| Browser panel missing | Select the exact folder containing manifest.json, check supported websites and refresh the website tab. |
| External service unavailable | Supply your own authorization/settings and verify access. Keep local output rather than claiming a sync/send succeeded. |

## Privacy and status

This is a source/skill distribution. No real accounts, OAuth tokens, customer/KOL lists, contracts, orders, mailbox exports or business media are included. You configure your own services. Documentation and package paths were checked; live orders, sends and publications were not executed as part of documentation validation.
