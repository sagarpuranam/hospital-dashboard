# MediCore — Hospital Management Dashboard

A single-file, front-end hospital management dashboard built with plain HTML, CSS, and JavaScript. No build step, no dependencies to install — just open it in a browser.

![status](https://img.shields.io/badge/status-demo-blue) ![type](https://img.shields.io/badge/stack-HTML%20%2F%20CSS%20%2F%20JS-informational)

## Features

- **Dashboard** — live stat cards (patients, doctors, appointments, revenue), recent patients, today's schedule, and bed occupancy bars
- **Patients** — search, filter by status, sortable columns, add new patients via modal, inline status updates, delete records
- **Doctors** — staff directory with specialty, department, and workload
- **Appointments** — schedule new appointments, view/cancel existing ones
- **Billing** — collected / pending / overdue summary with an invoice table
- **Departments** — quick overview of staff and patient counts per department
- **Reports** — auto-generated summary from current data
- Responsive layout with a collapsible sidebar on mobile
- Toast notifications for actions (add/remove/update)

All data is in-memory demo data defined at the top of the `<script>` block — nothing persists after a page refresh, and there is no backend.

## Getting started

Clone the repo and open the file directly in a browser:

```bash
git clone https://github.com/<your-username>/hospital-dashboard.git
cd hospital-dashboard
open hospital-dashboard.html   # macOS
# or just double-click the file / drag it into a browser tab
```

No installation, server, or build process required.

## Project structure

```
hospital-dashboard/
├── hospital-dashboard.html   # entire app: markup, styles, and JS in one file
└── README.md
```

## Customizing

- **Sample data** — edit the `patients`, `doctors`, `appointments`, `billing`, and `departments` arrays near the top of the `<script>` section.
- **Colors / theme** — CSS custom properties are defined in `:root` at the top of the `<style>` block.
- **Connecting a real backend** — replace the in-memory arrays and the render functions' data sources with `fetch()` calls to your API; the render/event-handling logic is already separated from the data so this is a relatively contained change.

## License

Add a license of your choice (e.g. MIT) if you plan to share or reuse this publicly.
