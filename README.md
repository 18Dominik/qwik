# Qwik
- Full-Stack JavaScript Web Framework
    - Core framework (Qwik) and meta framework (Qwik City).
    - Inspired by single web page applications **(SPA)** frameworks like React, Cue, Angular, Svelte, SolidJS and their meta frameworks **for full-stack development and Server-Side-Rendering (SSR)** (e.g. for handling **hydration** (hydration = making static HTML dynamic / "alive" / "hydrated" by (re-)loading and (re-)playing JavaScript on the client))- e.g. Next.js, Nuxt, SvelteKit 
    - Developed by https://www.builder.io/
    - Open Source
    - USP:
        - Problem: A **web application gets slower with increasing complexity** because current frameworks send too much JavaScript to the client
            - for the case of single web page applications **(SPA)** with React, Cue, Angular, Svelte, SolidJS, ... where rendering (interractive & non-interactive elemnts) is client aka browser side by executing JavaScript code)
            - for the case of server-sided rendering with full stack frameworks like Next.js, Nuxt, SvelteKit where - though the html is rendered server side, the JavaScript to make the website dyynamic, aka to get the interactive elements do sth., is executed client side
        - Solution approach. JavaScript streaming (instead of JavaScript downloading as it is in the case of with hydration):
            - **Progressive Hydration**  by automatically splitting up JavaScript in chunks by **closure chunking**
            - Only the - constant - JavaScript code needed for a specific user interaction is sent to the client, regardless of application complexity. This results in low start-up times aka high start-up performance.
        - Promise: Qwik apps can scale for as much/complex JavaScript code as desired
        - Implementation
            - New rendering paradigm to **solve the hydration problem**: Lazy Execution/**Resumeability**/Deferred JavaScript for constant start-up times):
              - Reactive (asynchronous programming/track which components are subscribed to which state)
              - Progressive: Client loads JavaScript components only when needed
              - Resumeability: Pausing execution on server and resuming execution in client - without having to repeat and re-download application logic, no DOM hydration/bootstrap component tree on every single refresh. **Amount of code to execute is proportional to actual user interaction rather than all possible        interactions on the page**
            - For example:
                - the page requests the code of a click handler only when the respective button is clicked.
                - A complex application with many components includes a counter that displays an integer. The component of the button and displayed integer is resumable, so not the whole DOM/component tree needs to be re-rendered by clicking the counter.
        - Developer Experience:
            - Uses JSX (see React syntax).
            - Full Stack Web Framework: One single programming language (JavaScript) in backend and frontend
            - Interoperability/no framework lock-in due to framework-specific wrappers, e.g. [Qwik-React](https://www.builder.io/blog/qwik-v1)
- Technical Intricacies:
  - Resumability is enabled by server-side HTML serialization of JavaScript, e.g. event-listeners. The client only loads the HTML string
  -  Lazy execution is enabled by HTML serialized event handling: JavaScript code is loaded only upon execution via UI interaction
  -  The "smart" HTML includes Component Boundaries, Event Listeners, and the page's app state
 
    
  ![image](https://github.com/18Dominik/qwik/assets/35842490/fe601e58-7c0a-4da4-9805-165742f45d8f)
  ![image](https://github.com/18Dominik/qwik/assets/35842490/b03f3def-811c-4963-9d6f-b8f6e84ebf2e)


# References
## Builder.io
### Setup
- [Builder.io](https://www.builder.io/)
- [Getting Started with Qwik](https://qwik.builder.io/docs/getting-started/). Don't forget to install node modules via ``npm i`` before starting the app in the app directory with ``npm start``
- [Qwik Release Blog](https://www.builder.io/blog/qwik-v1)
### Technical Details
- [Think Qwik](https://qwik.builder.io/docs/concepts/think-qwik/)
- [Qwik: USP](https://www.builder.io/blog/our-current-frameworks-are-on-we-need-o1)
- [Qwik City Routing and file formats](https://qwik.builder.io/docs/routing/)
- [builder.io: Progressive Hydration](https://www.builder.io/blog/why-progressive-hydration-is-harder-than-you-think)
## Courses
- [qwik courses](https://qwik.builder.io/ecosystem/#courses)
- [qwik introduction](https://learn.hirez.io/products/a-qwik-introduction)
## Dev.to
- [Dev.to: Resumability, WTF](https://dev.to/this-is-learning/resumability-wtf-2gcm)
- [Dev.to: Resumability with Qwik](https://dev.to/this-is-learning/resumable-javascript-with-qwik-2i29)
## German Resources
- [Great Article on Hydration vs. Resumability](https://entwickler.de/webentwicklung/resumability-hydration-javascript)
- [heise: Qwik](https://www.heise.de/news/Full-Stack-Framework-Qwik-1-0-bringt-neuen-Ansatz-fuer-schnellere-Interaktivitaet-8985672.html)











