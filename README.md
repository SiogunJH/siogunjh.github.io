# Jakub Hojda Portfolio (GitHub Pages + Jekyll)

Data-driven portfolio site for projects, skills, profile details, and code gists.

## Structure

- `_data/profile.yml` - personal info and external links
- `_data/experience.yml` - professional experience timeline
- `_data/education.yml` - education timeline
- `_data/skills.yml` - grouped skill sets
- `_data/projects.yml` - commercial, personal, and technical projects
- `_data/gists.yml` - gist entries with descriptions and links
- `_includes/` - reusable components (cards, hero, timeline, navigation)
- `_layouts/` - base page layouts
- `assets/css/main.scss` - visual design tokens and component styles
- `.github/workflows/pages.yml` - automatic GitHub Pages deploy

## Local development

1. Install Ruby and Bundler.
2. Install dependencies:
   ```bash
   bundle install
   ```
3. Run local server:
   ```bash
   bundle exec jekyll serve
   ```
4. Open `http://127.0.0.1:4000`.

## How to update content

### Add a project

1. Open `_data/projects.yml`.
2. Duplicate an existing project block.
3. Update:
   - `title`, `type`, `status`, `role`, `summary`
   - `highlights`, `tech_stack`, `platforms`
   - optional `links`

### Add or update skills

1. Open `_data/skills.yml`.
2. Add a new item under an existing category or create a new category.
3. Use `name` and `level` for each skill.

### Add a gist entry

1. Create or copy your gist URL.
2. Open `_data/gists.yml`.
3. Add a new item with:
   - `title`
   - `description`
   - `language`
   - `tags`
   - `gist_url`
4. Keep `repository_url` for profile fallback.

## Deployment

Deployment is automatic through GitHub Actions on push to `main`.

If this is the first deploy:
1. In repository settings, open **Pages**.
2. Set source to **GitHub Actions**.
3. Push changes to `main`.

