# Contributing

Ideas, bug reports and pull requests are welcome.

- **Better research or writing rules?** Edit `seo-research-content-system/SKILL.md`. Keep rules specific and checkable ("answer the main question in the first paragraph"), and only add claims you can back up.
- **Changed the input logic?** Update Step 0 in `SKILL.md`, the matching block in `prompt/universal-seo-content-prompt.md`, and the Inputs section of the README so all three agree.
- **New template field?** Add it to `templates/project-brief.md` or `templates/content-task.md` and say in Step 0 whether it's critical, derived or never invented.
- **Skill misbehaving?** Open an issue with the request you typed, what you expected, and the part of the output that went wrong (anonymise client details).

After editing `SKILL.md`, rebuild the package so the download matches:

```bash
zip -r seo-research-content-system.skill seo-research-content-system
```

Please never commit real client briefs, drafts or reports. The `.gitignore` keeps common report files out for that reason.
