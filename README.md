# School Timetable Builder – AI timetable maker for ChatGPT and Claude

School Timetable Builder is a free app for **ChatGPT** and a connector (MCP server) for **Claude** that makes a complete, clash-free weekly school timetable for every class and every teacher. It is built for primary and lower-secondary schools.

ChatGPT or Claude reads your existing files (staff list, subject hours, bell times, rooms, notes), asks only what it cannot work out, and sends the data to a constraint-based timetabling engine. The engine calculates the timetable, usually in 5–8 minutes, and you get it back as a spreadsheet with one sheet per class and one per teacher.

- **Website and full documentation:** https://wilbek-source.github.io/timetable-builder/
- **Step-by-step guides with screenshots:** [How to make a school timetable with ChatGPT](https://wilbek-source.github.io/timetable-builder/how-to-make-a-school-timetable-with-chatgpt.html) · [with Claude](https://wilbek-source.github.io/timetable-builder/how-to-make-a-school-timetable-with-claude.html)
- **Video (3½ min):** https://youtu.be/QCTekFEjFBQ · **ChatGPT short:** https://youtube.com/shorts/SOAwNf_KD2U

## How to connect

**ChatGPT:** open [School Timetable Builder in ChatGPT](https://chatgpt.com/plugins/plugin_asdk_app_6ace1e8cd2e88191873b77d3de760c68) (or search for "School Timetable" under Plugins) and click Connect. Works on the free plan.

**Claude:** open [Customize → Connectors](https://claude.ai/customize/connectors), search for "School Timetable Builder" and click Connect. Or add it as a custom connector with this MCP server address:

```
https://timetable-builder.wilbek.workers.dev/mcp
```

No account, login or API key is needed. Also listed in the official MCP Registry as `io.github.wilbek-source/timetable-builder`.

## What it handles

- 5-day weeks, 1–12 lessons a day, free break times
- Teacher availability (e.g. "not after lesson 4 on Fridays", "teaches at another school on Mondays")
- Teacher workload and part-time, planning time placed with no empty gaps
- Lessons per subject and week, double lessons, min/max lessons per day, fixed teachers
- Shared special rooms, classes taught at the same time (e.g. language groups)
- Every rule is a firm rule: you get a timetable that meets all of them, or a plain explanation of what clashes

Not supported: soft "if possible" preferences weighed against each other, whole-day events, student-choice course timetables.

## Privacy

Teachers can be given by name, initials or the school's own staff codes. They are replaced with codes (T01, T02, …) in the chat before anything is sent, so the service never receives names of teachers, pupils or the school. Data is deleted within 24 hours. See the [Privacy Policy](https://wilbek-source.github.io/timetable-builder/privacy.html) and [Terms of Use](https://wilbek-source.github.io/timetable-builder/terms.html).

This repository holds the public website only. Support: timetablingengine.support@gmail.com
