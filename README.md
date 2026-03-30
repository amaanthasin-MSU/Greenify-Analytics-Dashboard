# Greenify Analytics Dashboard

> 🌱 **Real-time job market analytics dashboard for sustainable careers in Michigan**

A production-ready analytics platform built with Next.js that aggregates and visualizes job market data across Tech, Engineering, Business, and Health sectors, helping job seekers discover opportunities in Michigan's growing green economy.

---

## 📊 Problem

Job seekers in Michigan's sustainable career market lack centralized, data-driven insights into hiring trends, top employers, and regional opportunities. Traditional job boards don't provide the analytical depth needed to make informed career decisions or understand market dynamics across different sectors and geographic regions.

---

## 🎯 Objective

Develop a comprehensive analytics dashboard to visualize Michigan job market trends using real-time data, enabling users to:
- Track hiring patterns across four major industries
- Identify top employers and in-demand skills
- Analyze geographic distribution of opportunities
- Monitor employment type trends over time

---

## 📁 Dataset

- **Source:** Supabase PostgreSQL database with Discord scraper integration
- **Features include:** job titles, company names, locations (city/county), employment types, required skills, posting dates
- **Data updates:** Real-time ingestion from Green Machine Discord bot
- **Schema:** Normalized tables with foreign key relationships between `job_postings_ingest_test`, `job_field_counts`, and `mi_counties`

---

## 🔧 Approach

### Data Architecture
- Connected Supabase PostgreSQL database to Next.js via API keys
- Implemented RESTful API routes for each industry category
- Designed normalized schema with 29 subcategories across 4 main fields
- Real-time aggregation using SQL JOINs and filtering

### Dashboard Development
- Built responsive UI with React components and TypeScript
- Implemented dynamic field selector for category switching
- Created reusable components for consistent design system
- Formatted data on frontend (company names, city capitalization)

### Visualization
- **Interactive county heatmap:** D3.js + TopoJSON for Michigan geography
- **Multi-line trend charts:** Recharts for subcategory performance over 30 days
- **Statistical cards:** Real-time metrics with percentage changes
- **Bar charts:** Top cities and companies with proportional scaling
- **Donut chart:** Employment type distribution

---

## 🔍 Analysis

### Key Metrics Tracked:
- Total active job postings with 30-day growth percentage
- Number of unique companies hiring per sector
- Top hiring cities and counties with geographic visualization
- Top 5 in-demand skills/subcategories per field
- Employment type breakdown (Full-Time, Part-Time, Contract, Internship)

### Insights Generated:
- Identified Tech sector as highest growth area (1067% increase)
- Detroit, Lansing, and Ann Arbor consistently lead in job postings
- Data Science/AI and Software Engineering dominate skill demand
- 94% of postings are full-time positions
- Wayne County leads with 2000+ job postings

---

## 🔑 Key Features

- **Dynamic field filtering:** Switch between Tech, Engineering, Business, and Health
- **Interactive visualizations:** Hover states, tooltips, and county highlighting
- **Responsive design:** Optimized for desktop viewing with dark theme (#0a0a0a background)
- **Real-time data:** API routes fetch latest data on each category switch
- **Geographic insights:** Michigan county-level heatmap with 5-color gradient scale
- **Trend analysis:** 30-day historical data with 8-subcategory tracking

---

## 🛠️ Tools Used

- **Frontend:** React, Next.js 14, TypeScript
- **Styling:** Tailwind CSS, inline styles
- **Data Visualization:** Recharts, D3.js, react-simple-maps, TopoJSON
- **Database:** Supabase (PostgreSQL)
- **API:** Next.js API Routes (RESTful)
- **Deployment:** Vercel
- **Development:** VS Code, Claude AI for debugging and learning

---

## 📂 Files
```
app/
├── api/analytics/
│   ├── tech/route.ts              # Tech sector API endpoint
│   ├── engineering/route.ts       # Engineering sector API endpoint
│   ├── business/route.ts          # Business sector API endpoint
│   ├── health/route.ts            # Health sector API endpoint
│   ├── counties/route.ts          # County data aggregation
│   └── subcategory-trends/route.ts # Trend data over 30 days
├── dashboard/
│   ├── page.tsx                   # Main dashboard layout
│   ├── components/
│   │   ├── FieldSelector.tsx      # Category switcher
│   │   ├── LargeStatCard.tsx      # Metric cards
│   │   ├── TopHiringCompaniesList.tsx
│   │   ├── TopSkillsInDemand.tsx
│   │   ├── TopCitiesChart.tsx
│   │   ├── SubcategoryTrendChart.tsx
│   │   ├── JobTypeSummary.tsx
│   │   └── MichiganCountyMap.tsx  # Interactive map
│   └── data/
│       └── michiganCounties.ts    # City-to-county mappings
```

---

## 🎓 Takeaway

This project demonstrated how machine learning principles apply to real-time data pipelines and interactive dashboards. Despite being my first React/Next.js project, I successfully built a production-ready analytics platform in 2 months by:

- Leveraging AI tools (Claude) to accelerate learning and debug complex issues
- Implementing best practices for component architecture and data formatting
- Mastering new technologies: React, TypeScript, D3.js, Recharts, Supabase integration
- Designing intuitive data visualizations that communicate insights effectively
- Building scalable API architecture with normalized database schemas

**Key Learning:** Combining traditional problem-solving skills with AI-assisted development dramatically accelerates both learning and execution, enabling rapid deployment of complex full-stack applications.

---

## 🚀 Live Demo

The following link will be accessible when the Greenify website goes live. But for now, a video recording of the dashboard is available.
**Dashboard:** [View Live](https://greenify-dashboard.vercel.app)  

---

## 📧 Contact

**Amaan Thasin**  
Data Science & Information Technology  
Michigan State University '24  
📧 amaan.thasin@gmail.com
🔗 [LinkedIn](https://linkedin.com/in/amaanthasin) | [Portfolio](https://amaanthasin.com)

---

## 📝 License

MIT License - feel free to use this project for learning purposes!
