# Screenshot gallery

[Back to the project overview](../README.md)

These are captures of the existing local dashboard with synthetic measurements and fabricated demonstration proposals. **No LLM was called, no wearable was connected, and no external calendar events were created for these images.** They show local interface behavior rather than a live native-agent deployment.

Every image carries a synthetic-demo label added during capture. The demonstration date is 2026-10-06. Screenshots contain no credentials or real health records.

## Dashboard, trends, and alerts

![Dashboard with synthetic HRV and resting heart rate, unknown sleep and steps, a 32-day trend, and a recovery alert.](../assets/screenshots/01-dashboard-overview.png)

Measured values and unknown values remain distinct. The alert describes a scheduling heuristic and explicitly avoids a diagnosis.

## Activity planning

![Six demo activities: four in local preview and two deferred by the daily limit.](../assets/screenshots/02-activity-planning.png)

The planner can leave activities out of the day. The four previewed tasks have proposed times; two additional activities remain deferred. Preview is not confirmation of a real calendar event.

## Specialist recommendations

![Six fabricated specialist proposals with circadian optimizer, inner compass, and sleep guardian expanded.](../assets/screenshots/03-specialist-recommendations.png)

Selected specialists keep individual recommendations and uncertainty text. These are fixed demo proposals. Their presence does not measure model quality or show all 15 specialists running simultaneously.

## Optional check-in

![Blank optional stress and wellbeing check-in form.](../assets/screenshots/04-check-in.png)

The form accepts optional self-reported stress, wellbeing flags, and a note. This screenshot shows the blank form; it does not record a submitted check-in.

## Mobile-sized view

![Responsive mobile-sized dashboard with synthetic measurements and explicitly unknown values.](../assets/screenshots/05-mobile-overview.png)

The same interface captured at a mobile-sized browser viewport. This is viewport emulation, not a physical-device test.

For the test scope and remaining acceptance work, see [Validation](validation.md).
