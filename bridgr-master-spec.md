# Bridgr — Master Platform Specification
### Complete product brief for designers, developers, and AI models
**Version 1.0 — April 2026**

---

## 1. What Bridgr Is

Bridgr is a three-party matchmaking platform that connects product brands with content creators, with a monthly in-person flagship event at its centre. The platform is built specifically for skincare, health, wellness, and lifestyle brands launching or scaling in the UK market.

**The core problem it solves:**
- Brands launching products need social proof, authentic UGC, SEO-indexed content, and reliable creator partnerships — but finding vetted creators is slow, risky, and relationship-dependent.
- Creators want to discover new products early, build their portfolio with authentic content, and earn professional commission income — but most brand-creator matching is follower-count-based and transactional.

**The Bridgr difference:**
- An AI-powered intelligence engine that analyses a brand's market position before they invest in any campaign
- Editorial curation on both sides — every brand and every creator is vetted before entering the platform
- A monthly in-person event where deals happen in the room, between people who've already reviewed each other's profiles online
- A creator standing system that rewards contribution quality and category relevance, not follower count

---

## 2. The Three Parties

### Brands
Product companies launching or scaling in the UK. Typically: founders, marketing directors, or brand managers with a physical product ready to ship and a commission budget. They use Bridgr to find creators who genuinely fit their product, generate authentic reviews and UGC, and build the social proof pipeline that enables retail listings and repeat sales.

### Creators
Content creators, influencers, UGC producers, and side-income builders with at least one active social platform and a focus category. They use Bridgr to discover vetted products before they hit mainstream, earn professional commission income through affiliate deals, and build a portfolio of authentic brand partnerships.

### Platform Managers (Bridgr team)
The internal operations team who curate both sides, run the monthly event, score and rank products and creators, manage disputes, and keep the platform's quality guarantees credible. They have unredacted visibility into everything on the platform.

---

## 3. The Complete User Flow

The platform has five distinct phases. A user may enter at any point, but the canonical brand journey is linear through all five.

---

### Phase 1 — Public Landing Page

**URL:** `bridgr.co/`

**Purpose:** Convert brand founders and creators visiting for the first time.

**What it contains:**
- Hero with dual CTAs: "Launch my product" (brand) and "Find products to promote" (creator)
- Three-column platform flow: Brand journey / Manager role / Creator journey
- Monthly flagship event section — what it is, how it works, why it matters
- Brand KPI pillars: SEO presence, reviews & social proof, UGC, trust transfer, word-of-mouth cohort
- Creator value: discovery first, portfolio building, authentic conviction content
- Positioning map vs other platforms (not influencer agencies, not generic affiliate networks)
- Trust pillars: editorial curation, physical trust (in-person), AI transparency, monthly cadence
- Results section with outcome metrics
- Primary CTA: "I'm launching a product" → routes to the Brand Intelligence Planner

**Design direction:** Dark warm palette. Deep navy/charcoal background, warm cream text, amber data highlights, brand red CTAs. Fonts: Plus Jakarta Sans (body), Playfair Display (serif headlines/numbers), DM Mono (data labels and codes).

---

### Phase 2 — Brand Intelligence Planner

**URL:** `bridgr.co/planner` (public — no account required)

**Purpose:** Qualify brand intent, generate market intelligence, and use the value of the output as the conversion mechanic for account creation. The planner is free to use. Publishing the profile and exporting the report requires creating an account.

**Layout:** Three fixed panes across the full viewport height:
- Left sidebar (280px): step navigation with numbered tiles, active/done state indicators, version footer
- Centre (flexible): one step form at a time, scrollable fields, pinned progress bar + action buttons at bottom
- Right panel (420px): single accumulating Product Intelligence Profile that builds section by section as each step is analysed — never resets between steps

**The five steps:**

