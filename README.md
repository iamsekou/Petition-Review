# Petition Review Flags

> **PROTOTYPE. Class demo, not an official court website.** CS4535 Team 4. Not affiliated with or endorsed by any court. Don't enter real personal or case information. Nothing is saved or filed.

CS4535 Team 4 prototype for Indiana's Protection Order E-filing Service. The look (colors, fonts, layout) follows the Indiana courts self-service pages so the demo feels familiar. It uses no seal or logo, and a prototype warning appears at the top of the page and in every section. See [FEEDBACK.md](FEEDBACK.md) for what we changed after Shark Tank feedback.

- **Petitioner preview:** neutral "Before you sign" notes (missing dates/places, single-incident stalking petitions, possible confidential info in public fields). Filing is never blocked.
- **Court staff queue:** petitions listed in the order received, with petitioner-reported safety flags and completeness flags. No scoring or ranking.
- **Filing walkthrough (`filing.html`):** a demo that follows the question order of Indiana's PO-0100 petition, with our safety questions and "Check before you sign" step added before signing. It has its own styling (not the state's), a warning on every screen, and no real submission.
- **PO-0100 with your answers (PDF):** on the last step of the walkthrough, "Download PO-0100 with my answers" writes the answers onto the court's own form, `forms/PO-0100.pdf` (Office of Judicial Administration, rev. 07/2026, from [in.gov/courts/iocs/publications/po-forms](https://www.in.gov/courts/iocs/publications/po-forms/)). The form has no fillable fields, so the answers and X marks are drawn at positions measured from that exact file with [pdf-lib](https://github.com/Hopding/pdf-lib) (pinned, loaded from cdnjs with an integrity hash). It all happens in the browser, so nothing is uploaded. Anything that doesn't fit (a 4th incident, a long description, a long case list) goes on an attachment page and the form's "Continued on Attachment" box and page count are filled in. Names, address, case number and signature are left blank on purpose, and a small note in the top margin of every page says it was prepared with a class prototype. Safety answers are never included. If the court revises PO-0100, the positions in `POS` in `filing.html` need re-measuring. If the form can't be loaded (for example when the page is opened as a saved file), it falls back to a plain practice copy made with [jsPDF](https://github.com/parallax/jsPDF).

Open `index.html` in a browser, or view it on GitHub Pages once enabled.

**DEMO ONLY.** This is a class prototype, not an official court site, and not legal advice. Nothing is filed. To get a real protection order, see https://www.in.gov/courts/selfservice/protection-orders/ or call 1-800-332-7385.
