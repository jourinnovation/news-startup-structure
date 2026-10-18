# Which News Startup Structure Is Your Team?

A Buzzfeed-style team quiz for **JOUR 3385: Media Innovation & Entrepreneurship** at Cal Poly San Luis Obispo. Student teams answer ten questions about their news venture and find out whether it fits best as a nonprofit, a for-profit, or a project that should keep testing before choosing a legal structure.

The quiz is based on Jo Ellen Green Kaiser's article [“Nonprofit or for-profit — which model is right for your news organization?”](https://medium.com/lion-publishers/nonprofit-or-for-profit-which-model-is-right-for-your-news-organization-ad57b72fe7d3) (LION Publishers, 2021).

## Learning goal

Students should be able to explain how a news venture's legal structure affects control, accountability, funding, political activity and the option to sell, and to defend a structure choice for their own project. No result is “correct.” What matters is the quality of the team's reasoning about its result.

## How to play (about 10–15 minutes)

1. **Gather around one screen.** One device per team works best.
2. **Enter a team or venture name** and start the quiz.
3. **Discuss each question before answering.** Every question includes a “Talk it over” prompt. Teams can tap an answer or press A–D or 1–4 on the keyboard.
4. **Read the note from the reading.** After each answer, a short explanation connects the question to the article.
5. **Get your result.** Teams see one of three types, along with their percentage mix across all three:
   - **The Public Trust:** nonprofit (501(c)(3))
   - **The Independent Owner:** for-profit (LLC, co-op, PBC and others)
   - **The Test Kitchen:** keep testing, for example under a fiscal sponsor
6. **Respond to the result.** In the “Do you buy it?” section, teams say whether they agree, then write:
   - one reason the result fits their venture
   - one thing the structure would make harder
   - one fact they need to verify
7. **Submit.** Teams can print or save as PDF, download a text file, or copy their response to paste into Canvas.

## Suggested assessment

Grade the written response, not the quiz result. A strong response:

- **uses the reading,** pointing to a specific rule or tradeoff from the article
- **fits the team's actual project,** referring to its audience, revenue model or team
- **names a real tradeoff** of the chosen structure
- **identifies something to verify,** such as a rule, cost, eligibility requirement or assumption

A team that disagrees with its result can earn full credit if it explains why.

## Hosting on GitHub Pages

The quiz is a single, self-contained `index.html` file with no external libraries, fonts or images.

1. Create a new GitHub repository and upload `index.html` and this `README.md`.
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, and save.
4. After a minute or two, the quiz will be live at `https://<your-username>.github.io/<repository-name>/`.

You can also open `index.html` directly in a browser without hosting it.

## Data and privacy

The quiz has no backend and sends no data anywhere. A team's answers and written responses are saved only in that browser's local storage, so a page refresh won't lose work. **Start over** in the header clears everything. Students should download or print their response before closing a shared or lab computer.

## Customizing the quiz

All content lives in the `<script>` section of `index.html`.

- **Questions** are in the `Q` array. Each question has:
  - `q`: the question
  - `talk`: the discussion prompt
  - `a`: a list of answers, each paired with point weights such as `{N:2}` or `{N:1, F:1}`
  - `why`: the note from the reading shown after answering
- **Result types** are in the `TYPES` object, keyed `N` (nonprofit), `F` (for-profit) and `T` (keep testing). Each type has a name, emoji, description, gains, tradeoffs, a real-world example and questions to verify.
- **Scoring:** each answer adds its weights to the matching types. The type with the most points is the result. Ties go to the Test Kitchen first. If the top two types are within two points, the result page flags a “close call.”
- **Colors** are CSS variables at the top of the `<style>` section and use Cal Poly green (`#154734`) and gold (`#BD8B13`).

If you change questions or answers after students have started, ask them to click **Start over** so old saved answers don't carry into the new version.

## Accessibility

- Answers work as a keyboard-accessible radio group, with letter and number shortcuts.
- Focus moves to each new question and to the result heading.
- The layout adapts to phones and narrow screens.
- Animations are turned off for users who have reduced motion enabled.

## A note on currency

The source article was published in 2021. Specifics such as the IRS's historical 20% advertising rule of thumb and typical fiscal sponsor fees (5–10% or more) may have changed. The quiz presents them as facts to verify, which makes them good material for the “one fact we need to verify” prompt.

## Credits

Created by Kim Bisheff for JOUR 3385, Cal Poly San Luis Obispo. Content is adapted and paraphrased from Jo Ellen Green Kaiser's article for LION Publishers. Examples cited in the quiz (Block Club Chicago, The PLUG, IndyWeek and Detour Media) come from that article.
