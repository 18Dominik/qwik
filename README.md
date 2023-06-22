# Qwik:
- Full-Stack JavaScript Web Framework
    - Core framework (Qwik) and meta framework (Qwik City).
    - Inspired by React, Cue, Angular, Svelte, SolidJS and their meta frameworks (e.g. for handling hydration (hydration = making static HTML dynamic / "alive" / "hydrated" by loading JavaScript) → performance optimization)- e.g. Next.js, Nuxt, SvelteKit for full-stack development and Server-Side-Rendering (SSR)
    Developed by https://www.builder.io/
    - Open Source
    - Qwik 1.0 Release Blog Article
    - USP:
        - Problem: A web application gets slower with increasing complexity because current frameworks send too much JavaScript to the client (Especially for single web page applications (SPA) with Angular, React, ... where rendering is client aka browser side by executing JavaScript code).
        - Solution approach. JavaScript streaming:
            - Progressive Hydration 
            - Only the - constant - JavaScript code needed for a specific user interaction is sent to the client, regardless of application complexity. This results in low start-up times aka high start-up performance.
        - Promise: Qwik apps can scale for as much/complex JavaScript code as desired
        - Implementation
            - New rendering paradigm to solve the hydration problem: Lazy Execution/Resumeability/Deferred JavaScript for constant start-up times):
              - Reactive (asynchronous programming/track which components are subscribed to which state)
              - Progressive: Client loads JavaScript components only when needed
              - Resumeability: Pausing execution on server and resuming execution in client - without having to repeat and re-download application logic, no DOM hydration/bootstrap component tree on every single refresh. Amount of code to execute is proportional to actual user interaction rather than all possible     i               interactions on the page
            - For example:
                - the page requests the code of a click handler only when the respective button is clicked.
                - A complex with many components includes a counter that displays an integer. The component of the button and displayed integer is resumable, so not the whole DOM/component tree needs to be re-rendered by clicking the counter.
        - Developer Experience:****
            - Uses JSX (see React syntax).
            - Full Stack Web Framework: One single programming language (JavaScript) in backend and frontend
            - Interoperability/no framework lock-in due to framework-specific wrappers, e.g. [Qwik-React](https://www.builder.io/blog/qwik-v1)
- Technical Intricacies:
        - Resumability is enabled by server-side HTML serialization of JavaScript, e.g. event-listeners. The client only loads the HTML string.
        - Lazy execution is enabled by HTML serialized event handling: JavaScript code is loaded only upon execution via UI interaction

  ![image](https://github.com/18Dominik/qwik/assets/35842490/fe601e58-7c0a-4da4-9805-165742f45d8f)
  ![image](https://github.com/18Dominik/qwik/assets/35842490/b03f3def-811c-4963-9d6f-b8f6e84ebf2e)


References:
- [Builder.io](https://www.builder.io/)
- [Qwik Release Blog](https://www.builder.io/blog/qwik-v1)
- [Think Qwik](https://qwik.builder.io/docs/concepts/think-qwik/)
- [Getting Started with Qwik](https://qwik.builder.io/docs/getting-started/). Don't forget to install node modules via ``npm i`` before starting the app in the app directory with ``npm start``
- [Qwik City Routing and file formats](https://qwik.builder.io/docs/routing/)
- [Great Article on Hydration vs. Resumability](https://entwickler.de/webentwicklung/resumability-hydration-javascript)
- [qwik courses](https://qwik.builder.io/ecosystem/#courses)
- [qwik introduction](https://learn.hirez.io/products/a-qwik-introduction)
- [Dev.to: Resumability, WTF](https://dev.to/this-is-learning/resumability-wtf-2gcm)
- [Dev.to: Resumability with Qwik](https://dev.to/this-is-learning/resumable-javascript-with-qwik-2i29)

