# NemoClaw Biohacking — demo screenshots

These are browser captures of the project's existing dashboard running locally with its bundled synthetic demonstration data. They can accompany the public `nemoclaw-biohacking-showcase` repository while the implementation remains private.

**Status: under active development and testing.** Every image is labelled **Synthetic demo · Local calendar preview**.

## What these captures demonstrate

- The actual saved dashboard and Python broker running together locally.
- A 32-day synthetic HRV and resting-heart-rate history, with calculations performed by the project's deterministic code.
- Missing sleep and step measurements displayed as **Unknown**.
- A non-diagnostic recovery alert and task planning within configured limits.
- Six fabricated specialist proposals from the bundled demo, including three expanded recommendations.
- The check-in form and the dashboard's responsive mobile layout.

The demo did not call an LLM, connect a wearable, write to Google Calendar, or run the NemoClaw/OpenClaw/OpenShell agent stack. These captures demonstrate the local dashboard and demo flow; live integration and deployment validation remain separate. The recommendations shown are fabricated demo proposals, not personal advice or live agent outputs. The blank check-in form is shown without submitting a check-in.

Synthetic measurements and the demonstration clock are dated **2026-10-06**. No real health records, credentials, source code, full prompts, or database files are included in this pack. Small synthetic-demo labels were added only in the capture session; the underlying project files were not redesigned or changed.

## Use on GitHub

1. Extract this ZIP.
2. Copy the `assets/screenshots/` folder into your public showcase repository.
3. Add this `SCREENSHOTS.md` beside your showcase's `README.md`, or copy the image links and captions below into that README. Keep the synthetic-demo labels and context.
4. Upload and commit those files. This pack does not need your private project's source code or Git history.

## Dashboard overview

![NemoClaw Biohacking dashboard showing synthetic HRV and resting heart rate, unknown sleep and step measurements, a trend chart, and a non-diagnostic recovery alert.](assets/screenshots/01-dashboard-overview.png)

Synthetic-data dashboard: measured values, missing-data visibility, a 32-day trend, and a recovery alert. Calendar actions remain in local preview mode.

## Activity planning

![Six demonstration activities, with four in preview and two deferred because of the daily limit.](assets/screenshots/02-activity-planning.png)

Four activities are accepted into the local preview. Two are deferred by the daily limit. No external calendar events were created.

## Specialist recommendations

![Six fabricated specialist proposals with circadian optimizer, inner compass, and sleep guardian expanded.](assets/screenshots/03-specialist-recommendations.png)

The selected demo specialists retain individual recommendations and uncertainty text. Three proposals are expanded here. No LLM was called to produce these fixtures.

## Check-in form

![Blank optional stress and wellbeing check-in form in the local demo dashboard.](assets/screenshots/04-check-in.png)

Optional self-reported stress, wellbeing flags, and notes. This image shows the form; no personal check-in was entered or submitted.

## Mobile overview

![Mobile-sized dashboard showing the same synthetic measurements and unknown sleep and step measurements.](assets/screenshots/05-mobile-overview.png)

The existing responsive interface captured at a mobile-sized viewport. This is browser viewport emulation, not a photograph or a test on a physical phone.
