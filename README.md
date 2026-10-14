# GEK CBT AI Online

This project packages the GEK CBT front end and a server-side AI grading endpoint. Written answers are sent only when the learner presses **AI grade matching, blanks & short notes**. The OpenAI API key is stored as a server environment variable and is never embedded in the browser code.

## Deploy to Vercel

1. Create a GitHub repository and upload the contents of this folder (not the folder wrapper itself).
2. Import that repository at https://vercel.com/ and deploy it as a project.
3. In Vercel Project → Settings → Environment Variables, add:
   - `OPENAI_API_KEY` = your OpenAI API key
   - optional `OPENAI_MODEL` = `gpt-4.1-mini`
4. Redeploy after adding the environment variables.
5. Open the deployed URL and test a short-note answer.

## Important

- This package is deploy-ready but is **not itself a live public website** until you deploy it to a hosting account and configure a valid API key.
- OpenAI API usage is billed separately from a ChatGPT subscription. Set usage limits/budget alerts in your API account.
- Do not put the API key in `public/index.html` or share it with students.
- Written answers are submitted to the AI provider for marking. Avoid sending personal/confidential information.
- Source banks sometimes lack extracted answer keys for written questions. In those cases the marker identifies that it used general marine-engineering knowledge instead of claiming it used the source answer key.
- This prototype does not include user accounts, saved cross-device history, or production-grade abuse protection. Add authentication/rate limiting before public high-traffic use.
