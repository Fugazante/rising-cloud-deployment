# Rising Cloud Deployment GitHub Action

This GitHub Action deploys your existing Rising Cloud project with only one step in your workflow.

```yaml
  - name: My rising cloud project deployment
    uses: Fugazante/rising-cloud-deployment@v1
    with:
      rising-cloud-user: ${{ secrets.RC_USER }}
      rising-cloud-pasword: ${{ secrets.RC_PASSWORD }}
```

- **rising-cloud-user**: Rising cloud user name
- **rising-cloud-pasword**: Rising cloud passsword

*rising-cloud-user* and *rising-cloud-pasword* parameters are mandatory. They shoud be the the credentials 
of a Rising Cloud account with all the permissions needed for the project deployment, otherwise the action will fail.
By default the action considers that the .yaml file of your Rising cloud project is in the root path a it is called
**risincloud.yaml**. If it is not the case, it is possible to configure the path and the file name using the following optional
paramenters.

## Execute the action with optional parameters

```yaml
  - name: My rising cloud project deployment
    uses: Fugazante/rising-cloud-deployment@v1
    with:
      rising-cloud-user: ${{ secrets.RC_USER }}
      rising-cloud-pasword: ${{ secrets.RC_PASSWORD }}
      working-directory: "path/to/project"
      config-file: "myCustomRisingCloud.yaml"
```

- **working-directory**: Root path of the rising cloud project, where .yaml file is located.
- **config-file**: Name of the .yaml file to use for the deployment.

--------------------------------------------------------------------------------------------------------------

*This GitHub action has been develop with :heart: by [Fugazante - Creative code lab](https://fugazante.com)*