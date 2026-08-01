# Caresyntax

Caresyntax is a surgical intelligence company that builds a vendor-neutral, enterprise-scale
data platform for the operating room. Founded in 2013 in Berlin and dual-headquartered in
Berlin and San Francisco, it captures video, audio, image, device, EMR, financial and outcomes
data from inside and around the OR and applies AI analytics to it — pre-operative workflow
optimization, real-time intraoperative decision support, and post-operative clinical safety,
quality and utilization insights. The platform pairs the PRIME365 vendor-neutral OR /
medical-device integration layer with the qvident surgical performance-management and analytics
suite, and is deployed in more than 4,000 operating rooms worldwide.

- https://www.caresyntax.com/
- https://caresyntax.com/platform/
- https://github.com/caresyntax (no public repositories)

## API surface

**No public API.** Enrichment on 2026-08-01 found no developer portal, API reference, OpenAPI /
AsyncAPI / GraphQL contract, SDK, CLI, MCP server or A2A agent card on any Caresyntax host.
An API gateway is live at `api.caresyntax.com` (Kong 3.4.2, CNAME `api.new.caresyntax.com`),
but every probed path — including `/openapi.json`, `/swagger.json`, `/graphql`, `/fhir`,
`/mcp` and all `/.well-known/*` paths — returns
`404 {"message":"no Route matched with those values"}`. Integration is delivered through
enterprise and partner engagements, not a self-serve developer program.

The marketing site sits behind a Vercel bot challenge (HTTP 403 on `/.well-known/*`, HTTP 429
on HTML paths) for automated fetches; that block is recorded in
`well-known/caresyntax-well-known.yml` rather than being treated as an absence.

## Artifacts

| Artifact | File | Method |
|---|---|---|
| Conformance | `conformance/caresyntax-conformance.yml` | searched |
| Domain security | `security/caresyntax-domain-security.yml` | probed |
| Well-known probe record | `well-known/caresyntax-well-known.yml` | probed |
| llms.txt | `llms/caresyntax-llms.txt` | generated |
