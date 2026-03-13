# Productivity-Automation-System

## Overview

This project is a **workflow automation system built using n8n** that helps manage daily tasks through Telegram and Google Sheets.
The system automatically stores tasks, tracks their status, and sends reminders for pending tasks using scheduled triggers.

The goal of this project is to demonstrate **workflow automation, API integrations, and event-driven systems** using n8n.


## Features

1. Add tasks directly from Telegram messages
2. Automatically store tasks in Google Sheets
3. Daily automated reminder for pending tasks
4. Status-based filtering using workflow logic
5. Multi-trigger automation using Telegram and Cron triggers


## Workflow Architecture

<img width="246" height="332" alt="image" src="https://github.com/user-attachments/assets/508a382f-f0ea-4639-b512-788506c6ebcc" />


## How It Works

### 1. Task Creation

1. A user sends a message to the Telegram bot.
2. The workflow captures the message using the Telegram Trigger.
3. The task is extracted and saved in Google Sheets with status **Pending**.

### 2. Task Storage

Each task is stored in a structured Google Sheet with fields:

| Task                  | Status  | Date       |
| --------------------- | ------- | ---------- |
| Prepare SQL interview | Pending | 2026-03-13 |


### 3. Daily Reminder Automation

1. A Cron trigger runs every day at a scheduled time.
2. It reads tasks from Google Sheets.
3. If any task has status **Pending**, the bot sends a reminder via Telegram.


## Technologies Used

1. **n8n** – Workflow automation platform
2. **Telegram Bot API** – Task input and notifications
3. **Google Sheets API** – Task storage and tracking


## Use Case

This project demonstrates how automation tools like n8n can be used to build **personal productivity systems** without writing backend code.
It can easily be extended to support:

1. task completion commands
2. priority tagging
3. dashboard integrations
4. email notifications


## Future Improvements

1. `/done` command to mark tasks as completed
2. `/tasks` command to list pending tasks
3. priority-based reminders
4. integration with calendar tools


## Project Purpose

This project was created to learn and demonstrate:

1. Workflow automation
2. Trigger-based event systems
3. API integrations
4. No-code/low-code automation tools
