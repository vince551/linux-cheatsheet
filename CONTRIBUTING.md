# Contributing to Linux Mastery

Thanks for helping improve the Linux learning hub.

## Good contributions

- Correct inaccurate commands or explanations.
- Add distribution-specific notes.
- Add safe beginner exercises.
- Improve diagrams and accessibility.
- Add troubleshooting examples.
- Improve spelling, formatting and navigation.

## Standards

1. Explain what a command does.
2. Prefer copy-safe examples.
3. Flag destructive or privileged operations.
4. Keep security examples authorized and lab-focused.
5. Prefer official documentation for external references.

## Workflow

```bash
git clone https://github.com/vince551/linux-cheatsheet.git
cd linux-cheatsheet
git switch -c docs/my-improvement
# make your changes
git add .
git commit -m "docs: improve Linux guide"
git push -u origin docs/my-improvement
```

Then open a Pull Request with a clear description of what changed and why.