**Step 1 — Establish Your Market Footprint**
Inputs: Primary launch market, product category, sales channel links (one URL per row, add-more button), product description/key claims, retail price, compliance certifications (tag input: FDA, UKCA, CE, etc.), additional target markets.
Right panel sections unlocked: 01 Product (category, sub-type, price, channels, regulatory status, certification badges), 02 Market Size (market value tile, growth rate tile, channel coverage bars).

**Step 2 — Define Your Customer Profile**
Inputs: Age range (dual-handle slider — independently draggable min and max handles with live number display; typing in either number box moves the slider; quick preset pills: 18+, 18–34, 25–44, 35–54, 45+; all three controls fully bidirectional), primary gender, skin concerns/health goals (tag input), lifestyle interests (tag input), price sensitivity tier, primary purchase trigger, discovery channels (tag input).
Right panel sections unlocked: 03 Target Audience (age range, gender, price tier, trigger, addressable pool), 04 Buying Behaviour (discovery channel bars), 05 Creator Match (pool count tile, avg engagement tile, niche breakdown bars).

**Step 3 — Map Your Competitive Position**
Inputs: Product name, competitors (name or URL, up to 5, add/remove rows), primary differentiation (textarea), price positioning (select), primary competitive advantage (select).
Right panel sections unlocked: 06 Competitive Position (2×2 positioning map with plotted dots — price vs clinical authority axes; differentiation table showing each competitor's positioning and brand's edge).

**Step 4 — Define Your Go-to-Market Channels**
Inputs: Channel selection grid (TikTok Shop, Instagram/Reels, Amazon, Own Website, Retail/Pop-up, YouTube, Creator/Affiliate, Email/CRM, plus an "Other" tile that reveals a free-text input), monthly marketing budget (range slider £500–£20k with live £ display), launch timeline, primary goal, target monthly revenue.
Right panel sections unlocked: 07 Launch Plan (budget tile, ROAS estimate tile, per-channel budget allocation bars with £ amounts and ROI notes, key-value rows for timeline/revenue target).

**Step 5 — Complete Your Launch Intelligence Briefing**
Inputs: Known risks/challenges, 6-month commercial objectives, core value proposition, creator commission rate (toggle pills: 10%/15%/20%/25%/30%), trial product allocation.
Right panel sections unlocked: 08 Market Readiness (circular score ring 0–100, readiness verdict, risk/opportunity/action items colour-coded by type).
Trigger: After analysis completes (~2 seconds), the sign-up modal appears automatically.

**Right panel behaviour:** The panel is a single persistent column. Each section starts as a greyed-out placeholder with dashed border. When a step's analysis runs (after clicking "Analyse ↗"), the relevant sections shimmer-load for ~1.6 seconds then populate with structured data — key-value rows, metric tiles, animated bar charts, a positioning map, and a score ring. Sections remain visible and filled as later steps are completed. By Step 5 the full right panel is a complete product launch profile.

---

### Phase 3 — Sign-Up Conversion Modal

**Trigger:** Automatically after Step 5 analysis completes, OR by clicking "Publish Profile & Export Report →" in the right panel CTA, OR via a persistent "Preview sign-up →" button in the nav.

**Purpose:** Convert the planner user into a registered brand account, using the completed intelligence profile as the incentive.

**What the modal shows:**
- Eyebrow: "Your profile is ready"
- Headline: "Publish your product. Export your intelligence."
- Three unlock cards, each showing what account creation unlocks:
  1. 🌐 Live product profile page — "Visible to creators on Bridgr with full interaction layer" — Included
  2. 📊 Market intelligence report — "PDF export — all 8 profile sections with insights" — Included
  3. 💬 Creator signals dashboard — "Likes, comments, buy intent, collaboration requests" — Included
- Tab switcher: Create account / Log in
- Create account form: First name, Last name, Work email, Password → "Create account and publish profile →"
- Log in form: Email, Password → "Log in and continue →"
- Success state: Green check circle, "Account created!", description + "Go to profile editor →" button
- Legal: "By creating an account you agree to Bridgr's Terms of Service and Privacy Policy"

