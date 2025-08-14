# Twitter API Setup Guide

## Quick Setup Steps

### 1. Get Twitter Developer Access
1. Visit [Twitter Developer Portal](https://developer.twitter.com/en/portal/dashboard)
2. Sign up with your Twitter account
3. Create a new project and app

### 2. Generate Bearer Token
1. Go to your app's "Keys and Tokens" section
2. Click "Generate" under Bearer Token
3. Copy the Bearer Token (starts with "AAAA...")

### 3. Configure Environment
1. Create `.env.local` in your project root:
\`\`\`bash
TWITTER_BEARER_TOKEN=AAAAAAAAAAAAAAAAAAAAAMLheAAAAAAA0%2BuSeid%2BULvsea4JtiGRiSDSJSI%3DEUifiRBkKG5E2XzMDjRfl76ZC9Ub0wnz4XsNiRVBChTYbJcE3F
\`\`\`

### 4. Restart Development Server
\`\`\`bash
npm run dev
\`\`\`

## Troubleshooting

### Error: "Authentication failed"
- ✅ Check Bearer Token starts with "AAAA"
- ✅ Ensure no extra spaces in token
- ✅ Verify token is over 100 characters
- ✅ Restart development server after adding token

### Error: "Access forbidden"
- Your API access level may be insufficient
- Essential access only allows recent tweets (7 days)
- Consider upgrading to Elevated access

### Error: "Rate limit exceeded"
- Wait 15 minutes for rate limit reset
- Reduce search frequency
- Consider implementing caching

## API Access Levels

| Level | Monthly Tweets | Historical Search | Cost |
|-------|---------------|-------------------|------|
| Essential | 500K | ❌ | Free |
| Elevated | 2M | ❌ | Free |
| Academic | 10M | ✅ | Free (Research) |

## Testing Your Setup

The app will automatically test your connection and show:
- ✅ **Connected**: API working correctly
- ❌ **Setup Required**: Missing or invalid credentials
- ⚠️ **Demo Mode**: Using mock data as fallback
