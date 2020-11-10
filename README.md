# BioHackOutcomes
BioHackathon project to define and follow up BioHackathon projects

# What we would like to do during the BioHackathon
* Parameters (to be set by hand)
  * BioHackathon year
  * Link to BioHackathon project
  * Dates when the events took place: bh_start_date, bh_final_date
  * Initial date for agregations: start_date (if ommited the created date of the analyzed repo will be used)
  * Final date for aggregations: final_date (if ommited "today" will be used)
* Let's focus on BioHackathon Europe GitHub repositories
  * 2019 Projects: https://github.com/elixir-europe/BioHackathon-projects-2019 
  * 2019 BioHackathon dates: 2019.11.18 - 2020.11.22
  * 2020 Projects: https://github.com/elixir-europe/BioHackathon-projects-2020
  * 2020 BioHackathon dates: 2020.11.09 - 2020.11.13
* For a given BioHackathon year (either 2019 or 2020 by now)
  * Let's get the projects out of the folder name "projects"
  * If there is any code in there, let's get metadata
  * If not, let's go through the readme.md file and find any GitHub repo mentioned there that is relevant for us
  * A GitHub repo is a link starting with github.com
  * A GitHub repo is relevant for us if it is a repo rather than an organization or user
  * Avoid duplicates/loops (e.g., this repo will be processed and it includes links to the BioHackathon projects)
  * For 2020 projects, double check that the repo **also** has the topic BioHackEU20 (non-case sensitive)
  * Extract metadata
    * Owner username
    * Repo title
    * Repo description
    * License
    * Creation date    
    * Contributor usernames and dates they joined
    * Total number of commits, downloads, forks, watch
      * between an initial date *start_date* and right before the starting date of the BioHackathon *bh_start_date*
      * during the BioHackathon days *bh_start_date* and *bh_final_date*
      * a given period *start_date* and *final_date*
  * Create dataframe with extracted metadata
      * Aggregate total number of contributors using the same date ranges as for commits and so
