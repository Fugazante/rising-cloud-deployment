# Rising Cloud Deployment GitHub Action

This GitHub Action deploys your existing Rising Cloud project with only one step in your workflow.

```yaml
  - name: My rising cloud project deployment
    uses: Fugazante/rising-cloud-deployment@v1
    with:
      rising-cloud-user: ${{ secrets.RC_USER }}
      rising-cloud-password: ${{ secrets.RC_PASSWORD }}
```

- **rising-cloud-user**: Rising cloud username
- **rising-cloud-password**: Rising cloud password

*rising-cloud-user* and *rising-cloud-password* parameters are mandatory. They should be the credentials 
of a Rising Cloud account with all the permissions needed for the project deployment, otherwise the action will fail.
By default, the action considers that .yaml file of your Rising cloud project is in the root path and it is called
**risingcloud.yaml**. If it is not the case, it is possible to configure the path and the file name using the following optional
parameters.

## Execute the action with optional parameters

```yaml
  - name: My rising cloud project deployment
    uses: Fugazante/rising-cloud-deployment@v1
    with:
      rising-cloud-user: ${{ secrets.RC_USER }}
      rising-cloud-password: ${{ secrets.RC_PASSWORD }}
      working-directory: "path/to/project"
      config-file: "myCustomRisingCloud.yaml"
```

- **working-directory**: Root path of the rising cloud project, where .yaml file is located.
- **config-file**: Name of the .yaml file to use for the deployment.

--------------------------------------------------------------------------------------------------------------

*This GitHub action has been developed with :heart: by [Fugazante - Creative code lab](https://fugazante.com)*