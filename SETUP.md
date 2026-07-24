# Setup guide

This package is designed for the GitHub profile repository:

`Krushang1818/Krushang1818`

## 1. Copy the files

Copy this complete structure into the repository root:

```text
Krushang1818/
|-- README.md
|-- assets/
|   |-- ai-chess-banner.svg
|   `-- footer-wave.svg
`-- .github/
    `-- workflows/
        |-- snake.yml
        `-- profile-3d.yml
```

The generated `profile-3d-contrib/` folder will appear automatically after the 3D workflow runs.

## 2. Commit and push

```bash
git add README.md assets .github/workflows
git commit -m "feat: redesign animated profile README"
git push origin main
```

## 3. Run both generators once

Open the repository's **Actions** tab and manually run:

1. `Generate contribution snake`
2. `Generate 3D contribution calendar`

The snake workflow creates an orphan branch named `output`. The 3D workflow creates and commits the `profile-3d-contrib/` folder on `main`.

## 4. If an Action cannot push

Open:

`Settings -> Actions -> General -> Workflow permissions`

Choose **Read and write permissions**, save, and run the failed workflow again. The workflow files already request `contents: write`.

## 5. Customize the copy

Edit the `SYSTEM PROFILE` Python block in `README.md` whenever your focus changes. Replace or add project cards using this pattern:

```html
<a href="https://github.com/Krushang1818/REPOSITORY_NAME">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=Krushang1818&amp;repo=REPOSITORY_NAME&amp;theme=tokyonight&amp;hide_border=true&amp;bg_color=00000000" alt="Repository card" />
</a>
```

## Notes

- GitHub profile READMEs do not run arbitrary JavaScript or page-level custom CSS.
- The custom hero and footer use self-contained SVG animation, so they stay in your repository.
- The contribution snake and 3D calendar are regenerated daily by GitHub Actions.
- Several stats cards use public third-party endpoints. The profile still works if one of those services has temporary downtime; only that card will be unavailable.
