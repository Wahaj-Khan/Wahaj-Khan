# Wahaj Ali Khan

AI Engineer and full-stack developer in Karachi. I build production LLM systems on Node/TypeScript and Next.js: agentic tool-calling loops, RAG pipelines, and workflow automation.

## Most of my work is private

I build client platforms, so the majority of what I ship lives in private repositories and will never show up on this profile. Here is what I actually work on, described without naming clients:

**Agentic systems.** A production conversational analytics assistant on AWS Bedrock with Claude: a hand-written streaming Converse loop over 7 tools, multi-round tool use, incremental assembly of tool-call JSON across stream deltas, and detection of unproductive loops with corrective prompt injection. RAG over a managed knowledge base is exposed as a tool *inside* the loop rather than bolted on beside it, because the managed retrieve-and-generate path returns its own refusal text and takes synthesis away from the primary model.

**Guardrails for LLM-generated SQL.** Single-statement SELECT-only enforcement, table allowlisting, CTE-aware table extraction, role-based multi-tenant scoping, and column-level PII redaction applied to result rows before they ever reach the model. Prompting alone is not a security boundary.

**LLM cost governance.** Budget enforcement backed by transactional spend accounting, per-user quotas, a runtime kill switch, database-backed per-model token pricing, and prompt-injection hardening via Unicode normalization and zero-width-character detection.

**Content and outreach pipelines.** Multi-stage Claude pipelines with two-tier model routing (a strong model to generate, a cheap one to critique and edit), prompt caching across tool and system prefixes, hard token budgets read from usage, LLM-as-judge QA with revision loops, and human approval gates over HMAC-verified webhooks.

**Serverless bulk processing.** AWS Lambda and SQS pipelines with transactional enqueue, message-size guards with automatic payload splitting, partial-batch failure reporting, and dead-letter queues.

**Workflow automation.** Multi-agent n8n systems that route between Claude and OpenAI agents based on pipeline state, with live tool calls against calendar and CRM APIs and Postgres-backed conversation memory.

## Tech

**AI:** Anthropic Claude (Messages API, Bedrock Converse, tool use, prompt caching), OpenAI, Google Vertex AI / Gemini, LangChain, RAG, Pinecone, Firestore vector search

**Backend:** Node.js, Express, NestJS, TypeScript, MongoDB, PostgreSQL, Supabase, Drizzle, Prisma

**Frontend:** React, Next.js, TypeScript, Tailwind, Redux Toolkit, Zustand

**Cloud:** AWS (Bedrock, Lambda, SQS, S3, Cognito, EC2), GCP (Vertex AI, Firestore, GCS), Docker

**Automation:** n8n, pg-boss, Vercel cron

## What is public here

[**life-os**](https://github.com/Wahaj-Khan/life-os) is a personal Flutter app and the one repo here that is documented properly. Worth a look if you want to see how I structure a codebase: feature-first modules with enforced layering, a pure-Dart scoring core built test-first, and a whole architecture shaped by the constraint of staying on Firebase's free tier.

The rest of the repos on this profile are personal experiments and are not representative of my professional work.

## Reach me

- Email: wahajkhan108@gmail.com
- LinkedIn: [linkedin.com/in/wahaj-a-khan](https://www.linkedin.com/in/wahaj-a-khan/)

Happy to walk through the architecture of any of the private work on a call.
