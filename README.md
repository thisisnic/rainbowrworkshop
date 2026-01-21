# LLMs in R for Data Analysis

## rainbowR 2026 Conference Workshop by Nic Crane

### Workshop Overview

LLMs can be massively useful in R workflows, when used in the right places and if you're aware of not only the benefits, but also the risks. In this hands-on workshop, you'll learn how to use LLMs programmatically in R, and come away with both the confidence to experiment and a working script that extracts data from unstructured text.

We'll look at where LLMs can help, where they'll let you down, and techniques for making your results more trustworthy. You're going to leave with a practical sense of what's possible and where to be cautious.

**What you'll learn:**

- Getting started with LLMs in R using {ellmer}
- Prompt engineering for more predictable results
- Extracting structured data from unstructured text
- Using LLMs to call R functions (tool calling)

### Workshop Prework

#### Option A: Use Posit Cloud (recommended for beginners)

If you'd prefer not to install anything on your laptop - or if you're on a work machine with restrictions on installing software or connecting to external APIs - you can use Posit Cloud instead.

1. Go to [posit.cloud](https://posit.cloud) and create a free account
2. Create a new RStudio project
3. Follow steps 1-4 below inside your cloud project

This runs R entirely in your browser. Your API key stays in your cloud project, not on your work machine.

#### Option B: Local installation

**1. Install R packages**

```r
install.packages(c("ellmer", "mall", "dplyr", "readr", "tidyr", "usethis"))
```

**2. Get an API key**

We recommend **Gemini** (free), but Anthropic or OpenAI work too if you already have credits.

- **Gemini (free)**: Go to [Google AI Studio](https://aistudio.google.com/app/apikey), sign in, and create an API key
- **Anthropic (paid)**: Get your key from [console.anthropic.com](https://console.anthropic.com)
- **OpenAI (paid)**: Get your key from [platform.openai.com](https://platform.openai.com)

**3. Store your API key**

Run `usethis::edit_r_environ()` in R, then add:

```
GOOGLE_API_KEY=paste-your-key-here
# OR: ANTHROPIC_API_KEY=paste-your-key-here
# OR: OPENAI_API_KEY=paste-your-key-here
```

Save the file and **restart R**.

**4. Test your setup**

```r
library(ellmer)
chat <- chat_google_gemini()  # or chat_anthropic() / chat_openai()
chat$chat("Say hello!")
```

If you see a greeting back, you're all set!

### Workshop Schedule

- Section 0: Welcome and Setup
- Section 1: Getting Started with LLMs in R
- Section 2: Prompt Engineering
- Section 3: Structured Output
- Section 4: Tool Calling
- Section 5: Wrap-up and Resources

### Instructor

[**Nic Crane**](https://niccrane.com) is an R educator and consultant.  They are passionate about open source, and learning and teaching all things R.

------------------------------------------------------------------------

Copyright © 2025 Nic Crane. All Rights Reserved.
