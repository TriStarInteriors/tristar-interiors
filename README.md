# TriStar Zoho Jobs Build

This repository is the working plan and code library for rebuilding TriStar's job workflow in Zoho One.

The goal is to create a simple operational system first:

Lead -> Job -> Job Components -> COGS -> Install Status -> Invoice

Do not try to rebuild every Odoo feature at once. Build the core workflow, test it with real jobs, then add automation.

## Phase 1: Zoho Creator app

Create a Zoho Creator application named `TriStar Jobs`.

Start with two forms:

1. `Jobs`
2. `Job Components`

The `Jobs` form tracks the overall project/customer.
The `Job Components` form tracks each trade/category inside the job, such as cabinets, countertops, closets, and flooring.

## Phase 2: Flooring logic

Flooring should be treated as a job component, not as a separate disconnected app.

Each flooring component should track:

- Square feet
- Waste percent
- Carton coverage
- Cartons needed
- Cost per carton
- Material cost
- Labor rate
- Labor cost
- Trim cost
- Underlayment cost
- Demo cost
- Total COGS
- Installed status

## Phase 3: Automations

After the forms work manually, add Deluge scripts for:

- Flooring carton calculation
- Material cost calculation
- Labor cost calculation
- Gross profit and margin
- Job status updates
- CRM deal to Creator job creation
- Creator job to Books invoice creation

## Rule

Manual and correct first. Automated later.
