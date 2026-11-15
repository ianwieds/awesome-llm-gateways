# Contributing

Thanks for helping keep this list useful. Please read these rules before you open a pull request.

## What belongs here

This list covers projects that route or govern LLM traffic between applications and model providers: gateways, proxies, model routers, caches, cost controls, security proxies and the client libraries that give one API across providers. An MCP gateway belongs in [Awesome MCP Gateways](https://github.com/ianwieds/awesome-mcp-gateways) and a model host or inference server belongs elsewhere; an observability, API management or security product belongs here only when routing or governing LLM calls is central to what it does.

<!-- awesome:rules -->
An entry must be:

- **Public:** a repository or page anyone can open without signing in.
- **Documented:** a README or docs page that explains what it does and how to use it.
- **Maintained:** for a repository, not archived, not marked deprecated by its owner, and with a commit in the last 12 months.
- **Established:** a GitHub project has at least 10 stars when it is submitted.
- **Working:** every link resolves.<!-- /awesome:rules -->

<!-- awesome:guide -->
## How to add an entry

1. Pick the section (and subsection, where there is one) that fits best.
2. Add one line in this format:

   ```markdown
   - [Name](https://link) - Short description.
   ```

3. Keep the section in alphabetical order by name (case-insensitive).
4. Write the description in your own words: one short sentence, 100 characters at most, ending with a period. Say what it does, plainly. No marketing words, no star counts, no emoji, no em dashes.
5. Link the original source: the repository or product page for a project, the original post for an article or talk. No tracking links or mirrors.

## Pull requests

- One entry per pull request.
- Use a title like `Add <Name>`.
- Search the list first to make sure the entry is not already here.
- Removals and fixes for dead links, archived repos or wrong descriptions are welcome; say why in the pull request.

Every pull request is checked automatically against the rules above. One that fails is closed with a comment that says what to fix; a fixed pull request is welcome.

By contributing, you agree to release your contribution under the [CC0 1.0](LICENSE) dedication.
<!-- /awesome:guide -->
