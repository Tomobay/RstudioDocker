# Rstudio images
Rstudio docker images

The user can start their projects by forking from this repository and customize the docker file to cater to their project needs.

## Editing
 - _rstudio/Dockerfile
 - change the base image, install packages, change global options, etc.
 - _rstudio/docker-compose.yml
 - rename the image name your-project-name:latest

## Usage
1. Start the RStudio Server:
   ```sh
   docker-compose up -d
   ```
2. Browse <http://localhost:8787> to connect to the local RStudio Server
3. Open the R project `/home/rstudio/{yourproject}/project.Rproj`
4. Do your analysis
5. Stop the RStudio Server:
   ```sh
   docker-compose down
   ```

## Requirement
# GITHUB_PAT (personal access token)
you need to set GITHUB_PAT to your local environment
to get your personal access token access to https://github.platforms.engineering/settings/tokens
* check to repo & gist
* you can refer following for more information
```R
usethis::browse_github_pat()
```

If you don't prefer to set personal access token to your own env you can modified _rstudio/docker-compose.yml `$GITHUB_PAT` to your personal access token.
