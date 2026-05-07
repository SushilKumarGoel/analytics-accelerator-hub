# analytics-accelerator-hub

analytics-accelerator-hub/
├── index.html                      ← Hub landing page
├── ecc-s4-lineage.html             ← Lineage tool (fetches from CSV)
├── cds-reference.html              ← Your existing CDS app (rename your current file)
├── data/
│   ├── ecc-s4-lineage.csv          ← Data maintained in Excel, saved as CSV
│   └── cds-reference.csv           ← (Future: move CDS data here too)
├── lib/
│   └── papaparse.min.js            ← Lightweight CSV parser (5KB gzipped)
└── README.md


Team maintains in Excel          GitHub Repo              Browser
┌───────────────────┐      ┌──────────────────┐     ┌────────────────────┐
│  Excel Workbook   │      │  data/           │     │  HTML Page loads   │
│  (local machine)  │─────▶│  lineage.csv     │────▶│  fetch('data/...'  │
│                   │ save │                  │     │  parse CSV         │
│  Add/edit rows    │ as   │  Git tracked     │     │  Render table      │
│  in familiar UI   │ CSV  │  version history │     │  Filter/search     │
└───────────────────┘      └──────────────────┘     └────────────────────┘