---

### Phase 4 — Product Profile Editor

**URL:** `bridgr.co/brand/product/:id/edit` (authenticated — brand role)

**Purpose:** Post-login editing environment. Pre-populated from planner data. The brand reviews, edits, and enriches each section before publishing.

**Layout:** Two panes:
- Left sidebar (260px): section navigation list with green dot indicators showing which sections are filled, profile completeness percentage bar at the bottom
- Centre (flexible): scrollable editor with collapsible sections

**Profile header (always visible at top):**
- Product images: one large main slot (180×180px) + three thumbnail slots, each clickable to upload from device with live preview on selection. Note: in production, images are auto-extracted from submitted URLs where available; upload is the fallback.
- Inline editable product name (Playfair Display, large)
- Inline editable tagline
- Price input (DM Mono, amber colour)
- Buy link input
- Category and certification badges

**Collapsible sections:**
1. Brand story & product description — full description textarea, founder note textarea
2. Key selling points — up to 5 numbered text inputs (constraint: 120 chars each forces clarity)
3. Target audience — age range, gender, skin concerns chips, lifestyle interest chips, price sensitivity, commission rate
4. Compliance & certifications — certification chips, regulatory notes (internal, not shown publicly)
5. Where to buy — primary shop link, Amazon, TikTok Shop, other channels (one per line)
6. Founder profile — name, title, short bio (max 200 chars), LinkedIn/website
7. Visibility settings — three radio options (see below)

**Visibility settings (inline + nav dropdown):**
- 🌐 Public — anyone on Bridgr or the open web can view
- 👤 Registered creators only — visible only to verified creators on platform (recommended default)
- ✉️ By invitation only — only creators with a private link can view

**Auto-save:** Fires 800ms after any input change. Shows a green toast: "Changes saved automatically."

**Nav actions:**
- Visibility pill showing current setting with colour-coded dot (green = public, amber = registered, red = invite-only)
- "Preview live page →" — opens the published profile view
- "Publish profile" — makes the page live at the selected visibility

---

### Phase 5 — Live Published Product Profile

**URL:** `bridgr.co/product/:slug` (visibility-controlled)

**Purpose:** The public-facing page that creators and visitors see. This is what the brand's market presence looks like on Bridgr. It is NOT the brand dashboard — it is the product's public identity.

**What it contains:**

**Image carousel (full-viewport width):**
- Auto-advances every 5 seconds
- Manual prev/next controls
- Dot indicators
- Images auto-extracted from submitted product URLs in production; uploaded manually in edit mode as fallback
- No AI-generated market context on this page — that stays in the brand's private intelligence report

**Product content (below carousel, max-width 720px):**
- Category and certification badges
- Product title (Playfair Display, large)
- Tagline
- Price + creator commission pill + "Buy now" button
- Key selling points (numbered cards)
- Full product description
- Target audience grid (age, price tier, skin concerns chips)
- Founder quote card with avatar
- Where to buy links (3 channels)

**TikTok-style vertical interaction bar (fixed to right edge, vertically centred):**
Five buttons stacked vertically. Each has an icon circle, a count, and a label below.

1. ❤️ **Like** — toggling on increments the counter with a slide-in animation; icon circle turns red when active; toggling off decrements
2. 💬 **Comment** — clicking slides open a comment panel from the right (340px wide); panel shows existing comments with creator name, badge, text, timestamp; a textarea at the bottom lets anyone leave a public comment; pressing Enter or the send button posts it and increments the count
3. 🛍️ **I want to buy it** — records purchase intent signal; increments count; after a short delay redirects to the product's buy link; button turns green and stays active
4. 📣 **I want to promote it** — opens a floating panel where the creator enters their handle, social link, and niche; submitting sends a collaboration signal to the brand's dashboard; button turns amber and stays active; count increments; signal count is brand-visible only
5. 💌 **Private DM** — subscription-only feature; non-subscribers see an upgrade tooltip explaining this is a Bridgr Pro feature; Pro subscribers get a private message thread with the brand not visible publicly; the button has a small amber ✦ badge to indicate it is a premium feature

