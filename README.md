# Kyambuthia Blog Content

This repository contains the articles and translations for [kyambuthia.com](https://kyambuthia.com). It is integrated into the main website as a Git submodule.

We welcome contributions! If you'd like to help translate an article into your language, please follow the guide below.

## Directory Structure

Articles are organized by language codes (e.g., `en/`, `sw/`, `kik/`).

```text
content/
├── en/           # English (Source)
├── sw/           # Swahili
├── kik/          # Gikuyu
└── README.md
```

## How to Contribute a Translation

### 1. Find the Article
Navigate to the `en/` folder to find the source article you want to translate.

### 2. Create the Language Folder
If your language doesn't have a folder yet, create one using its standard ISO 639-1 code (e.g., `fr` for French, `es` for Spanish).

### 3. Create the Translated File
Copy the `.mdx` file from the `en/` folder into your language folder. **Keep the filename exactly the same** (this preserves the URL slug across languages).

### 4. Update the Metadata
Each file starts with an `export const metadata` block. You **must** translate the `title` and `description` fields.

```javascript
export const metadata = {
    title: "Translated Title Here",
    date: "2025-01-12", // Keep the original date
    category: "devlog", // Keep the original category
    description: "Brief summary in your language"
}
```

### 5. Translate the Content
Translate the MDX content below the metadata block. You can use standard Markdown as well as React components if available (standard MDX).

### 6. Submit a Pull Request
Once you're done, submit a Pull Request to this repository. After review and merge, the changes will be automatically deployed to the main website.

---

*Note for Maintainers: The main website uses a build script to generate a `posts-registry.json` based on the folder structure and metadata found in this repository.*
