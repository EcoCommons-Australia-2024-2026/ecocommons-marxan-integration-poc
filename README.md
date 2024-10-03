# ecocommons-marxan-integration-poc
Proof of Concept by the EcoCommons Australia team on how EcoCommons outputs can be integrated into Marxan Planning Platform (https://marxanplanning.org/)

If you would like to run this project in your device, please git clone this repository to your device.

First, in terminal, cd to the directory where you'd like to place this project.

In your terminal, Clone the template repository to this directory

```
   git clone https://github.com/EcoCommons-Australia-2024-2026/ecocommons-marxan-integration-poc
```

In ecocommons-marxan-integration-poc/ecocommons-marxan-integration-poc/, you will find "ecocommons-marxan-integration-poc.qmd", this Quarto Markdown file contains the codes to:

1. Import and plot the planning units of Queensland prepared with the Marxan MaPP
2. Plot a cost layer produced based on the planning units.
3. Plot three rasters of species distribution modelling outputs produced with the EcoCommons Platform.
4. Turn the SDM rasters of probability to binary presence and absence shapefiles with user defined thresholds (range from 0 to the Maximum TSS)
5. Plot the shapefiles of presence of examplar species. These shapefiles can be uploaded to the Marxan MaPP as features.

# File list and description
1. app.R and rsconnect folder organise the threshold shinyapp.
2. ec_html_template.css is the template for html file.
3. footer.html sets the format of footer for each html file.
4. renv.lock and renv folder sets the renv for the Quarto Markdown.

**You might need to install/update some packages, including "shiny" for running markdown file.**

<p align="center">
  <img src="https://github.com/user-attachments/assets/80e373cf-cd38-442a-a894-564660005e95" alt="Centered Image" width="400"/>
</p>
