
DxVida helps small and medium textile businesses navigate the complexity of exporting to Germany and the EU. Instead of spending weeks researching compliance, you get answers in minutes.


- **Compliance path checker** — regulatory requirements by product category and destination market
- **Label compliance tool** — textile labeling rules per country (REACH, care labels, language requirements)
- **Business model archetypes** — find the right market entry model for your product
- **Opportunity case explorer** — real market opportunities with context
- **Photo analysis** — upload product photos for AI-assisted compliance review
- **Institution directory** — relevant authorities, certifications bodies, and support organizations
- **Multilingual** — German and English interface


---


## Built with


![Claude](https://img.shields.io/badge/Claude-AI-black?style=flat-square)
![Netlify](https://img.shields.io/badge/Netlify-Deploy-00C7B7?style=flat-square&logo=netlify&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![HTML](https://img.shields.io/badge/HTML-Single--file-E34F26?style=flat-square&logo=html5&logoColor=white)


---


## Architecture


Deliberately minimal. One HTML file + serverless functions + data modules.


```
dxvida-export-copilot/
├── index.html                    # Full app — single file
├── netlify.toml                  # Deployment config
├── data/
│   ├── compliancePaths.js        # Regulatory paths by category
│   ├── businessModelArchetypes.js # Market entry models
│   ├── opportunityCases.js       # Market opportunity data
│   ├── textileLabelCompliance.js # Label rules by country
│   ├── explorerTranslations.js   # i18n strings
│   └── institutionDirectory.js   # Authorities & bodies
└── netlify/functions/
    ├── analyze-photos.js         # Claude vision — product photo review
    ├── product-lookup.js         # AI product compliance lookup
    └── regulatory-scout.js       # Regulatory intelligence function
```


---


## Why this matters


Export compliance is genuinely hard for small businesses. The information exists but it's scattered across government websites in German, buried in EU directives, and requires a consultant to decode.


This tool is a first attempt at making that accessible — combining structured data with AI to give small textile exporters a real starting point.


---


## Status


Active. Built and deployed solo as part of ongoing AI product development work.


---


*Built by [Pri Hidalgo](https://github.com/phidalgosol-oss) · AI consultant & builder · [LinkedIn](https://linkedin.com/in/priscillahidalgo1985)*

