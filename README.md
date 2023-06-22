# Qwik:
 
    - Full-Stack JavaScript Web Framework
    - Core framework (Qwik) and meta framework (Qwik City).
    - Inspired by React, Cue, Angular, Svelte, SolidJS and their meta frameworks (e.g. for handling hydration (hydration = making static HTML dynamic / "alive" / "fluid" with JavaScript) → performance optimization)- e.g. Next.js, Nuxt, SvelteKit 
    Developed by https://www.builder.io/
    - Open Source
    - Qwik 1.0 Release Blog Article
    - USP:
        - Problem: A web application gets slower with increasing complexity because current frameworks send too much JavaScript to the client (Especially for single page applications where rendering is client aka browser side).
        - Solution approach. JavaScript streaming:
            - Progressive/Progressive Hydration
            - Only the - constant - JavaScript code needed for a specific user interaction is sent to the client, regardless of application complexity. This results in low start-up times aka high start-up performance.
        - Promise: Qwik apps can scale for as much/complex JavaScript code as desired
        - Implementation
            New rendering paradigm to solve the hydration problem: Lazy Execution/Resumeability/Deferred JavaScript for constant start-up times): 
            Pausing execution on server and resuming execution in client - without having to repeat and re-download application logic, no DOM hydration/bootstrap component tree on every single refresh.
            - For example: the page requests the code of a click handler only when the respective button is clicked.
        - Developer Experience:
            - Uses JSX (see React syntax).
            - Interoperability/no framework lock-in due to framework-specific wrappers, e.g. [I'm an inline-style link](https://www.google.com)
    - Technical Intricacies:
        - Resumability is enabled by server-side HTML serialization of JavaScript. The client only loads the HTML string.
        - Lazy execution is enabled by HTML serialized event handling: JavaScript code is loaded only upon execution via UI interaction

  ![image](https://github.com/18Dominik/qwik/assets/35842490/fe601e58-7c0a-4da4-9805-165742f45d8f)



References:
- https://www.builder.io/blog/qwik-v1
