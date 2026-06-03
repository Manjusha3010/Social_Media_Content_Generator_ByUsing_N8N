# Social Media Content Generator (n8n)

**What is this?**  
An n8n workflow that automatically creates LinkedIn posts about **Software Testing in 2026** and saves them to Google Sheets.

---

## What does it do?

1. **AI picks a topic** — e.g. Playwright, AI testing, QA trends  
2. **AI writes the post** — hook, main text, and image idea  
3. **Saves to Google Sheet** — title, content, date, status  
4. **Posts to LinkedIn** — via Upload Post integration  

![Workflow](Screenshots/image%20(1).png)

---

## What you need

- [n8n](https://n8n.io) (free or paid account)
- API keys for:
  - **OpenRouter** (topic ideas)
  - **Groq** (post writing)
  - **Google Gemini** (format output)
  - **Google Sheets** (save posts)
  - **Upload Post** (publish to LinkedIn)

---

## Quick setup (5 steps)

1. Open n8n → **Import** → choose `LinkedPostGeneration.json`
2. Add your API keys in each node (red warning icons)
3. Create a Google Sheet with columns:  
   `title | rationale | hook | status | Date | content | image_prompt`
4. Connect that sheet in the **Google Sheets** node
5. Turn the workflow **Active** → open **Chat** → send any message to run

---

## Files in this project

| File | What it is |
|------|------------|
| `LinkedPostGeneration.json` | Import this into n8n |
| `ContentGenerator.xlsx` | Example of the Google Sheet |
| `Screenshots/` | Pictures of workflow, sheet, and LinkedIn post |
| `README.md` | Full detailed documentation |

---

## How to run

- **Default:** Send a message in the n8n chat panel  
- **Optional:** Enable **Schedule Trigger** to run automatically on a timer  
- **Optional:** Enable **Generate an image** for AI images (needs OpenAI key)

---

## Example result

![Google Sheet output](Screenshots/image%20(2).png)

![LinkedIn post](Screenshots/image%20(3).png)

---

## Tips for beginners

- Start with **chat trigger** — easiest way to test  
- Check **Google Sheet** first before posting to LinkedIn  
- All credential IDs in the JSON are from the original setup — you must add your own in n8n  
- Change the AI prompts in Step 1 & Step 2 to write about other topics  

---

**Need more detail?** See [README.md](README.md)
