# Lumina import checklist

Run this checklist before importing the repository into a Lumina canvas.

## Package rules

- Every tracked file ends in `.md`, `.txt`, `.json`, `.yaml`, or `.yml`.
- Extensions are lowercase.
- Names use only ASCII letters, numbers, underscores, and hyphens before the extension.
- Names are at most 64 characters.
- The package contains no extensionless `LICENSE`, binary media, archives, source code, or hidden configuration files.
- Generated media is stored elsewhere and referenced by stable ID or URL.

## Content checks

- `SKILL.md` contains valid YAML frontmatter with `name` and `description`.
- `agents/openai.yaml` contains quoted interface strings.
- JSON templates parse successfully.
- YAML templates parse successfully.
- All relative Markdown links resolve.

## Import sequence

1. Choose repository import in Lumina.
2. Select this repository and the desired branch.
3. Confirm that the preview lists only supported text files.
4. If Lumina reports an unsupported file, cancel the import and remove that file from the selected source. Do not continue with a partially imported package.
5. Complete the import and open `SKILL.md` as the canvas entry document.
