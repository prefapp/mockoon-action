# mockoon-cli-action

This action starts a mockup api using `mockoon-cli`.
It was designed to be used in a workflow as the previous step to execute tests. 

## Usage

You can now consume the action by referencing the v1 branch

```yaml
steps:
  - name: Start mockup api
    id: package
    uses: prefapp/mockoon-cli-action@v1
    with:
      file: ${{ github.workspace }}/__tests__/fixtures/mockoon/backstage-api-simulation.json
  - run: curl http://localhost:5000/api/firestarter-config
        shell: bash
```
