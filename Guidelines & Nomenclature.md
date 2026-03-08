# Guidelines & Nomenclature

## The One Strict Rule

**One Page Only (OPO) — non-negotiable.**

Every guide **must** explain its topic **completely and self-contained** within **a single wiki page**.  
- No splitting the topic into multiple pages.  
- No making core understanding dependent on hyperlinks to other pages.  
- Hyperlinks are allowed only as optional extras (references, man pages, further reading).  

If a contribution is not OPO — **it goes straight into the garbage can**. No exceptions, no partial accepts, no "maybe later."  
This is the only hard line. Everything else is flexible.

## Handling Similar or Duplicate Content

**If a new page covers substantially the same topic as an existing one** (same core subject, overlapping steps/explanations, similar scope), **it will be merged into the preexisting page**.

- The goal is **one canonical, best-in-class page per topic** — not competing versions or fragmented alternatives.
- Merging ensures:
  - All good contributions are preserved and combined.
  - Readers always find the most complete, up-to-date, and well-refined guide in one place.
  - No dilution from redundancy across pages.
- Process:
  1. The new page (or draft) is flagged (via discussion, edit comment, or issue).
  2. Contributors/reviewers merge the best parts: unique explanations, additional edge cases, better examples, clearer steps, improved redundancy, distro variations, etc.
  3. The result is **forced to be coherent** — one unified narrative, logical flow, consistent tone/structure where possible.
  4. The duplicate page is deleted or redirected (GitHub/GitLab wikis support simple redirects via page renaming or #REDIRECT syntax if you enable it).
- If the new content is truly different enough (e.g., a narrower scope, advanced variant, or alternative approach that doesn't overlap heavily), it can stay separate — but this should be rare and discussed first.

This isn't about gatekeeping creativity; it's about **centralizing knowledge** so every topic has its definitive, scrollable masterclass.  
If you're unsure whether your page overlaps too much, start by discussing on the existing page's talk/discussion section or open an issue with links to both.

Example: Someone submits "Installing NVIDIA drivers on Fedora" when "Installing NVIDIA drivers" already exists (covering multiple distros). → Merge the Fedora-specific steps/variations into the main page under a "Fedora" subsection or table — no new page created.
## Everything Else Is Guidance, Not Rules

We promote creative expression and freedom of thought.  
Write in your own teaching style. Make the guide **you** wish you had when learning Linux.

Some suggestions to maximize clarity and usefulness (optional — adapt freely):

- Organize logically from beginning to end with clearly named major step sections  
  (e.g., Backup → Resize → Make → Format → Mount → Troubleshooting).  
- Under each section: 3–4 explanatory sentences + numbered sub-steps (Backup.1, Backup.2, …).  
- Embrace good redundancy — repeat helpful concepts inline where they aid understanding.  
- Use Markdown freely: code blocks, bold warnings, tables for comparisons, etc.  
- Add a strong intro/overview so readers know immediately if this is the right page.  
- Go as long as needed for completeness — no artificial length limit.

The goal is a scrollable, self-contained masterclass per topic.  
If your page achieves that while breaking none of the above suggestions — perfect.  
If it achieves that **and** follows some of the suggestions — even better.

Questions or edge cases? Discuss on the page itself or open an issue.

Happy writing — one page at a time. 🐧
