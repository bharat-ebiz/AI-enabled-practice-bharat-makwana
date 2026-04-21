# Implementation Plan

- Implement this work in parallel mode. where agents and subagents will responsible for there task where

**Backend Agent :**

- take reference from current plan usage calculation handling
- reference file : `@plan/context-calculation.ts`.
- update `ResponseGeneratorService` method and inject `contextUsage` in `Response` object as it already having `stream` based formatting response that will return token usage in real time.

**Frontend Agent :**

- Review `PromptInputBox` component (File : `@components/prompt-input-box.tsx`).
- Add footer in `PromptInputBox` component to show token usage in two format token and percentage wise.
- Update `Response Mapping Model` (File : `@components/response-mapping-model.ts`). with `contextUsage` new parameter.
- Make style align with current prompt input box UI/UX. and it will not disturb user for prompting.
- It should be need to use stander secondary color for footer and it respective text.
