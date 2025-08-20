# Steal these prompts to ship better product

# Steal These Prompts: 4 AI Workflows to Help You Ship Better Products

#### Brian Balfour

Brian is the Founder and CEO of Reforge. Most recently, he was the VP of Growth @ HubSpot. Prior to HubSpot, he was an EIR @ Trinity Ventures and founder of Boundless Learning (acq by Valore) and Viximo (acq by Tapjoy). He advises companies including Blue Bottle Coffee, Gametime, Lumoid, GrabCAD, and Help Scout on growth and customer acquisition.

[Learn More](/profiles/brian-balfour)

A common complaint about AI tools is that they spit out slop, but this is mostly user error. If you want a document that looks like a product strategy, ChatGPT will create one in about 10 seconds. A PM who tells their team “build something users want” won’t get good results either. Better input yields better output.

Product managers are generally early adopters. Still, seeing how others use AI can inspire their own usage. I put together some example prompts as part of our [Spring Cohort](https://www.reforge.com/learning) that I’ll share here today. They will help you:

-   Create a feature taxonomy for your own product or a competitor’s.
-   Turn a product strategy into a compelling narrative to sell your vision.
-   Frame every [PRD](https://www.reforge.com/blog/evolving-product-requirement-documents) within the context of that strategy.
-   Evaluate your PRDs from a CPO’s perspective

I put together example inputs and outputs for each as well, so you can see how they work and adapt as needed for your own work.

## The formula for great AI workflows

Stepping back just briefly, my hope is that you can use these prompts right away, but also that they encourage you to think more deeply about how to use AI in your work. There’s a framework I used to create each of these that can help you find new ways to use AI.

-   **First, you need to understand AI’s capabilities.** This is always changing (and improving) and you have to use lots of tools to understand AI’s current strengths and weaknesses. We’ll use a handful of different tools to run the prompts below based on the needs and constraints of each.
-   **Next is task decomposition.** When you break a task down into smaller components, it helps you think through the steps and it’ll help you get much better outputs from AI. In general, the bigger the task, the more generic the output will be. And the more narrow the task, the more specific the output will be. As an example, you should separate the creation of PRD from the evaluation of it. The first part requires creativity and narrative. The second part requires critical analysis. Combining this into a single workflow would water down the results.
-   **And lastly, bring conviction, opinions, subject matter expertise, data and non-consensus thinking.** You have to fuel the workflow with your own insights to get good results. This is where AI really shines—helping you turn your ideas into something tangible you can advocate for, build and sell. (How you find those unique insights is outside the scope of this article but we have a course on it called [Mastering Product Management](https://www.reforge.com/programs/mastering-product-management-eg/preview/material).)

With that foundation in mind, let’s get into a few prompts that can help you in some of the important work you do as a PM.

## Prompt #1: Create a feature taxonomy (from your customer’s eyes)

It’s always helpful to understand your own product from a user’s point of view. One way to do this is to create a feature taxonomy. Tools like ChatGPT or Perplexity are an easy way to start. You can just ask the AI to scrape the website and build the taxonomy. The challenge is that they’ll crawl the _marketing_ site, which will basically mirror the picture you’ve already painted. It’s helpful, but it doesn’t allow you look from the outside in.

To see what your users see, you can use a computer control model like [OpenAI Operator](https://operator.chatgpt.com/) or [Manus](https://manus.im/) to create an agent that will make an account and login to the product. I used Manus to create a feature taxonomy for Calendly to show how it works.

The full prompt is below. Replace “\[Enter site URL here\]” with the URL of the site you want to crawl. By default, Manus will create a fake email address to make an account, but this won’t work since you can’t verify the email. Instead, create a temporary, disposable email from a tool like [AdGuard](https://adguard.com/en/adguard-temp-mail/overview.html) or [Temp-Mail](https://temp-mail.org/en/) and include it in the prompt. We **do not** recommend sharing a real account with these tools.

Manus will mostly handle this on its own, but you may have to step in to handle a reCAPTCHA form. It’ll ask you to take over the screen, then it’ll pick up where it left off.

[Here’s the example output from Manus.](https://manus.im/share/file/a069f1c8-0f95-4eb7-9c38-2a6fa5d04065)

`<role>`

`Your mission: **map every customer‑facing capability of the target software product and deliver a structured feature‑taxonomy with clear descriptions and use‑cases.**`

`</role>`

`<target_product>`

`URL: [Enter site URL here] Auth: If a free trial or demo account is available, self‑register with this email address: [example@example.com]. If no trial exists, explore public marketing pages, docs, videos, and help articles.`

`</target_product>`

`<high‑level_objectives>`

`**Explore the product end‑to‑end**`

`– navigate all menus, settings, and flows a typical user can access.`

`**Capture every distinct capability**`

`– note names, UI labels, and where each feature lives in the interface.`

`**Synthesize a feature‑taxonomy**`

`– organize capabilities into a 3‑tier hierarchy:`

`* Module (top‑level area)`

`* Feature (customer‑valuable function)`

`* Sub‑feature / Action (granular tasks or settings)`

`**Describe & contextualize**`

`– for every (sub‑)feature, write:`

`* Clear 2–4‑sentence description (what it does & why it matters)`

`* Key use‑case(s) in bullet form (when a real user would rely on it)`

`Create a simple table to show the hierarchy of modules and their associated features.`

`</high‑level_objectives>`

`<detailed_instructions>`

`A. **Initial reconnaissance**`

`Land on the home page ➜ read nav labels & hero copy.`

`Crawl public pages: “Features”, “Pricing”, “Docs”, “Help Center”, “Blog”.`

`Build an initial list of modules/features mentioned.`

`B. **Hands‑on exploration (if trial/demo available)**`

`Create a trial account using the email address I provided.`

`Complete onboarding flows and note each screen.`

`Open every primary navigation item; within each, click all tabs, buttons, or expandable menus.`

`For complex widgets (dashboards, editors, builders) open tooltips, settings, and advanced menus.`

`C. **Evidence capture**`

`* For any non‑obvious feature name, hover/click tooltips and note the explanation.`

`* If a feature references an external doc page, open it and skim the first two paragraphs for intent.`

`D. **Avoid these traps**`

`* Ignore marketing hype; focus on concrete capabilities users can directly access.`

`* Do not include purely internal admin tools unless visible to standard users.`

`E. **Quality checks before finishing**`

`* Every feature must belong to exactly one module.`

`* Descriptions should start with an **active verb** (“Create…”, “Automate…”, “Visualize…”).`

`* Use‑cases use customer language (“A support manager…” not “the user”).`

`</detailed_instructions>`

`<output_format>`

`Return **one document** that includes the following:`

`* Product Name`

`* Url`

`* Table`

`* Module Name`

`* Module Description`

`* All feature names and feature descriptions that tie to that module`

`* All sub-feature names, descriptions, and use cases`

`Do that for all Modules and Features`

`</output_format>`

`<termination_condition>`

`When all primary navigation areas and linked docs have been inspected **or** 30 minutes of wall‑clock time have elapsed—whichever comes first—stop and output the taxonomy immediately`

`</termination_condition>`

You can do this for your own product, but also competitors. And once you’ve run several, you could ask AI to create a feature comparison chart to easily see how your product stacks up against the rest of the market. You can also feed this taxonomy into a product strategy, which brings us to the next prompt.

## Prompt #2: Turn a product strategy into a compelling narrative to sell your vision

Most product strategies struggle not because they're wrong, but because they're boring. In the same way your marketing and sales teams need to sell the product, you need to sell the product strategy.

This prompt will help you turn a tightly structured product strategy into a narrative that will galvanize the rest of your team around the vision. The goal here is to make easy to get buy-in for your strategy. A product strategy needs a market analysis, value-prop statement and a feature taxonomy (see above!) but this alone will not help you sell the vision.

I’ve used elements of Andy Raskin’s [strategic narrative framework](https://www.lennysnewsletter.com/p/the-power-of-strategic-narrative) to build this prompt, but there are [other narrative structures](https://www.perplexity.ai/search/can-you-find-a-few-examples-of-jntW8Uu7S_6694ERckt7MQ) you can use.

There are a few inputs you’ll need:

-   **`Product Strategy Outline` (Required):** An outline of the core components of your strategy. The problem you solve, target audience, value prop, business model, growth strategy, competitive advantage, and your core unique insight. Reforge Learning members can [get a template and see real strategy documents here](https://www.reforge.com/artifacts/c/strategy/product-strategy).
-   **`Target Audience` (Required):** Who the audience is, a description of buyers vs. end users. Provide the most detailed description possible.
-   **`Example Narratives` (Optional):** Provide example narratives that you like. This isn’t required because I find that it does an 80% job if you just give it the structure of the narrative provided in the prompt.

You can use Claude or ChatGPT to run this prompt. If you use Claude Projects then I suggest you put the below Prompt into project instructions. Put `Example Narratives` as Project Knowledge. Upload the `Product Strategy Outline` as an attachment to the chat. That way you can use the project and upload different variations of your `Product Strategy` as you iterate. You can also use the <style> section of the prompt as a custom writing style in Claude.

For OpenAI’s o1-pro or o3, you’ll need to put your `Product Strategy Outline` and `Example Narratives` directly in the prompt.

I ran a test by:

-   Creating an example product strategy outline for Calendly ([see it here](https://docs.google.com/document/d/11gEGL853M_rTW4aYs4Fp_u2AR0oMF86raKungr6zwP8/edit?usp=sharing))
-   Creating an example overview of Calendly’s target market ([see it here](https://docs.google.com/document/d/1Iz_qScAbuK7I7sr69mU-decS8PD4YQhwikTasnOW524/edit?usp=sharing))

Just a note that I don’t have any insider knowledge of Calendly and I created both of these documents using Claude.

[Here’s the output.](https://docs.google.com/document/d/1eqtk3-26V_I0Wp1p2eXaqTBDABbJeGkbcSKbHACt_zs/edit?usp=sharing)

`<role>`

`You are a veteran CEO who has built multiple billion-dollar software companies. You excel at shaping strategic vision and product strategy and telling compelling stories that inspire teams and stakeholders.`

`</role>`

`<goal>`

`I (the user) will provide you with an outline of a product strategy, data points, and thoughts for our company, [Your Company]. I want you to synthesize these into a powerful narrative to communicate the product strategy that:`

`1. **Captivates** the audience with clear headlines and memorable hooks.`

`2. **Inspires** action and alignment around our strategic direction.`

`3. **Persuades** with a confident, punchy tone.`

`4. **Follows** the structured <structure> outline below.`

`</goal>`

`<context>`

`Company: [your company]`

`Audience: [Description of your audience buyers / end users]`

`</context>`

`<structure>`

`This is the narrative structure to follow.`

`1. **Name the Undeniable Shift in the World**`

`* Identify the fundamental change shaking up our market (e.g., a technology disruption, evolving customer expectations, or industry-wide behavior shift).`

`* Clearly explain why this shift matters right now.`

`2. **Show That There Will Be Winners and Losers**`

`* Illustrate how this shift creates a divide: those who adapt (winners) and those who don’t (losers).`

`* Emphasize the urgency and importance of acting now.`

`3. **Tease the Promised Land**`

`* Describe the future state of success for those who embrace this shift.`

`* Paint a vivid, aspirational vision that resonates deeply with our customers and team.`

`4. **Introduce the Obstacles**`

`* Acknowledge the specific challenges or complexities standing in the way.`

`* Demonstrate empathy by showing you understand the audience’s struggles.`

`5. **Present Our Product as the Magic Gift**`

`* Position [Your Company] product or approach as the key enabler that helps people overcome these obstacles.`

`* Move beyond features. Instead, highlight how we facilitate real, meaningful transformation.`

`6. **Provide Proof and Evidence**`

`* Include concise customer success examples, metrics, or relevant data points that validate our strategy.`

`* Show that what we promise can — and already does — happen in the real world.`

`7. **How We Win**`

`* Explain our unique advantage: What differentiates [Your Company] from others in the market?`

`* Articulate our plan to seize this opportunity and how it drives both customer and company success.`

`8. **Call To Arms**`

`* Close with an inspiring rally cry that tells the team exactly what to do next.`

`</structure>`

`<style>`

`Follow this style and tone guidance:`

`- **Story Headlines:** Use headlines that tell a story and narrative. Do not use descriptive headlines like “How We Win” or “The Promised Land.”`

`- **Punchy**: Short, confident statements that quickly hit key points.`

`- **Persuasive**: Use language that convinces your readers emotionally and logically.`

`- **Aspirational**: Speak to our grand vision and the bigger “why,” so the team feels energized.`

`- **Clear & Structured**: Use headlines, bullet points, and crisp paragraphs. Ensure each section stands on its own.`

`</style>`

`<instructions>`

`1. Integrate the raw notes I provide, but refine them to tell a cohesive story.`

`2. Keep the narrative under a cohesive overarching theme so it reads like one flowing argument.`

`3. Remember you’re a seasoned CEO who’s done this before — let that confidence shine through.`

`4. Ensure each structured section above is distinctly addressed.`

`5. Aim for a final output that is easily shareable and can be used to rally the entire organization.`

`</instructions>`

PMs don’t always think like salespeople, but selling is a soft skill that’ll help you get buy-in and build excitement around where your product is heading.

## Prompt #3: Frame every PRD within the context of that strategy

Executive coach Patricia Fripp [says](https://fripp.com/about-patricia-fripp/frippicisms/), “It is not your customer’s job to remember you, it is your obligation and responsibility to make sure they don’t have the chance to forget you.” In this context, “customers” can be replaced with “team” and the quote holds up. Salespeople know this, PMs can learn from it.

This prompt helps you shape each new initiative within your product vision and format it in a way that makes it easy to get excited about. For this prompt, you’ll need a `product strategy document`. If you created one with the above prompt, use that one.

You’ll also need an overview of an `initiative` you are trying to communicate to your team. This can be notes on an idea, a one-page narrative, raw thoughts, a [PRD](https://www.reforge.com/blog/evolving-product-requirement-documents), etc.

Sticking with Calendly, we created a PRD for auto-blocking users’ calendars when they are out of office. (Calendly already has this feature, this is just an example.) To do it, we used our own [PRD template](https://www.reforge.com/artifacts/prd-template-from-reforge), which was created by Rula’s SVP of Product Anand Subramani and Linktree’s Chief Product Officer Jiaona Zhang. [Reforge Learning](https://www.reforge.com/learning) members can use Reforge AI to draft similar documents in the app.

[Here’s the initial PRD before we ran it through this prompt.](https://docs.google.com/document/d/1qGpdRTuC8TKpf6VCVPw-6KnbSfjhrsdexwjswxqKwF0/edit?usp=sharing)

The prompt will make sure that the initiative is closely tied to your overall strategy and craft a narrative around it. It makes it clear that your initiative isn’t just a shiny new object, but a project that will get you one step closer to achieving your strategic vision and add value to your customers. If you have KPIs, add those too and let AI connect the work back to them.

I used Claude for this example. I uploaded our `product strategy doc` and the draft `initiative`, then ran it through this prompt. I left placeholders in the prompt and recommend uploading or pasting these documents directly into the chat.

[Here’s the output.](https://docs.google.com/document/d/1sqKEfbQxXQuQcpfPemgj2L2dsIC5PFciyfqEpdhDxa0/edit?usp=sharing)

`<role>`

`You are a Staff‑level Product Manager famed for laser‑sharp strategic framing. You instinctively translate feature ideas into narratives that show exactly how they advance the broader product strategy and bottom‑line goals.`

`</role>`

`<task>`

`Using the two inputs provided below, craft a concise narrative (≈200–300 words, max 5 paragraphs) that:`

`1. Hooks the reader with the “why now” from the strategy.`

`2. Explicitly maps the initiative to the named pillars/OKRs of the strategy.`

`3. Traces a clear causal chain: *initiative ► capability ► user value ► strategic metric*.`

`4. Quantifies (or clearly qualifies) the business impact.`

`5. Ends with a crisp call to action that motivates decision‑makers.`

`</task>`

`<guidelines>`

`• Write in first‑person plural (“we”) for ownership and momentum.`

`• Use bold, punchy section headers: **Why Now?**, **Strategic Fit**, **Impact**, **Next Step**.`

`• One idea per sentence; keep jargon to a minimum.`

`• If the strategy names metrics, weave them in; otherwise, state qualitative wins.`

`• Assume the reader has 30 seconds of attention—make every line count.`

`</guidelines>`

`<format>`

`Respond **only** with the narrative described, nothing else.`

`</format>`

`<inputs>`

`PRODUCT_STRATEGY: [[ Insert the full Product Strategy here ]]`

`INITIATIVE: [[ Insert the one‑pager / PRD excerpt / feature idea here ]]`

`</inputs>`

The more you do this, the more you’ll strengthen your sales muscle. Most senior PMs will tell you that selling a narrative is at least as important (if not more) than seeing the opportunity and facilitating a solution.

## Prompt #4: Blow it up before you send it up the chain

AI tends to be sycophantic. If you aren’t careful, it’ll tell you that your product strategy is fantastic even if it objectively stinks. This prompt is about turning creativity dial way down and cranking the critical dial way up. We don’t want a “yes-man” but rather a legitimate evaluation of a PRD.

You can run this prompt in any chatbot with deep reasoning. I used Claude with “Extended Thinking” turned on. I uploaded my `product strategy document`, `initiative` and `target audience`. If you have a GTM strategy document or presentation, I recommend uploading that too.

I also uploaded a summary of Hamilton Helmer’s book, “7 Powers: The Foundations of Business Strategy,” to use as a strategic framework. ([Here is that summary if you want to use it.](https://www.perplexity.ai/search/can-you-summarize-hamilton-hel-ndF00.0ZQgG9bWR_OKAvvQ#0)) You can use this, another book like “Good Strategy, Bad Strategy” by Richard Rumelt or add notes on your own company’s overall strategic thinking.

This prompt assesses your plans with the critical eye of an experienced CPO. It’ll look at the potential second order effects of the proposed project and help you analyze the potential risks.

[Here’s the output.](https://docs.google.com/document/d/1Pm4n0APxn6Sg0ZkFTmdJDnfr5-dqVkANk59GTD2MSZw/edit?usp=sharing) Interestingly, it _despises_ the initiative. I was struck by how helpful this was, especially since AI is usually so ingratiating. I recommend reading the output to see how it evaluated the idea. Is it right? It makes good points, but I don’t recommend taking it at face value. Without more information on the product and GTM plans, there isn’t quite enough input to trust this entirely. At the very least, it’s a great sparring partner as you refine your plans.

`<role>`

`- You are a world-class Chief Product Officer with a proven track record of building multiple billion-dollar products and teams.`

`- You have deep expertise in product strategy, market analysis, and organizational leadership.`

`- You are known for your brutally honest, direct, and to-the-point feedback style.`

`</role>`

`<instructions>`

`1. Read and Understand the Provided Documentation   The user will provide a PRD, one-pager, or initiative document. Review it thoroughly.`

`2. Assess and Critique with Brutal Honesty`

`**Strategy Alignment**`

`- Identify any conflicts with the overarching product strategy, target audience, or go-to-market motion.`

`- If there is a misalignment, be explicit about how and why it occurs.`

`**Metric & Goals Tie-In**`

`- Determine whether the document clearly ties to the company’s metric goals (e.g., revenue targets, user growth, engagement).`

`- If unclear, articulate the gaps and uncertainties.`

`**Problem Definition Clarity**`

`- Assess whether the problem being solved is stated clearly and convincingly.`

`- If the problem is vague or poorly defined, call that out.`

`**Second-Order Effects**`

`- Think beyond the immediate outcome. Identify any potential ripple effects—both positive and negative—that could result from the initiative.`

`**Impact & Rationale**`

`- Explain why (or why not) this initiative will create meaningful impact for the business.`

`- If the impact is overstated or unsubstantiated, critique it.`

`**Risk Assessment**`

`- Classify the primary risks:`

`1. **Execution Risk:** Known product-market fit; success depends on strong execution.`

`2. **Market Risk:** Uncertainty around whether market demand exists.`

`3. **Product Risk:** The problem and market are known, but the product solution that will work is unclear`

`- If more than one risk applies, break them down in detail.`

`- **Asymmetric Bet Potential**`

`- Evaluate if this is a high-upside, low-downside opportunity.`

`- If the payoff is large only under specific conditions, call that out.`

`- **Big Wins Feasibility*`

`- If successful, does this initiative have the potential to become a game-changer for the company?`

`</instructions>`

`<style>`

`- **Blunt, Brutally Honest, and Direct**: Do not sugarcoat issues or observations.`

`- **Deeply Critical**: Highlight flaws, gaps, and weaknesses—along with any overlooked opportunities.`

`- **Concise & Actionable**: Provide succinct feedback but include actionable insights where relevant.`

`- **Structured Output**: Organize your response under clear headings or bullet points for each area of critique.`

`</style>`

`<output>`

`**Example Structure for Your Output:**`

`1. **Strategic Alignment**`

`2. **Metric & Goals Tie-In**`

`3. **Problem Definition**`

`4. **Second-Order Effects**`

`5. **Impact Justification**`

`6. **Risk Classification**`

`7. **Asymmetric Bet Analysis**`

`8. **Overall Verdict & Recommendations*`

`</output>`

These tools are evolving quickly, but the underlying principle of effective AI workflows won’t change. AI works best when you bring clear thinking and specific context to well-designed prompts. Start with one of these frameworks on your next strategic initiative. Tweak as needed and load each with as much context and specificity as possible.

Hopefully, this helps you improve some of your day-to-day work, but also sharpen the way you think about AI and how to best leverage it. For more, check out our courses on [AI Foundations](https://www.reforge.com/courses/ai-foundations/details) and [AI Strategy](https://www.reforge.com/courses/ai-strategy/details).

[Brian Balfour](/profiles/brian-balfour)


](/blog/crossing-the-canyon-product-manager-to-product-leader)

Explore more blog posts from top experts

[See all blog posts](/blog)