**Count visibility rules:**
- Like count: public
- Comment count: public
- Buy intent count: public
- Promote count: visible to the brand only (not shown publicly)
- DM: fully private, no count shown

**AI product chatbot (floating, bottom right):**
- A robot icon button labelled "Ask about this product"
- Clicking opens a small chat window (320×400px) with a typing indicator
- The bot answers questions about ingredients, suitability, usage, price, commission, and where to buy — drawn from the product profile content
- Falls back gracefully for anything outside the product profile scope
- This is NOT a general AI assistant — it is a smart product FAQ scoped to this product only

**Edit controls (shown when logged in as the brand owner):**
- "Edit profile" button in the nav
- Visibility tag in the nav showing current setting

---

## 4. The Monthly Flagship Event

Bridgr's platform cycle is monthly. The event is the culmination of each cycle.

**What it is:** A curated in-person gathering — brands demo and pitch their products, creators trial them and agree commission deals in the room. Both sides arrive prepared because the platform has done the matching groundwork in the preceding weeks.

**The cycle stages:**
1. Submission — brands submit products to the pool
2. AI Audit — engine analyses market position, competitors, creator fit
3. Creator Feedback — creators browse pool, like/comment/score products; brands see real-time signals
4. Event Decision — brands choose Trial track (product samples only) or Featured Launch (3-min pitch + demo station + priority matching)
5. Top 10 Announcement — platform managers publish the ranked Top 10 products and Top 10 creators; simultaneous notifications to featured parties and all event attendees
6. Event Night — in-person pitching, product demos, deal room where partnerships are agreed and logged
7. Results — content goes live, affiliate links activate, commissions tracked, brand's post-event analytics populate

**Top 10 mechanics:**
- Products ranked by composite AI score + creator engagement
- Managers can reorder within 2 positions of score rank (editorial judgment allowed, manipulation prevented — system-enforced)
- Creators ranked by contribution quality and category relevance, not follower count
- Publish is irreversible; locks the list and fires simultaneous notifications

**Event night mobile view:**
- Mobile-first screen for both brands and creators attending
- Creators see their shortlisted brands with their own comment surfaced ("why I was interested")
- "Interested" button sends instant push to that brand's attendee
- In-room deal form: brand, commission rate, content commitment, confirm → both parties receive push + email immediately

---

## 5. Creator Standing System

Creators are ranked on contribution quality and relevance, not follower count.

**Two pillars (described in plain English to creators; formula and weights are never exposed):**
- Contribution quality — the depth and usefulness of feedback given to products in the pool
- Category relevance — how well the creator's content niche matches the product categories they engage with

**Tiers:** Recognised / Active / New

**What Top 10 unlocks for creators:** priority event matching, public announcement feature, first access to new brands entering the pool

**Scoring transparency rule:** every score is paired with a plain-English interpretation. The "How is this calculated?" disclosure explains the concept but never reveals the model, weights, or methodology in enough detail to be gamed.

---

## 6. Visibility & Trust Architecture

**Creator visibility levels (4):**
- Open to all — full profile, exact stats, engagement rate
- Open to brands (default) — profile visible, follower counts as ranges
- Selective — profile visible only to brands whose products the creator has engaged with
- Private — entirely invisible to brands; visible to managers only

**Brand visibility levels (4):**
- Open to all — full profile, founder info, all details
- Product only (default) — product listing visible; founder bio hidden until creator engages
- Selective — full profile visible only to Recognised-tier creators in their category
- Private — product visible in pool; brand profile hidden; contact via manager introduction only

**Comment identity:** Default anonymous (category badge only). Creator can opt-in to show their display name per comment. AI theme clusters are always aggregate — individual identity never inferrable from cluster data.

