# Ohio Childcare Locator

Interactive map of licensed childcare providers in Ohio, built with Leaflet and OpenStreetMap.

🌐 **Live Site**: [View on Vercel](https://ohio-childcare-map.vercel.app)

## Features

- 🗺️ Interactive map with all licensed Ohio childcare providers
- 🔍 Search by city, ZIP code, or provider name
- 🎨 Filter by provider type (Center, Home, School-Age)
- 📱 Mobile-responsive design
- 📊 Real-time provider count
- 📞 Clickable phone numbers

## Data Source

Data sourced from [U.S. Department of Health and Human Services (HHS) Child Care Provider Dataset](https://files2.hhs.gov/childcare/ChildCareProviderData.csv), updated quarterly.

All facilities are licensed by the [Ohio Department of Job and Family Services (ODJFS)](https://childcaresearch.ohio.gov).

## Deployment

This project is deployed on Vercel. To deploy:

1. Connect your GitHub repository to Vercel
2. Vercel will automatically detect it as a static site
3. Deploy!

## Local Development

Simply open `index.html` in a web browser or use a local server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve
```

## Adding Full Dataset

1. Download latest HHS dataset: https://files2.hhs.gov/childcare/ChildCareProviderData.csv
2. Filter for Ohio (ProviderState == "OH")
3. Geocode addresses to get lat/long coordinates
4. Convert to GeoJSON format
5. Save as `data/ohio-childcare.geojson`

The map will automatically load the GeoJSON file if it exists, otherwise it uses sample data.

## License

Public domain - uses open government data.

