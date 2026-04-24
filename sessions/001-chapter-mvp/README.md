# Chapter 001 — Session Submissions

This directory contains the verifiable artifacts produced by Exchange sessions in Chapter 001 (MEAC MVP Deployment).

> **Map Leads:** This is where you drop session records. If it is not in this folder, the session did not happen.

## Submission Requirements

Per `ARC-001-REQ-v1.0`, every session must produce a co-signed SCQA record before the session closes. The Map Lead is responsible for committing that record to this directory.

### 1. Folder Structure
Create a new folder for each session using the date and partner organization name:
`YYYY-MM-DD-[partner-name]/`

Example:
`2026-09-15-acme-corp/`

### 2. Required Files
Inside the session folder, you must commit:
1. `ETU-[date]-[partner].md` — The completed SCQA session record (use the template in the `templates/` folder)
2. `canvas.png` or `canvas.jpg` — A clean image of the final Wardley Map produced in the session

### 3. How to Submit (GitHub Web Interface)
If you are not using the command line, use the GitHub web interface:
1. Click **Add file** > **Create new file** in this directory
2. Name the file with the folder path: `2026-09-15-acme-corp/ETU-2026-09-15-acme.md`
3. Paste the contents of the ETU template and fill it out
4. Commit the file directly to the `main` branch
5. Open the folder you just created, click **Add file** > **Upload files**, and upload the map image

## Pre-Session Compliance Documents

Before Session 1, the Chapter Lead must ensure the following documents are signed and stored locally (do not commit PII to this public repository):
- **Athlete Participation Agreement** (NFR-001)
- **TAC Credential Document** (NFR-002)

Templates for these documents are in the `templates/` folder.