**Managers see everything** — all creator identities on all comments, exact social stats, all AI audits including competing products, full deal histories, all dispute records, the full scoring audit trail, Private creator profiles. This is the structural requirement that makes quality guarantees credible.

**What brands cannot see:**
- Creator numeric scores or rank positions (tier label only)
- Other brands' AI audit reports
- Creator identities beyond what each creator permits
- Commission amounts earned by other brands or creators
- The scoring model, weights, or methodology
- Creators marked Private

**What creators cannot see:**
- Other creators' exact scores or rank positions
- The full AI audit report brands receive
- Which creators brands have shortlisted
- Commission amounts earned by other creators
- The scoring model or methodology
- Brand profiles they don't qualify for under that brand's Selective setting

---

## 7. Messaging Rules

Brands cannot message creators cold. The inbox only becomes active once:
- A deal is confirmed on event night (both parties unlock immediately)
- A manager confirms a match pre-event (both parties unlock one introduction message)
- A creator hits "I want to promote it" on a brand's product page (brand can send one response message)

This prevents brands from flooding creators with unsolicited pitches. All conversations are tied to a specific deal or match, giving managers context if a message is flagged.

**Private DM on the product profile page** is subscription-gated (Bridgr Pro). Non-subscribers see an upgrade prompt. Messages in this channel are private and not visible in the public comment feed.

---

## 8. Data Architecture — Key Entities

**Users:** id, email, role (brand / creator / manager), created_at, visibility_level

**Brands:** id, user_id, company_name, logo_url, founder_name, founder_bio, category, website, social_links, location, vat_number, visibility_level, created_at

**Products:** id, brand_id, name, tagline, description, hero_images, selling_points (array), category, subcategory, retail_price_gbp, commission_rate_pct, target_age_min, target_age_max, target_gender, certifications, buy_link, channel_links, status (pending / approved / paused / removed), visibility_level, created_at

**Creators:** id, user_id, display_name, avatar_url, bio, categories (array, max 3), platform_links, location, content_style_tags, availability_status, visibility_level, created_at

**AI Audits:** id, product_id, cycle_id, market_score (0–100), market_value_gbp, growth_rate_pct, competitor_data (JSON), keyword_opportunities (JSON), creator_fit_by_subcategory (JSON), recommendations (array), run_at

**Cycles:** id, name, stage (submission / audit / feedback / decision / top10 / event / results), stage_dates (JSON), created_at

**Product cycle scores:** id, product_id, cycle_id, ai_score, engagement_score, composite_score, top10_eligible, top10_featured, locked_at

**Creator cycle scores:** id, creator_id, cycle_id, contribution_score, relevance_score, composite_score, tier, top10_featured

**Deals:** id, brand_id, creator_id, product_id, cycle_id, commission_rate_pct, content_commitment (JSON), agreed_at, status (pending / active / disputed / completed), affiliate_link

**Affiliate events:** id, deal_id, type (click / conversion), revenue_gbp, commission_gbp, recorded_at

**Messages:** id, deal_id (or match_id), from_user_id, to_user_id, body, sent_at, flagged

**Product reactions:** id, product_id, creator_id, type (like / score / comment), score_value, comment_text, identity_opt_in, sentiment, created_at

---

## 9. Key API Endpoints

