Windows:

~~~~~~~~~~~~~~~~~

Install a recent R-Version.
Install the according Rtools version.
Install RStudio.




Ubuntu:
~~~~~~~~~~~~~~~~~

Installation of R in Ubuntu 22.04:

.. code-block:: console

wget -qO- https://cloud.r-project.org/bin/linux/ubuntu/marutter_pubkey.asc | sudo gpg --dearmor -o /usr/share/keyrings/r-project.gpg

echo "deb [signed-by=/usr/share/keyrings/r-project.gpg] https://cloud.r-project.org/bin/linux/ubuntu jammy-cran40/" | sudo tee -a /etc/apt/sources.list.d/r-project.list

.. code-block:: console

sudo apt update

sudo apt install --no-install-recommends r-base

sudo apt install r-base-dev

sudo apt install libcurl4-openssl-dev libssl-dev libxml2-dev libfontconfig1-dev

.. code-block:: console

sudo -i R

Installation of required packages in R

.. code-block:: console

install.packages("devtools")

install_github("wulms/bidsconvertr")

# Everything should be installed automatically.

This command starts the workflow:

.. code-block:: console

convert_to_BIDS()

