# Sample of CI - CD pipeline for github and gitlab

This repository is to gather example template for Github and Gitlab CI - CD for different languages

An idea would be to create all your common actions into one repo and do something like :

```yml
  - name: Set up XXX
  uses: ./global-common-actions-git/actions/setup-gcp-gar-npm-config
  with:
    project-id: ${{ secrets.GCP_PROJECT_ID }}
    region: ${{ secrets.GCP_PROJECT_ID }}
    repository-name: npm-repository
    service-account: ${{ secrets.SERVICE_ACCOUNT }}
    scope: ${{ github.event.organization.login }}
    workload-identity-provider: ${{ secrets.WORKLOAD_IDENTITY_PROVIDER }}   
```