```
AUTH
POST   /api/auth/register/brand
POST   /api/auth/register/creator
POST   /api/auth/login
POST   /api/auth/verify-email
POST   /api/auth/reset-password

BRANDS
POST   /api/brands
GET    /api/brands/:id
PATCH  /api/brands/:id
POST   /api/brands/:id/products
PATCH  /api/brands/:id/products/:pid
GET    /api/brands/:id/products/:pid/audit     (brand + manager only)
GET    /api/brands/:id/products/:pid/feedback  (visibility-filtered)
GET    /api/brands/:id/creators                (creator discovery browser)

PRODUCT PROFILE PAGE
GET    /api/products/:id/public                (visibility-filtered — public view)
POST   /api/products/:id/like                  (toggle like)
POST   /api/products/:id/comments              (post public comment)
POST   /api/products/:id/buy-intent            (record purchase intent signal)
POST   /api/products/:id/promote-intent        (record collaboration interest)
POST   /api/products/:id/dm                    (Pro subscribers only — open DM thread)
GET    /api/products/:id/chatbot               (AI Q&A scoped to product profile)

CREATORS
POST   /api/creators
GET    /api/creators/:id
PATCH  /api/creators/:id
GET    /api/creators/:id/standing
GET    /api/creators/:id/deals

PRODUCT POOL (creator-facing)
GET    /api/products                           (pool browser with filters)
POST   /api/products/:id/reactions             (like / score / comment)

SCORING (manager)
GET    /api/scores/products/:cycleId
GET    /api/scores/creators/:cycleId
POST   /api/scores/override                    (logged with required reason)
POST   /api/scores/lock/:cycleId

CYCLES & EVENTS
GET    /api/cycles/current
POST   /api/cycles/:id/top10/publish           (manager only — irreversible)
POST   /api/events/:cycleId/attend
POST   /api/events/:cycleId/checkin/:uid       (manager — event night)
POST   /api/events/:cycleId/matches            (manager only)
POST   /api/cycles/:id/close

DEALS
POST   /api/deals
POST   /api/deals/:id/confirm
POST   /api/deals/:id/content
PATCH  /api/deals/:id/content/:cid/rate
POST   /api/deals/:id/dispute

ADMIN
GET    /api/admin/applications
POST   /api/admin/applications/:id/approve
POST   /api/admin/applications/:id/reject      (reason code required)
PATCH  /api/admin/products/:id/status
GET    /api/admin/analytics
```

---

## 10. Technical Stack

| Layer | Technology | Rationale |
|---|---|---|
| Frontend | Next.js 14 (App Router) | SSR for product pool SEO; CSR for dashboard interactivity |
| Auth | Clerk | OAuth social login, role-based access, email verification |
| Database | PostgreSQL via Supabase | Row-Level Security enforces visibility rules at database level |
| Real-time | Supabase Realtime (Postgres CDC) | Pushes DB row changes to subscribed clients — no polling |
| AI engine | OpenAI GPT-4o + Perplexity API | GPT-4o for summaries, sentiment, recommendations; Perplexity for live web research (competitor data, keyword trends) |
| Job queue | Inngest | Durable background jobs — AI audits, score recomputation, payout scheduling, notifications |
| File storage | Cloudflare R2 | Product images, creator avatars, PDF exports |
| Email | Resend + React Email | Transactional email with React templates |
| Affiliate tracking | Custom (Next.js API + Supabase) | First-party only; short-code redirects; no third-party dependency |
| Payments | Stripe Connect | Creator payouts, platform fee deduction, UK banking support |
| Analytics | PostHog | Funnel analysis, session replay, feature flags |

---

## 11. Design System

**Fonts:** Plus Jakarta Sans (body, forms, labels) · Playfair Display (serif headlines, large numbers, product names) · DM Mono (data values, codes, timestamps, scores)

**Colour palette:**
- Background: `#0d0e14` (base) · `#11121a` (panel) · `#1c1f2e` (card) · `#222538` (card hover/active)
- Brand red: `#c03b1b` — primary CTAs, brand-specific UI, error states
- Amber gold: `#c9a245` — data highlights, scores, AI-generated content accent
- Green: `#3aaa78` — success states, creator-specific UI, "done" indicators
- Cream: `#f2ede4` (primary text) · `#a09890` (secondary text) · `#5a6070` (muted/labels)

**Form elements:** 1.5px borders, 10px border-radius, 13–14px font, minimum 44px height, amber border-color on focus

