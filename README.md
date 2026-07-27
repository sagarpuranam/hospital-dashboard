# 🏥 MediCore — Hospital Management Dashboard

A single-file, front-end hospital management dashboard built with plain HTML, CSS, and JavaScript. No build step, no dependencies to install, no backend required — clone it and open it in a browser.

![status](https://img.shields.io/badge/status-demo-blue) ![stack](https://img.shields.io/badge/stack-HTML%20%2F%20CSS%20%2F%20JS-informational) ![license](https://img.shields.io/badge/license-MIT-green) ![PRs](https://img.shields.io/badge/PRs-welcome-brightgreen)

## Contents

- [Features](#features)
- [Getting started](#getting-started)
- [Project structure](#project-structure)
- [Customizing](#customizing)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)

## Features

| Module | What it does |
|---|---|
| **Dashboard** | Live stat cards (patients, doctors, appointments, revenue), recent patients, today's schedule, and bed occupancy bars |
| **Patients** | Search, filter by status, sortable columns, add new patients via modal, inline status updates, delete records |
| **Doctors** | Staff directory with specialty, department, and workload |
| **Appointments** | Schedule new appointments, view and cancel existing ones |
| **Billing** | Collected / pending / overdue summary with an invoice table |
| **Departments** | Staff and patient counts per department |
| **Reports** | Auto-generated summary from current data |

Also included: a responsive layout with a collapsible sidebar on mobile, keyboard-accessible modals, and toast notifications for add/remove/update actions.

All data is in-memory demo data defined at the top of the `<script>` block — nothing persists after a page refresh, and there is no backend or database.

## Getting started

Clone the repo and open the file directly — that's the entire setup:

```bash
git clone https://github.com/<your-username>/hospital-dashboard.git
cd hospital-dashboard
open hospital-dashboard.html   # macOS
# Windows: start hospital-dashboard.html
# Linux:   xdg-open hospital-dashboard.html
```

No install, no server, no build process. If you'd rather not use the command line, just double-click the file or drag it into a browser tab.

**Prefer a local server?** (useful if you later add `fetch()` calls that don't work over `file://`)

```bash
python3 -m http.server 8000
# then visit http://localhost:8000/hospital-dashboard.html
```

## Project structure

```
hospital-dashboard/
├── hospital-dashboard.html   # entire app — markup, styles, and JS in one file
└── README.md
```

## Customizing

- **Sample data** — edit the `patients`, `doctors`, `appointments`, `billing`, and `departments` arrays near the top of the `<script>` section.
- **Colors / theme** — CSS custom properties live in `:root` at the top of the `<style>` block; change one variable to re-theme the whole app.
- **Connecting a real backend** — swap the in-memory arrays and the render functions' data sources for `fetch()` calls to your API. Rendering and event handling are already separated from the data, so this is a fairly contained change.

## Roadmap

Ideas for anyone who wants to extend this:

- [ ] Persist data with `localStorage` or a real backend/database
- [ ] Authentication and role-based views (admin, doctor, receptionist)
- [ ] Export patient/billing records to CSV or PDF
- [ ] Charting for trends (admissions over time, revenue by department)
- [ ] Dark mode

Contributions toward any of these are welcome — see below.

## Contributing

Issues and pull requests are welcome. If you're proposing a larger change, opening an issue first to discuss it is appreciated.

1. Fork the repo
2. Create a branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m "Add your feature"`)
4. Push to your fork and open a PR

## License

[MIT](LICENSE) — free to use, modify, and distribute. Add a `LICENSE` file to the repo root if GitHub didn't generate one for you.
