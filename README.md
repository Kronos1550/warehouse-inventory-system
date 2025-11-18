# Warehouse Inventory Management System

A complete, portable warehouse inventory management system designed for mobile-first operations. Features bulk CSV upload, offline storage, and optional backend API.

## 🚀 Quick Start (Android/Mobile)

**For immediate use on your phone:**

1. Download [`mobile-app/warehouse-inventory-mobile.html`](mobile-app/warehouse-inventory-mobile.html)
2. Open in Chrome or Edge browser
3. Add to home screen
4. Start managing inventory!

📱 **[Mobile Installation Guide](mobile-app/INSTALL.md)**

---

## 📦 What's Included

### 1. Mobile App (Standalone)
- **Single HTML file** - works completely offline
- **IndexedDB storage** - data saved on device
- **PWA support** - install as app
- **Bulk CSV upload** with intelligent parsing
- **No backend required** - perfect for independent warehouses

📁 Location: [`mobile-app/`](mobile-app/)

### 2. Backend API (Optional)
- **Node.js + Express** REST API
- **PostgreSQL** database
- **Multi-user support** with role-based access
- **Real-time sync** across devices
- **Complete audit trail**

📁 Location: [`backend-api/`](backend-api/)

### 3. Documentation
- Installation guides
- API documentation  
- CSV format specifications
- Deployment guides

---

## 🎯 Use Cases

### Standalone Mode (No Server)
Perfect for:
- Small warehouses (< 10 users)
- Independent locations
- Offline-only operations
- Quick deployment (< 5 minutes)

**Just use:** `mobile-app/warehouse-inventory-mobile.html`

### Connected Mode (With Backend)
Perfect for:
- Multiple locations
- 10+ concurrent users
- Real-time inventory sync
- Centralized reporting

**Setup:** Backend API + Mobile App

---

## 📱 Mobile App Features

✅ **Bulk CSV Upload**
- Custom format: `ITEM-001 - Description, 150 EA`
- Preview before processing
- Detailed error reporting

✅ **Offline First**
- All data stored locally
- Works without internet
- Syncs when backend available (optional)

✅ **Touch Optimized**
- Large buttons for mobile
- Swipe gestures
- Fast input

✅ **Portable**
- Copy file to any device
- No installation needed
- Share with team easily

---

## 🔧 Backend API Features

✅ **RESTful API**
- Items, locations, inventory management
- Transaction audit trail
- User authentication

✅ **Database Schema**
- 12+ tables with relationships
- Indexes for performance
- Migration scripts included

✅ **Bulk Operations**
- CSV upload endpoint
- Batch updates
- Error tracking

---

## 📊 CSV Upload Format

The system uses a unique 2-column format:

```csv
Item Number and Description,Quantity and Unit
WIDGET-001 - Premium Widget A,250 EA
BOLT-500 - Hex Bolt 1/2",500 CS
DRILL-X200 - Cordless Drill,30 EA
```

**Parsing Rules:**
- **Column 1:** Split by `" - "` → Item Number + Description  
- **Column 2:** Split by space → Quantity + Unit
- Extra columns ignored
- Validates items and units automatically

---

## 🚀 Installation

### Mobile App (Standalone)

```bash
# Clone repo
git clone https://github.com/YOUR-USERNAME/warehouse-inventory-system.git

# Navigate to mobile app
cd warehouse-inventory-system/mobile-app

# Open warehouse-inventory-mobile.html in Chrome on your phone
# Or copy file to your phone's Downloads folder
```

**That's it!** No build step, no dependencies.

### Backend API (Optional)

```bash
# Navigate to backend
cd backend-api

# Install dependencies
npm install

# Setup database
cp .env.example .env
# Edit .env with your PostgreSQL credentials

# Run migrations
npm run migrate

# Seed sample data
npm run seed

# Start server
npm run dev
```

📖 **[Backend Setup Guide](backend-api/README.md)**

---

## 📖 Documentation

- **[Mobile Installation Guide](mobile-app/INSTALL.md)** - Install on Android
- **[Quick Start Guide](mobile-app/QUICKSTART.md)** - 3 steps to upload inventory  
- **[Backend API Docs](backend-api/README.md)** - API endpoints and setup
- **[Frontend Integration](backend-api/FRONTEND_INTEGRATION.md)** - Connect mobile to backend
- **[CSV Format Spec](docs/CSV_FORMAT.md)** - Detailed parsing rules

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────┐
│         Mobile Web App (PWA)            │
│    warehouse-inventory-mobile.html      │
│                                         │
│  ┌─────────────────────────────────┐   │
│  │   IndexedDB (Local Storage)     │   │
│  │   - Items, Locations            │   │
│  │   - Inventory Balances          │   │
│  │   - Transactions                │   │
│  └─────────────────────────────────┘   │
└─────────────────────────────────────────┘
              │ (Optional)
              │ REST API
              ↓
