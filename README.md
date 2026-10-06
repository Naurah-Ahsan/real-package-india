The Real Package

→ Open the live tool 

An interactive tool that puts the "average package" on an Indian engineering college brochure next to what engineering graduates actually earn — and works out how long the real number takes to pay the degree back.

The question

Every engineering college in India advertises an average placement package. Almost nobody checks that figure against national earnings data.

So: where does a typical advertised package actually sit in the real distribution of graduate salaries?

What I found

An ₹8 lakh "average package" works out to about ₹67,000 a month. The median employed engineering graduate aged 22–26 earns ₹28,000 a month. The 90th percentile is ₹50,000.

The figure printed as average sits above where roughly nine in ten graduates actually land.

Three more things that surprised me:

Finding	Number
NIRF-ranked colleges' claimed ₹6 lakh placements vs. the national supply of such jobs	1.8×
Graduate unemployment vs. the national rate	11.2% vs 3.1%
Share of employed engineering graduates working in software	58%, at ₹32,600/month

The 1.8× is the one I keep coming back to. India's ranked engineering colleges collectively claim almost twice as many entry-level ₹6 lakh placements as the entire country has jobs at that salary — and that's after every reported salary was discounted by 20%.

What the tool does

Pick a branch, a college type, and how you prepared for entrance exams. It returns:

An itemised bill — coaching fees (including drop years, which no calculator counts) plus four years of college
A payback period — years until earnings cover the cost, on real median earnings rather than the advertised package
A distribution chart showing exactly where the brochure figure falls among actual graduate salaries
A payback chart comparing the brochure scenario against the data
How the model works

Every preparation year charges the coaching cost. Every college year charges a quarter of the four-year total. Nothing comes in during either.

From graduation, earnings start at the branch's median and grow 8% a year — early-career salary growth in India runs well ahead of general wage growth.

Payback is the first year cumulative earnings cover total cost.

Pre-tax, nominal rupees, education loan interest excluded.

Data sources
What	Source
Graduate earnings by percentile	Analysis of PLFS data, Avanti Fellows
Placement claims vs. job supply	Same analysis
Employability by stream	India Skills Report 2026, Wheebox and ETS
Graduate unemployment	PLFS Annual Report 2025, National Statistical Office (March 2026)
College fees	Published 2026 fee structures
Coaching costs	Published 2026 institute fee pages
Method note — read this one

The percentile figure for the advertised package is modelled, not measured.

Only two points of the earnings distribution are published: the median (₹28,000) and the 90th percentile (₹50,000). I fitted a lognormal curve through those two points and read the advertised package off that curve.

That gives a defensible estimate of position — it is not a measured percentile. Treat it as "roughly where this sits," not a precise rank.

Limitations
Two salary tiers only. The published data distinguishes software from everything else, so that's all the tool distinguishes. It can't tell mechanical from civil.
Some employability rates are estimated. Computer science (80%), IT (78%) and engineering overall (70.15%) come straight from the India Skills Report. The others are placed inside the published spread and marked as estimates.
A national median flattens an enormous range. The gap between an IIT graduate and a tier-three college graduate is huge, and a single median hides all of it.
Opportunity cost is excluded. Earlier versions charged for wages forgone during six years of study. I removed it because it confused more than it clarified — but it means every result here is more optimistic than reality.
Selection effects are ignored. People who clear entrance exams differ from those who don't in ways that would show up in their earnings regardless of the degree.
It also treats a degree purely as a financial instrument, which is the one thing it certainly is not.
Built with

HTML, CSS and vanilla JavaScript in a single file. Charts are hand-drawn SVG — no chart library. Hosted on GitHub Pages.

No framework, no build step, no dependencies. The dataset is small enough to live in the page.

How this was built

Vibecoded with Claude. Saying so up front rather than leaving it to be guessed at.

I set the question, chose the India angle, and made the calls on scope and design — what went in, what got cut, and how it should look. Claude sourced and checked the data and wrote the HTML, CSS and JavaScript.
