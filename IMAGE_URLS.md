# Image URLs Reference

Current menu item images are loaded from Unsplash. Here are the direct URLs:

## Menu Item Images

### 1. Idly
- **URL:** https://images.unsplash.com/photo-1588168333986-5078d3ae3976?w=400&h=300&fit=crop&auto=format
- **Direct View:** https://images.unsplash.com/photo-1588168333986-5078d3ae3976
- **Save as:** `public/images/idly.jpg`

### 2. Puttu
- **URL:** https://images.unsplash.com/photo-1504674900247-0877df9cc836?w=400&h=300&fit=crop&auto=format
- **Direct View:** https://images.unsplash.com/photo-1504674900247-0877df9cc836
- **Save as:** `public/images/puttu.jpg`

### 3. Poori
- **URL:** https://images.unsplash.com/photo-1563379091339-03246963d599?w=400&h=300&fit=crop&auto=format
- **Direct View:** https://images.unsplash.com/photo-1563379091339-03246963d599
- **Save as:** `public/images/poori.jpg`

### 4. Dosa
- **URL:** https://images.unsplash.com/photo-1596797038530-2c107229654b?w=400&h=300&fit=crop&auto=format
- **Direct View:** https://images.unsplash.com/photo-1596797038530-2c107229654b
- **Save as:** `public/images/dosa.jpg`

### 5. Coffee
- **URL:** https://images.unsplash.com/photo-1461023058943-07fcbe16d735?w=400&h=300&fit=crop&auto=format
- **Direct View:** https://images.unsplash.com/photo-1461023058943-07fcbe16d735
- **Save as:** `public/images/coffee.jpg`

### 6. Tea
- **URL:** https://images.unsplash.com/photo-1556679343-c7306c1976bc?w=400&h=300&fit=crop&auto=format
- **Direct View:** https://images.unsplash.com/photo-1556679343-c7306c1976bc
- **Save as:** `public/images/tea.jpg`

### 7. Vada
- **URL:** https://images.unsplash.com/photo-1529692236671-f1f6cf9683ba?w=400&h=300&fit=crop&auto=format
- **Direct View:** https://images.unsplash.com/photo-1529692236671-f1f6cf9683ba
- **Save as:** `public/images/vada.jpg`

## Where Images Are Used

- **Configuration:** `backend/data/menu.json` (contains image URLs)
- **Display:** `public/index.html` and `public/admin.html` (via JavaScript)
- **Storage Location (if downloaded locally):** `public/images/`

## Viewing Images

1. **In Browser:** Copy any "Direct View" URL above and paste in your browser
2. **On Website:** Visit your site and images will load from Unsplash
3. **In Code:** Check `backend/data/menu.json` for all image URLs

## Download Images Locally (Optional)

If you want to store images locally instead of using external URLs:

1. Click each "Direct View" URL above
2. Right-click the image → "Save image as..."
3. Save to `public/images/` folder with correct filename (e.g., `idly.jpg`)
4. Update `backend/data/menu.json` to use `/images/idly.jpg` instead of Unsplash URL

**Note:** Images will load from the internet by default. No local storage needed unless you want offline access or custom images.

