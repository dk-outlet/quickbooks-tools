# quickbooks-tools
QuickBooks Tools Reusable Python & .NET scripts for QuickBooks Online automation
  — one-time OAuth setup, encrypted refresh tokens, headless order/inventory sync. 
  
What You Get 
  - OAuth Flow : Run once — client clicks , then forever-automated.
  - Pull Data : Open sales receipts, inventory quantities, customer info.
  - Zero Approval : Works in Development mode (up to 20 companies).
  - Secure : Tokens encrypted with Fernet (never plain text).
  - Ready for Anywhere : Desktop, cron job, AWS Lambda
  - plug and run.
  
Quick Demo (Python) 
bash pip install requests cryptography 
python py/demo.py 

1. Browser opens → log in → click .
2. Paste redirect URL → script saves token.
3. Next run? No pop-up — pulls orders instantly.
  
> Change CLIENT_ID, CLIENT_SECRET, and query to match your environment.

Folder Layout 

quickbooks-tools/ 
├── py/ 
│ ├── demo.py # Full example above 
│ ├── oauth_auth.py # Reusable token handler 
│ └── order_downloader.py# Pulls open sales receipts 
├── cs/ 
│ └── QboInventoryQuery.cs # .NET Lambda-ready version 
└── utils/ 
  └── encryption.py # Fernet wrapper for token security MIT Licensed • Built by For Upwork, prototypes, or internal tools — ship fast, stay clean.
