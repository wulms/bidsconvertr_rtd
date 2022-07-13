Windows:





Ubuntu:

Installation of R in Ubuntu 22.04:

:: wget -qO- https://cloud.r-project.org/bin/linux/ubuntu/marutter_pubkey.asc | sudo gpg --dearmor -o /usr/share/keyrings/r-project.gpg

:: echo "deb [signed-by=/usr/share/keyrings/r-project.gpg] https://cloud.r-project.org/bin/linux/ubuntu jammy-cran40/" | sudo tee -a /etc/apt/sources.list.d/r-project.list

:: sudo apt update

:: sudo apt install --no-install-recommends r-base

:: sudo apt install r-base-dev

:: sudo apt install libcurl4-openssl-dev libssl-dev libxml2-dev libfontconfig1-dev

:: sudo -i R

Installation of required packages in R

:: install.packages("devtools")

:: install_github("wulms/bidsconvertr")

# Everything should be installed automatically.

This command starts the workflow:

:: convert_to_BIDS()

