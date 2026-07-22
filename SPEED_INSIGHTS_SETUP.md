# Vercel Speed Insights Setup Guide

## What Was Installed

Vercel Speed Insights has been successfully integrated into the EduQuest project.

## Files Modified

1. **README.md** - Added Speed Insights CDN script and initialization code
2. **index.html** - Created proper HTML entry point with Speed Insights
3. **package.json** - Created to document the dependency
4. **vercel.json** - Created for Vercel deployment configuration

## How It Works

The integration uses the official `@vercel/speed-insights` package (v1.0.10) via CDN:

```html
<!-- Load the library -->
<script type="module" src="https://cdn.jsdelivr.net/npm/@vercel/speed-insights@1.0.10/dist/index.mjs"></script>

<!-- Initialize it -->
<script type="module">
    import { injectSpeedInsights } from 'https://cdn.jsdelivr.net/npm/@vercel/speed-insights@1.0.10/dist/index.mjs';
    injectSpeedInsights();
</script>
```

## What Gets Tracked

Speed Insights automatically collects Core Web Vitals:
- **LCP** (Largest Contentful Paint)
- **FID** (First Input Delay) 
- **CLS** (Cumulative Layout Shift)
- **FCP** (First Contentful Paint)
- **TTFB** (Time to First Byte)
- **INP** (Interaction to Next Paint)

## Viewing the Data

1. Deploy your project to Vercel
2. Go to your project dashboard on Vercel
3. Click on the "Speed Insights" tab
4. View real-time performance metrics from real users

## Important Notes

- ⚠️ Speed Insights **does not** collect data in development mode (localhost)
- ✅ Data collection starts automatically after deployment to Vercel
- 📊 Free tier includes 100,000 data points per month
- 🔒 No sensitive user data is collected - only performance metrics

## Testing

To test that Speed Insights is loaded:
1. Deploy to Vercel or open `test-speed-insights.html` in production
2. Open browser DevTools console
3. Look for Speed Insights initialization messages

## No Build Required

This implementation uses CDN and requires no build tools or npm installation. The site remains fully static and can be deployed as-is to Vercel.

---

For more information, visit: https://vercel.com/docs/speed-insights