**Role colour coding:**
- Brand-facing UI elements: `#c03b1b` (brand red)
- Creator-facing UI elements: `#1c5c3f` (forest green)
- AI-generated content: `#3d3075` (purple) with ✦ prefix — always visually distinct from human-authored content
- Manager-only data: `#c49a3c` (amber) — signals information not visible to brands or creators

**Score display rules:**
- Never show a raw score without context — "84/100" always paired with "Strong — top 15% in Clean Beauty this cycle"
- Scores always show trend vs prior cycle: ↑ / ↓ / = with percentage change
- Every AI-generated figure has a "How is this calculated?" plain-English disclosure tooltip — never reveals model or weights

**Empty state rules:**
- New brand, no feedback yet: "Creator feedback appears as soon as the pool opens to your category. Here are 3 ways to make your listing stand out." + 3 specific tips
- New creator, never reviewed: "Start here — one product review takes 3 minutes and immediately begins building your standing." + a featured product to review
- Manager, no disputes: "No active disputes." — positive signal, not a blank screen

**Mobile:** Brand and creator dashboards fully functional at 375px. Event night screens are mobile-first. Product pool: swipeable card stack on mobile. Deal form: full-screen mobile flow, not a modal.

---

## 12. Pages Built (Current Status)

| Page | File | Status | Notes |
|---|---|---|---|
| Landing page | `bridgr-v4.html` | Built | Hero, 3-pane flow, event section, brand KPIs, creator journey, why different table, trust pillars, results, CTAs |
| Brand Intelligence Planner | `bridgr-brand-planner.html` | Built | 5-step form, accumulating right panel, dual age slider, channel links, compliance tags, sign-up modal trigger |
| Sign-up modal | Embedded in planner | Built | Unlock cards, tab switcher, create account / log in forms, success state |
| Profile editor | `bridgr-profile-editor.html` | Built | Pre-filled from planner, image upload, collapsible sections, visibility controls, auto-save |
| Live product profile | `bridgr-product-profile.html` | Built | Image carousel, product content, TikTok-style action bar, comment panel, promote panel, DM paywall, AI chatbot |

**Pages not yet built:**
- Brand dashboard (`/brand/dashboard`)
- Creator dashboard (`/creator/dashboard`)
- Product pool browser (`/creator/products`)
- Creator standing page (`/creator/standing`)
- Event night mobile view (`/brand/event/night`, `/creator/event/night`)
- Platform manager dashboard (`/admin/dashboard`)
- All manager sub-pages (applications, scoring, top 10 builder, event management)

---

## 13. What Has Not Been Built Yet

**Platform intelligence layer:**
- The right panel in the planner currently shows demo/static data. In production, "Analyse ↗" triggers a real API call: Perplexity searches for live competitor data, market size, and keyword trends; GPT-4o synthesises the output into the structured profile sections.

**Real account system:**
- Sign-up and login forms in the modal are UI-only. No Clerk integration yet.

**Creator-side experience:**
- Creator registration, profile setup, product pool browser, standing score system, and all creator dashboard screens are specified in the UX report but not yet built as HTML.

**Manager dashboard:**
- The complete admin interface (applications, scoring oversight, Top 10 builder, event management, disputes, analytics) is fully specified but not yet built.

**Event system:**
- Cycle management, Top 10 publish flow, event night mobile views, and deal confirmation system are specified but not built.

**Backend:**
- No database, API routes, job queue, or payment system implemented yet. All data is static/demo.

---

## 14. The One Core Principle

Every design and product decision on this platform is governed by a single rule:

**Both sides must arrive at the event already knowing why they want to work with each other.**

The planner generates market intelligence so brands know their position before they pitch. The product pool and creator feedback system means creators have already reviewed, commented on, and scored a brand's product before meeting them. The matching system surfaces the most relevant pairings. The deal form makes the agreement immediate.

The event is not a discovery mechanism. It is a confirmation mechanism. Everything before the event is designed to make the in-room conversation inevitable rather than cold.

---

*Bridgr Master Specification v1.0 — April 2026*
*For questions about this document contact the founding team.*
