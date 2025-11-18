# Warehouse Inventory App - Android Installation Guide

## 📱 What You're Getting

A **single HTML file** that works as a complete warehouse inventory app on your Android phone:
- ✅ Works offline (no internet needed after first load)
- ✅ Data saved on your phone (IndexedDB)
- ✅ Bulk CSV upload with preview
- ✅ Can be installed as an app (PWA)
- ✅ Touch-optimized for mobile
- ✅ Portable - copy file to any phone

## 🚀 Installation Methods

### Method 1: Direct Open (Easiest)

1. **Download the file** to your Android phone
   - File name: `warehouse-inventory-mobile.html`
   
2. **Open with Chrome or Edge browser:**
   - Find the file in your Downloads folder
   - Tap to open with Chrome or Microsoft Edge
   - Allow file access if prompted

3. **Bookmark for easy access:**
   - Tap the ⋮ menu → ⭐ Add bookmark
   - Or add to home screen (see Method 2)

4. **Start using!**
   - Login as Admin/Manager/Clerk
   - Upload your CSV files
   - Data saved automatically on your phone

### Method 2: Install as App (Recommended)

1. **Open the HTML file** in Chrome or Edge

2. **Install to Home Screen:**
   
   **On Chrome:**
   - Tap the ⋮ menu (top right)
   - Select "Add to Home screen"
   - Name it "Warehouse Inventory"
   - Tap "Add"
   - Icon will appear on your home screen

   **On Edge:**
   - Tap the ⋯ menu (bottom center)
   - Select "Add to phone"
   - Tap "Add"

3. **Launch from home screen:**
   - Tap the icon just like any app
   - Works in fullscreen mode
   - Looks and feels like a native app

### Method 3: Use with Local Web Server (Advanced)

If you want to share with multiple devices on same network:

1. **Install a simple HTTP server app:**
   - Try "Simple HTTP Server" or "HTTP Server" from Play Store

2. **Place HTML file** in the server's folder

3. **Access from any device** on same WiFi:
   - Open browser on other devices
   - Go to `http://[phone-ip]:8080/warehouse-inventory-mobile.html`

## 📂 File Access

The app needs access to:
- **Downloads folder** (to read CSV files you want to upload)
- **Local storage** (to save your inventory database)

**First time you upload a CSV:**
- Android will ask for file permission
- Tap "Allow" to select CSV files

## 💾 Data Storage

**Where is data saved?**
- Data is stored in your phone's browser IndexedDB
- Completely offline and private
- Survives phone restarts
- Tied to the browser (Chrome or Edge)

**How much data can I store?**
- Typically 50-100 MB available
- Enough for 10,000+ items easily

**Backing up data:**
Currently, data is stored locally. To backup:
1. Export inventory to CSV (future feature)
2. Or copy the HTML file to another phone to start fresh

## 🔄 Sharing with Team

**Option 1: Give each person the HTML file**
- Copy `warehouse-inventory-mobile.html` to their phone
- Each person has their own database
- No data sharing between devices

**Option 2: Set up shared server** (requires WiFi)
- Use backend API from `warehouse-api/` folder
- Everyone connects to same database
- Real-time inventory updates
- Requires technical setup (see BACKEND_SETUP.md)

## 📊 Sample Data Included

The app comes pre-loaded with:
- 3 users (Admin, Manager, Clerk)
- 5 sample items
- 4 warehouse locations
- Sample inventory balances

**To reset data:**
- Clear browser data for the site
- Or delete and re-download the file

## 🧪 Testing the App

1. **Login:**
   - Use Admin, Manager, or Clerk account
   - No password needed (add authentication later)

2. **Download template:**
   - Click "Bulk Upload CSV"
   - Click "Download CSV Template"
   - Opens in your spreadsheet app

3. **Edit template:**
   - Fill in your items
   - Format: `ITEM-001 - Description,150 EA`
   - Save as CSV

4. **Upload:**
   - Select location (A-01, B-01, etc.)
   - Choose your CSV file
   - Click "Preview Parsed Data" to check
   - Click "Upload and Process CSV"

5. **View results:**
   - See success/error counts
   - Review each item processed
   - Fix any errors and re-upload

## ⚙️ Customizing for Your Warehouse

**To add your items:**
- Edit the seed data in the HTML file (search for "initializeDatabase")
- Or just upload your items via CSV
- Sample items are harmless - won't affect your real inventory

**To change locations:**
- Edit seed data to match your warehouse layout
- Or add via future UI (coming soon)

**To add more users:**
- Edit seed data
- Or add authentication system (requires backend)

## 🔧 Troubleshooting

**"Database initialization failed"**
- Clear browser cache
- Try different browser (Chrome or Edge)
- Restart phone

**"Can't select CSV file"**
- Grant file access permission
- Check file is actually .csv format
- Try moving file to Downloads folder

**"All items show as 'not found'"**
- Check your CSV format matches template exactly
- Item number must match exactly (case-sensitive)
- Preview data before uploading

**"App won't install to home screen"**
- Use Chrome or Edge browser only
- Firefox/Samsung Internet may not support PWA
- Try "Add to Home screen" instead of "Install"

**"Data disappeared"**
- Don't clear browser data/cache
- Data is tied to specific browser
- If you switch browsers, data won't transfer

## 🆘 Getting Help

**Check these first:**
1. Are you using Chrome or Edge browser?
2. Did you allow file access permissions?
3. Is your CSV format correct? (use Preview feature)
4. Are item numbers exactly matching?

**CSV Format Reminder:**
```csv
Item Number and Description,Quantity and Unit
WIDGET-001 - Premium Widget A,250 EA
BOLT-500 - Hex Bolt,500 CS
```
- Column 1: `ITEM# - Description` (split by " - ")
- Column 2: `Quantity Unit` (split by space)
- Extra columns ignored

## 🚀 Next Steps

Once you're comfortable with the app:

1. **Add all your items** via CSV upload
2. **Set up your locations** to match warehouse
3. **Train your team** on using the app
4. **Consider backend** for multi-user (optional)
5. **Implement cycle counting** (future feature)

## 📱 System Requirements

- **Android 8.0+** (recommended Android 10+)
- **Chrome 90+** or **Edge 90+** browser
- **50 MB free storage** for database
- **No internet required** (after initial file download)

## 🔐 Security & Privacy

- All data stored locally on your phone
- No cloud sync or external connections
- No tracking or analytics
- No account registration needed
- 100% private and offline

---

**Questions?** This is a standalone app - share the HTML file with anyone who needs it!

**Want backend/server?** See `warehouse-api/` folder for Node.js backend setup.
