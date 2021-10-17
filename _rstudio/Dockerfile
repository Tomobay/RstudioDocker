# image *you can modified
FROM rockerjp/tidyverse

# Install packages (you can add your packages if neccessaery)
RUN install2.r devtools
# get commands
RUN apt-get update
RUN apt-get install -y ca-certificates r-cran-rjava

ARG GITHUB_PAT http_proxy https_proxy

COPY --chown=rstudio:rstudio .config/rstudio/rstudio-prefs.json /home/rstudio/.config/rstudio/rstudio-prefs.json
ENV GITHUB_PAT $GITHUB_PAT
ENV http_proxy $http_proxy
ENV https_proxy $https_proxy

RUN echo $GITHUB_PAT
