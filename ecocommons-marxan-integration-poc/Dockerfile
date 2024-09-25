# Base image with R and Shiny Server
FROM rocker/verse:latest

# Install system dependencies
RUN apt-get update && apt-get install -y \
    libudunits2-dev \
    libgdal-dev \
    libgeos-dev \
    libproj-dev

# Install Quarto CLI
RUN wget https://quarto.org/download/latest/quarto-linux-amd64.deb && \
    dpkg -i quarto-linux-amd64.deb && \
    rm quarto-linux-amd64.deb

# Set the working directory
WORKDIR /srv/quarto-server/

# Copy your Quarto project into the container
COPY . /srv/quarto-server/

# Activate renv (if needed) and restore packages
RUN R -e "renv::restore()"


# Expose the port for Shiny (3838)
EXPOSE 3838

# Render the Quarto document
RUN quarto render ecocommons-marxan-integration-poc.qmd

# Start Shiny Server
CMD ["R", "-e", "shiny::runApp('/srv/quarto-server')"]
