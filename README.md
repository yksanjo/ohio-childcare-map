# Ohio Childcare Map

A public, searchable map of all licensed childcare providers in Ohio that accept public subsidies.

🔍 **Data Source**: 
- Ohio Department of Job and Family Services (ODJFS)
- Public records published at: https://childcaresearch.ohio.gov
- Includes license status, subsidy contracts (CCIU/PI/SP), Star Ratings, inspections

⚖️ **Legal Basis**: 
- Ohio Revised Code § 5104.031 (public records)
- Federal CCDF Plan 2024–2026 (transparency requirement)

🚀 **Deployed on Vercel** — updated monthly.

## Features

- 🗺️ Interactive map with all licensed Ohio childcare providers
- ⭐ Star ratings (1-5) from Ohio's quality rating system
- 💰 Subsidy contract indicators (CCIU, PI, SP)
- 📋 Inspection history and compliance status
- 📱 Mobile-responsive design
- 📞 Clickable phone numbers

## To Update Data

1. Run data extraction script against ODJFS public API
2. Replace `public/ohio-childcare.json`
3. Push to GitHub → Vercel auto-redeploys

## Local Development

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve
```

Then open `http://localhost:8000` in your browser.

## Data Structure

The `public/ohio-childcare.json` file contains GeoJSON with the following properties per provider:

- `providerId`: Unique identifier
- `providerName`: Name of the facility
- `address`, `city`, `state`, `zipCode`, `county`: Location information
- `phoneNumber`: Contact phone
- `licenseNumber`: ODJFS license number
- `licenseStatus`: Active, Provisional, etc.
- `providerType`: Center or Home
- `starRating`: 1-5 star quality rating
- `totalCapacity`: Maximum capacity
- `ageGroupsServed`: Array of age groups (Infant, Toddler, Preschool, School-Age)
- `contracts`: Array of subsidy contracts (CCIU, PI, SP)
- `inspections`: Array of inspection records with dates and results

## License

Public domain - uses open government data.
