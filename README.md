# Detect AI-Generated Phishing Emails

<div align="center">
  <img src="https://github.com/30Gramz/AI-Generated-Phishing-Email-Detection/blob/386d8a733dcf532fd1868691532145813aadd2de/images%20(1).png">
</div>


This project focuses on detecting AI-generated phishing emails using free tools in a home lab environment. It analyzes email headers and body content to identify suspicious patterns, such as spoofed sender addresses, unusual language structures, and AI-generated text. The project uses *SpamAssassin* for spam filtering, *YARA rules* for AI text pattern detection, and a *Python script* to assess email readability and detect potential AI-generated phishing attempts. The goal is to develop an efficient, open-source method for identifying advanced phishing attacks.

# Technical skills

### 1. Email Security Analysis

 - Extracting and analyzing email headers.  
 - Identifying spoofed addresses and phishing indicators.


### 2. AI-Generated Text Detection

 - Using *Python* to analyze text readability and detect AI patterns.  
 - Writing *YARA rules* to flag AI-generated content.

### 3. Spam Filtering & Threat Detection

 - Configuring *SpamAssassin* to classify phishing emails.  
 - Training spam filters with phishing datasets.

### 4. Network Traffic Monitoring

 - Capturing SMTP/IMAP email traffic with *Wireshark*.

### 5. Automation & Scripting

 - Writing Python scripts to process multiple emails automatically.

### 6. Cybersecurity Investigation & Incident Response

 - Collecting and analyzing phishing samples.
 - Creating security reports on AI-generated phishing threats.  

# Project Plan

- *Ubuntu VM* (your existing setup)  
- *Python* (for email analysis and AI detection)  
- *Wireshark* (to capture network traffic)  
- *SpamAssassin* (open-source spam filter)  
- *YARA Rules* (to detect AI-generated patterns)  
- *Phishing Email Dataset* (from open sources like PhishTank)

# Steps

## Step 1: Set Up The Environment
1. Update Ubuntu

bash :
sudo apt update && sudo apt upgrade -y    (*copy onto Ubuntu terminal*)

2. Install Required Tools

 bash : 
 sudo apt install python3 python3-pip wireshark spamassassin yara -y   (*copy onto Ubuntu terminal*)

 ## Step 2: Collect Phishing Email Samples

1. Use public phishing email datasets
 - PhishTank <a href="https://www.phishtank.com/">PhishTank</a>.
 - SpamAssassin corpus <a href="https://spamassassin.apache.org/publiccorpus/">SpamAssassin</a>.

2. Store them in a directory:

 - bash :
 mkdir ~/phishing_emails && cd ~/phishing_emails  (*copy onto Ubuntu terminal*)

 ## Step 3: Analyze Email Headers & Content

 1. Extract email headers

- bash :
cat email_sample.eml | grep -E "From:|Subject:|Received:|Return-Path:"  (*copy onto Ubuntu terminal*)

 3. Check for AI-generated text patterns

 - Look for unusual sentence structures and unnatural text flow.
 

  
