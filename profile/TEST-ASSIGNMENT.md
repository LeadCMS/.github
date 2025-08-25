
# LeadCMS Portfolio Website Development Assignment

Thank you for your interest in joining the LeadCMS team! This assignment will help us evaluate your skills in full-stack development, integration, and modern web tooling.

## Overview
Create a personal portfolio website that showcases your skills and projects, integrated with **LeadCMS** as the content management system. This assignment will demonstrate your ability to work with modern web technologies, design user interfaces, and integrate with external content APIs.

## Requirements

### Core Functionality
1. **LeadCMS Integration**
   - Install and run LeadCMS locally ([Docker Compose Guide](https://github.com/LeadCMS/leadcms.core/blob/develop/docker-compose/README.md))
   - Design and configure content types within LeadCMS (recommended: MDX format for landing page content, JSON format for project data)
   - Explore the [main LeadCMS repository](https://github.com/LeadCMS/leadcms.core) for additional documentation and examples
   - Fetch and display personal information from LeadCMS
   - Display a list of projects with filtering/sorting capabilities
   - Show detailed project pages with all project data (technologies, features, challenges, results, etc.)
   - Handle dynamic content updates from the CMS
   - Add at least three different content types: MDX, JSON, images
   - Reference the [sample content structure](https://github.com/LeadCMS/leadcms.ai.next/tree/main/.leadcms/content) for examples of content organization
   - Note: It's acceptable to commit dynamic content from LeadCMS to your repository for change tracking

2. **Essential Pages**
   - **Homepage**: Personal introduction, skills showcase, experience summary, list of completed projects (content managed through LeadCMS using MDX format)
   - **Project Detail**: Individual project pages with comprehensive information (content managed through LeadCMS using JSON format)

3. **Responsive Design**
   - Mobile-first approach
   - Works seamlessly across desktop, tablet, and mobile devices
   - Modern, professional aesthetic

4. **Design Approach**
   - Create your own design or use AI design tools like [v0.app](https://v0.app) or similar
   - Focus on clean, professional aesthetics and excellent user experience

### Technical Requirements

- **API Integration**: Connect to LeadCMS API for dynamic content fetching
- **Content Types**: Handle MDX (rich formatting), JSON (structured data), and images
- **Content Management**: Design appropriate content types within LeadCMS for portfolio needs
- **Reference Guide**: Use the [sample content structure](https://github.com/LeadCMS/leadcms.ai.next/tree/main/.leadcms/content) for content organization examples

### Integration Examples

To help you get started with LeadCMS integration, here are some practical examples from our existing repositories:

#### 1. **Sample Scripts and NPM Commands**
See how to set up automated content fetching in your Next.js project: [package.json example](https://github.com/LeadCMS/leadcms.ai.next/blob/main/package.json)

Key scripts that demonstrate LeadCMS integration:
```json
"scripts": {
  "fetch:leadcms": "node ./scripts/fetch-leadcms-content.mjs",
  "generate:env": "node ./scripts/generate-env-js.mjs",
  "prebuild": "npm run fetch:leadcms && npm run generate:env",
  "predev": "npm run prebuild",
  "prestart": "npm run prebuild",
  "build": "next build",
  "dev": "next dev",
  "start": "next start",
  "lint": "next lint",
  "serve": "npx serve out"
}
```

**Live Content Updates**: For development mode and live preview, you can use the [SSE watcher script](https://github.com/LeadCMS/leadcms.ai.next/blob/main/scripts/sse-watcher.mjs) to subscribe to live updates from the CMS:
```bash
node scripts/sse-watcher.mjs & npm run dev
```

#### 2. **Configuration Setup**
Example environment configuration for LeadCMS: [.env.sample](https://github.com/LeadCMS/leadcms.ai.next/blob/main/.env.sample)

This shows the configuration values needed to connect your application to LeadCMS.

#### 3. **Plugin Development**
Learn how to develop custom plugins for LeadCMS: [Plugin Integration Guide](https://github.com/LeadCMS/leadcms.core?tab=readme-ov-file#plugin-integration)

This documentation covers extending LeadCMS functionality with custom C# plugins.

### Technology Recommendations

**Recommended Stack:**
- **Frontend**: Next.js 14+ with TypeScript
- **Styling**: Tailwind CSS
- **Content**: MDX and JSON for rich content rendering
- **Additional Resources**: Check our [main repository](https://github.com/LeadCMS/leadcms.core) for more technical documentation

*Note: These are suggestions based on our testing. Feel free to use any modern web framework (React, Vue, Angular, Svelte, etc.) or even vanilla JavaScript if you prefer.*

## Bonus Points

- Dockerize your Next.js site for easy deployment
- Implement a custom LeadCMS plugin (in C#) to extend functionality
- Polish the UI/UX and demonstrate responsive design
- Deploy your website with SSL and production-ready configuration ([nginx setup guide](https://github.com/LeadCMS/leadcms.nginx) for standalone server deployment)

## Deliverables

### Primary Submission
**GitHub Repository** (Required)
- Public repository with complete source code
- Clear README with setup instructions
- Live demo link if deployed

### Optional Enhancements
- **Deployed Website**: Live website with SSL on your own domain (bonus points) - see [nginx setup guide](https://github.com/LeadCMS/leadcms.nginx) for standalone server deployment
- **Zip Package**: Alternative delivery method with detailed setup instructions

### Documentation Requirements
Include in your README:
- Project overview and features
- Technology stack used
- Setup and installation instructions
- LeadCMS integration details
- Design decisions and approach
- Any challenges faced and solutions implemented

## Questions?
If you have any questions about the assignment or need clarification on requirements, please don't hesitate to reach out at [https://leadcms.ai/contact-us](https://leadcms.ai/contact-us).

---

We look forward to seeing your work and welcoming you to the LeadCMS team!