┌─────────────────────────────────────────┐
│         Backend API (Node.js)           │
│                                         │
│  ┌─────────────────────────────────┐   │
│  │   PostgreSQL Database           │   │
│  │   - Centralized data            │   │
│  │   - Multi-user support          │   │
│  │   - Real-time sync              │   │
│  └─────────────────────────────────┘   │
└─────────────────────────────────────────┘
```

---

## 🎓 Getting Started Tutorial

### Day 1: Test with Sample Data

1. Open mobile app on your phone
2. Login as Admin/Manager/Clerk  
3. Go to "Bulk Upload CSV"
4. Download template
5. Upload template (to see it work)

### Day 2: Add Your Data

1. Edit template CSV with your items
2. Use format: `YOUR-ITEM-001 - Your Product,100 EA`
3. Select your location
4. Preview parsed data
5. Upload and review results

### Day 3: Team Rollout

1. Copy HTML file to team phones
2. Show them Quick Start guide
3. Each person uploads their section
4. Monitor for errors

### Week 1: Full Production

1. All items uploaded
2. Team trained
3. Daily inventory updates
4. Consider backend if needed

---

## 🔐 Security & Privacy

**Standalone Mode:**
- All data on device only
- No external connections
- 100% private and offline
- No tracking

**With Backend:**
- JWT authentication
- Password hashing (bcrypt)
- SQL injection protection
- HTTPS recommended
- Role-based access control

---

## 📊 Sample Data Included

The mobile app includes:

**Users:**
- Admin User (ADMIN role)
- Manager User (MANAGER role)
- Clerk User (CLERK role)

**Items:**
- WIDGET-001 - Premium Widget A
- BOLT-500 - Hex Bolt 1/2"
- DRILL-X200 - Cordless Drill 20V
- TAPE-50 - Packing Tape 2"
- SENSOR-A1 - Motion Sensor Pro

**Locations:**
- A-01 (Aisle A - Bay 1)
- A-02 (Aisle A - Bay 2)
- B-01 (Aisle B - Bay 1)
- B-02 (Aisle B - Bay 2)

---

## 🛠️ Tech Stack

**Mobile App:**
- React 18 (UMD build)
- Tailwind CSS
- Dexie.js (IndexedDB wrapper)
- Progressive Web App (PWA)

**Backend API:**
- Node.js 16+
- Express 4
- PostgreSQL 13+
- JWT authentication

---

## 📱 Browser Support

**Mobile App:**
- ✅ Chrome 90+ (Android)
- ✅ Edge 90+ (Android)
- ⚠️ Firefox (limited PWA support)
- ❌ Samsung Internet (no PWA)

**Backend API:**
- Works with any HTTP client
- Fetch API / Axios recommended

---

## 🤝 Contributing

This is a complete working system designed for your warehouse. Feel free to:

- Fork and customize for your needs
- Add features (cycle counting, min/max, reports)
- Improve UI/UX
- Add barcode scanning
- Implement additional reports

---

## 📄 License

MIT License - Free to use and modify

---

## 🆘 Support

**For mobile app issues:**
- See [Mobile Troubleshooting](mobile-app/INSTALL.md#troubleshooting)
- Check [FAQ](docs/FAQ.md)

**For backend API issues:**
- See [Backend Setup Guide](backend-api/README.md)
- Check [API Documentation](backend-api/API.md)

**General questions:**
- Open an issue on GitHub
- Check existing issues first

---

## 🗺️ Roadmap

**Current Version (v1.0):**
- ✅ Bulk CSV upload
- ✅ Offline storage
- ✅ Backend API
- ✅ Mobile-optimized UI

**Planned Features:**
- 🚧 Cycle counting interface
- 🚧 Min/Max management UI
- 🚧 Reports dashboard
- 🚧 Barcode scanning
- 🚧 Export to CSV
- 🚧 Multi-warehouse sync

---

## 📞 Contact

Built for warehouse operations with 2000+ SKUs and high-volume transactions.

**Need help?** Open an issue on GitHub.

---

**Ready to start?** → [Download Mobile App](mobile-app/warehouse-inventory-mobile.html) or [Setup Backend](backend-api/README.md)