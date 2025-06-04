# n8n Agents

This repository contains example n8n workflows.

## SEO Outline from SERP

File: `workflows/seo-outline-serp.json`

This workflow accepts a keyword, queries a SERP API, and uses OpenAI to return a blog outline. It exposes a POST webhook at `/webhook/seo-outline`.

### Requirements

- [Serper API](https://serper.dev/) key in the `SERPER_KEY` environment variable.
- [OpenAI API](https://platform.openai.com/) key in the `OPENAI_API_KEY` environment variable.

### Usage

1. Import the JSON file into n8n.
2. Activate the workflow.
3. Send a POST request with a JSON body:

```json
{
  "keyword": "your search term"
}
```

The workflow returns an outline generated from the SERP results.
