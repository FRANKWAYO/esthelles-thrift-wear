# Esthelle's Product Management Guide

## 📦 How to Update Dresses & Prices

You now have a complete product management system! Here's how to use it:

### **Option 1: Admin Dashboard (Easiest)**
1. Open `admin.html` in your browser
2. You'll see three tabs: **View All**, **Add New Dress**, **Export/Import**

#### View All Tab
- See all your products in a table
- Search by dress name or type
- Click **Edit** to update price, rating, name, colors, etc.
- Click **Delete** to remove a dress

#### Add New Dress Tab
Fill out the form to add a new product:
- **Dress Name** - e.g., "Adom Linen Wrap Dress"
- **Type** - Casual, Formal, Party, Seasonal
- **Length** - Mini, Midi, Maxi
- **Image URL** - Full URL to the product image
- **Price (GH₵)** - Current selling price
- **Original Price** - Optional, for showing discounts
- **Rating** - Star rating (e.g., 4.8)
- **Reviews** - Number of reviews
- **Colors** - Comma-separated (e.g., "Cream,Sage,Black")
- **Sizes** - Comma-separated (e.g., "XS,S,M,L,XL")
- **Badge** - Optional (e.g., "Bestseller", "New In", "Eco Find")
- **Badge Color** - Gold, Ink, Blush, or Sale

#### Export/Import Tab
- **Download JSON** - Backs up all your products
- **Import JSON** - Restore or merge products from a file

### **Option 2: Direct JSON Editing**
Edit `products.json` directly to update products:
```json
{
  "id": 1,
  "name": "Dress Name",
  "type": "casual",
  "price": 240,          // UPDATE THIS
  "old": 320,            // Old price (optional)
  "rating": 4.8,
  "reviews": 124
}
```

---

## 🔧 How It Works

| File | Purpose |
|------|---------|
| **products.json** | Master data file with all products, prices, colors, images |
| **admin.html** | Dashboard to view, add, edit, and delete products |
| **index.html** | Main site - loads products from `products.json` |

When you update `products.json` (via admin panel or direct edit), the main site automatically shows the changes when you refresh!

---

## ⚡ Quick Price Updates

**Fastest way to update a single price:**
1. Open `admin.html`
2. Find the dress in the table
3. Click **Edit**
4. Change the price
5. Click **Save Changes**
6. Refresh your main site to see the change

**Bulk update example:**
- Download JSON from Export tab
- Edit prices in the JSON file
- Upload it back via Import tab

---

## 📝 Product Data Fields Explained

| Field | Description | Example |
|-------|-------------|---------|
| id | Unique product ID | 1 |
| name | Dress name | "Adom Linen Wrap Dress" |
| type | Category | "casual" |
| length | Dress length | "midi" |
| price | Current price in GH₵ | 240 |
| old | Original price (optional) | 320 |
| rating | Star rating | 4.8 |
| reviews | Review count | 124 |
| colors | Available colors | ["Cream","Sage","Black"] |
| sizes | Available sizes | ["XS","S","M","L","XL"] |
| img | Image shorthand | "p1" |
| badge | Special badge | "Bestseller" |
| bc | Badge color | "b-gold" |
| added | Days since added | 5 |

---

## 🆚 Changing Image URLs

If you want to use different product images:

1. Get the full image URL
2. In `admin.html`, click **Edit** on the dress
3. Or manually update `products.json` - change the `img` field to the full URL
4. Example: `"img": "https://example.com/dress.jpg"`

---

## 💾 Backing Up Your Products

Regular backups are smart!

1. Open `admin.html`
2. Go to **Export/Import** tab
3. Click **📥 Download JSON**
4. Save the file safely

---

## 🎨 Badge Colors Available

- **b-gold** → Gold (Bestseller, Editor's Pick)
- **b-ink** → Dark (One of One, New In)
- **b-blush** → Pink (Eco Find)
- **b-sale** → Dark Pink (On Sale - auto-calculated)

---

## ❓ FAQ

**Q: Will changes appear immediately?**
A: Update in admin panel or JSON → Refresh your main website → Changes show!

**Q: Can I add unlimited products?**
A: Yes! Add as many as you want.

**Q: What if I delete a product by mistake?**
A: Import your backup JSON to restore it.

**Q: How do I show a discount?**
A: Set both `price` and `old` fields. Admin panel and site automatically calculate & display the discount percentage.

---

## 📱 Using on Your Phone

The admin panel is mobile-friendly! You can manage products from your phone.

---

**Questions?** The system is designed to be simple. Start with the admin dashboard - it's the easiest way! 🚀✦
