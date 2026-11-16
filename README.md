# Staff management iOS app

**Rotas, clock-in, holidays and compliance for a hospitality group. Live on the App Store.**

![Platform](https://img.shields.io/badge/platform-iOS%20%C2%B7%20App%20Store-0a84ff)
![Users](https://img.shields.io/badge/in%20daily%20use-15%2B%20staff-2ea043)
![Saving](https://img.shields.io/badge/replaced-%C2%A3800%2Fmonth%20platform-f78166)

- Replaced an £800/month workforce platform
- Geofenced and NFC clock-in, rotas and shift swaps
- Sold on as a white-label product

> Source is private (live business system). **[Full write-up →](https://sajjad.omni-genai.com/projects/staff-app)**

`Swift` · `SwiftUI` · `Supabase` · `PostgreSQL` · `Edge Functions` · `APNs`

<details>
<summary><b>What I built</b></summary>

- **Three roles:** staff, manager and owner, each capped at five tabs, with PIN sign-in handled on the server.
- **Clock-in:** geofenced clock-in and clock-out, plus NFC tags.
- **Rota and leave:** rota builder with push notifications, holiday accrual and approval, and shift swaps that need manager sign-off.
- **Compliance:** time-locked daily sheets, timed toilet checks and weekly cleaning checklists.
- **Stock:** cross-site transfers, plus food and drinks counts that feed the weekly report.
- **Hotel guests:** check-in and extra-night billing; bookings imported from the property system's PDF reports, with the newest report always winning.
- **Team tools:** announcements with read receipts, and a live read-only view of table orders.
- **Privacy:** pay data kept separate from general staff records.

</details>

<details>
<summary><b>Security</b></summary>

- Every user signs in to an authenticated session, with an automatic PIN re-login every 12 hours.
- Internal database functions are closed to the public.
- Guest ID photos and documents sit in private storage behind sign-in rules.

</details>

<details>
<summary><b>What went wrong on the way</b></summary>

- Push notifications failed for some staff. They were still on test builds whose tokens the live service rejects. The fix was moving them to the App Store build, not changing code.

</details>

---

Built by **[Sajjad Mahessar](https://sajjad.omni-genai.com)** · [LinkedIn](https://www.linkedin.com/in/sajjadmahessar/)
