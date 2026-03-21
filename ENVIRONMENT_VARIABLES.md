# Environment Variables Guide

## Required Variables

### ULTRAVOX_API_KEY
- **Description**: Your Ultravox API key for voice AI functionality
- **Type**: Secret/API Key
- **How to get it**: 
  1. Go to https://app.ultravox.ai
  2. Sign in to your account
  3. Navigate to API Keys or Settings
  4. Copy your API key
- **Example value**: `ZbSdlQ3R.CApXeiAqlE1fciX10VayldQM1QXHPu28` (replace with your actual key)

## Optional Variables

### PORT (if needed)
- **Description**: HTTP port for the web server
- **Type**: Number
- **Default**: 8000
- **Example value**: `8000`

---

## How to Add to Render

1. Go to your Render Web Service dashboard
2. Click **Settings** (or **Environment** tab)
3. Click **Add Environment Variable**
4. For each variable:
   - **NAME_OF_VARIABLE**: Enter the variable name (e.g., `ULTRAVOX_API_KEY`)
   - **value**: Enter the value (e.g., your actual API key)
5. Click **Save** or **Update**

---

## How to Add to .env (Local Development)

In your project root, create a `.env` file (copy from `.env.example`):

```
ULTRAVOX_API_KEY=your-actual-ultravox-api-key-here
PORT=8000
```

Then in Python, these are automatically read by `os.environ.get()`.

---

## Variables Summary Table

| Variable Name | Required | Type | Purpose |
|---------------|----------|------|---------|
| ULTRAVOX_API_KEY | ✅ Yes | Secret | Voice AI API authentication |
| PORT | ❌ No | Number | Web server port (default: 8000) |

---

## Security Notes

- ⚠️ **Never commit `.env` file to GitHub** (it's in `.gitignore`)
- ⚠️ Always use environment variables for secrets in production
- ✅ `.env.example` is safe to commit (it shows the template, not real values)
- ✅ Render's environment variables are encrypted and private
