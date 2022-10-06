# EXO Subgraph

Aims to deliver analytics & historical data for EXO. Still a work in progress.

The Graph exposes a GraphQL endpoint to query the events and entities.

Current subgraph locations:

1. **Exchange**: Includes all EXO Exchange data with Price Data, Volume, Users, etc:

## To setup and deploy

For any of the subgraphs follow below steps

1. CD in to the subgraph directory `subgraphs:[subgraphName]`
2. Run the `yarn run prepare:[network]` to prepare yaml file from template.yaml and network specific data.
3. Run the `yarn run codegen` command to prepare the TypeScript sources for the GraphQL (generated/schema) and the ABIs (generated/[ABI]/\*)
4. [Optional] run the `yarn run build` command to build the subgraph. Can be used to check compile errors before deploying.
5. Run `graph auth https://api.thegraph.com/deploy/ <ACCESS_TOKEN>`
6. Deploy via `yarn run deploy`.
