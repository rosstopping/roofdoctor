# Copilot website build

Create a production-quality marketing website for **Roof Doctor**, operating in the **Roofing** sector.

## Business brief

Doncaster roofers who take pride in the job
We're a local Doncaster roofing team with the knowledge and skill to take care of every kind of roofing job, from a quick repair to a complete new roof. We work right across Doncaster and South Yorkshire for homeowners and businesses alike.

We take real pride in the quality of our work and in leaving every site clean and tidy. A lot of our work comes from repeat customers and recommendations, which we think says everything about the service we give.

No pushy sales and no nasty surprises, just honest advice, fair prices and roofs that last. If you're after a quote from roofers who'll do the job properly, we'd love to hear from you.

Required pages: Home, About, Services, Contact.

## Understand the business before designing

Before designing or writing code, determine from the supplied brief:

- what industry the business actually operates in within the Roofing sector
- who the likely customer is
- what the visitor is trying to accomplish
- whether the decision is urgent, considered, high-value, repeat, luxury, specialist, local, or another relevant buying mode
- what creates trust in this specific industry
- the likely market positioning: budget, mainstream, premium, specialist, local, established, or similar
- the most appropriate visual language for this business rather than for websites in general

Then establish an internal design direction and use it consistently throughout the build. This design direction should cover:

- overall visual personality
- colour treatment
- typography style
- layout density
- border radius and shape language
- photography style
- appropriate use of icons
- CTA hierarchy
- trust signals
- content hierarchy
- navigation style
- animation and motion level
- section structure
- mobile conversion behaviour

Different industries should produce noticeably different websites. Use the business and customer context to choose the right direction. Practical trades, hospitality, SaaS, and professional services should not converge on the same look, structure, copy style, or conversion strategy.

## Copy, content, and imagery

- Plan the page and section hierarchy around real customer intent. Help visitors understand whether they are in the right place, whether this business offers what they need, whether it serves their location or situation, why it can be trusted, what evidence exists, what the process looks like, and how to contact, book, buy, or request a quote. Adjust the order based on the industry.
- Write useful British-English copy based only on the supplied brief. Match the tone to the business and industry. Avoid generic AI phrasing, inflated claims, and unnecessarily poetic language when the business would be better served by straightforward, specific copy.
- Prioritise evidence over marketing fluff. Where the brief genuinely provides them, prominently use project photography, testimonials, reviews, years established, guarantees, accreditations, awards, case studies, customer logos, before-and-after imagery, team photography, locations served, statistics, or qualifications.
- Never invent awards, certifications, locations, people, prices, statistics, testimonials, clients, guarantees, accreditations, or any other trust signals that were not supplied.
- When imagery is available, favour imagery that evidences the actual product, service, place, team, or result. Avoid decorative stock-style imagery when more meaningful imagery is available.
- Every requested page must have substantial, differentiated content and a clear conversion path.

## Avoid generic defaults

- Do not default to a generic "modern website" aesthetic or a generic SaaS landing page unless the business genuinely calls for it.
- Only use rounded cards, large border radiuses, pill-shaped UI, gradients, glassmorphism, floating decorative cards, abstract blobs or shapes, generic icon grids, oversized whitespace, repeated three-column feature grids, repeated eyebrow-plus-heading section formulas, or heavy animation when they clearly support the chosen design direction.
- Do not place every section inside a card or container by default.
- Do not rely on generic startup layouts for non-technology businesses.
- Use industry-appropriate design cues, trust mechanisms, and conversion patterns rather than one reusable visual formula.

## Required implementation

- Keep Eleventy as the static-site generator and Tailwind CSS v4 as the styling system.
- Use the existing CSS-first Tailwind setup with `@import "tailwindcss"`; do not add a legacy `tailwind.config.js` or deprecated v3 utilities.
- Build reusable Nunjucks layouts/components and data-driven navigation. Use clean semantic HTML.
- Make the result responsive from small phones through large screens, keyboard accessible, WCAG-conscious, and respectful of reduced-motion preferences.
- Add unique page titles, meta descriptions, canonical-ready URLs, Open Graph metadata, favicon treatment, and appropriate structured data supported by the brief.
- Optimise image dimensions/loading and avoid layout shift. Use properly licensed remote imagery only when the source and licence are clear; otherwise use art-directed CSS/SVG treatments.

## Lead form — mandatory

The Contact page must contain this functional form contract exactly:

```html
<form method="POST" action="https://sitewell.digizu.co.uk/submit">
  <input type="hidden" name="_form_name" value="Contact form">
  <div class="..." style="position:absolute;left:-9999px;width:1px;height:1px;overflow:hidden" aria-hidden="true">
    <label>Leave this field empty<input type="text" name="_honeypot" tabindex="-1" autocomplete="off"></label>
  </div>
  <label>Name<input type="text" name="name" required></label>
  <label>Email<input type="email" name="email" required></label>
  <label>Message<textarea name="message" required></textarea></label>
  <button type="submit">Send enquiry</button>
</form>
```

The fields may be visually composed with Tailwind classes, but do not change the action, method, hidden field, honeypot name, or public field names.

## Final design sanity check

Before finalising the implementation, ask:

1. If the company name and copy were swapped out, could this exact design plausibly be reused for a completely unrelated industry? If yes, the design direction is too generic and should be reconsidered.
2. Does a visitor get a strong sense of what kind of business this is before reading much of the copy? The answer should ideally be yes.

## Completion checklist

1. Implement every requested page and all shared components.
2. Run `npm install`, `npm run build`, and `npm run check`.
3. Resolve all build errors, broken internal links, missing assets, overflow, and obvious accessibility issues.
4. Keep generated `_site` output uncommitted.
5. Open a pull request summarising the design direction, page structure, form integration, and verification performed.