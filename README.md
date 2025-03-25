## Medium Blog Repository

This repository contains blog posts written in **Markdown**, which are automatically published to **Medium** using GitHub Actions and the Medium API.

## How It Works

- Blog posts are written in **Markdown** format and stored in the `posts/` directory.
- When a new post is added and pushed to GitHub, a GitHub Action is triggered.
- The action converts the Markdown file to **HTML** and publishes it to **Medium** via the Medium API.

## Writing and Publishing

1. Create a new Markdown file in the `posts/` directory:

```bash
   touch posts/my-new-blog.md
```

2. Write the content using standard Markdown formatting. Example:

# Understanding SaaS, PaaS, and IaaS

Cloud computing is categorized into three main service models: SaaS, PaaS, and IaaS...

3. Commit and push the changes:

```bash
git add .
git commit -m "Added new blog post: Understanding SaaS, PaaS, and IaaS"
git push origin main
```

4. The GitHub Action will run, and the post will be published to Medium.

## Configuration

Medium API Token

1. Generate a Medium API token from Medium Settings.
2. Add it as a GitHub Secret:
   • Navigate to GitHub Repository → Settings → Secrets → Actions
   • Click New Repository Secret
   • Set the name as MEDIUM_API_TOKEN and paste the API token as the value.

### Publishing Status

By default, posts are published as public. To change this to draft, update the .github/workflows/publish.yml file:

```bash
"publishStatus": "draft"
```

### Features

• Write blog posts in Markdown format.
• Automatically convert Markdown to HTML.
• Publish posts to Medium via the Medium API.
• Configurable publishing status (public or draft).
