# Welcome

Welcome and thank you for participating in the Materials Informatics Workshop. 
I look forward to meeting all of you for an exciting two days.

One of the main objectives of the workshop is to provide hands-on tutorials on 
the use of the Materials Project software stack for materials analysis and 
automation. For these sessions, it would be extremely helpful if you already 
have the right equipment set up prior to the workshop. Below are some
instructions for setting up your laptop prior to the workshop.

# Required equipment

* Laptop with functioning Wi-Fi connection.
* OS should be reasonably modern and updated. Ideally, latest versions of 
  Windows, Mac or Linux OS, but slightly older versions should also be fine.

# Materials Project Account and API key

1. Go to [https://materialsproject.org](https://materialsproject.org) in your
   browser.

2. Sign up for a free account if you do not already have one.

3. Login to the Materials Project.

4. Go to your [Materials Project dashboard](https://materialsproject.org/dashboard).

5. Click "Generate API key" and copy down the API key. You will be using it to
   query the Materials Project for data.

# Machine preparation

1. Go to [https://conda.io/miniconda.html](https://conda.io/miniconda.html) 
   in your browser. Download and install the appropriate version of 
   **Python 3.6 miniconda** for your operating system. Detailed installation
   instructions can be found [here](https://conda.io/docs/user-guide/install/index.html) 
   for all OSes.

2. Open up an Anaconda terminal (if you are on Windows) or simply a terminal 
   (Mac or Linux). Create an environment for this workshop as follows:
   ```bash
   conda create --name MIWorkshop --yes python=3.6
   ```
   An environment is an isolated box in which you can work on things without
   affecting the rest of your machine. It is also easy to start over if you make
   any mistakes. More information can be found
   [here](https://conda.io/miniconda.html)

3. Go into the new conda environment.

   On Windows:
   ```bash
   activate MIWorkshop
   ```
   
   On Mac/Linux:
   ```bash
   source activate MIWorkshop
   ```

4. Install some common scientific Python packages and tools from Anaconda cloud.

   ```bash
   conda install --yes numpy scipy matplotlib sympy pandas requests jupyter git
   ```

5. Install pymatgen from the matsci channel.

   ```bash
   conda install --yes --channel matsci pymatgen
   ```

6. Check that you have installed everything correctly by typing:

   ```bash
   python -c "import pymatgen; print(pymatgen.__version__)"
   ```

   You should see something like "2017.12.8" or similar in your terminal.

7. Clone the [Github repository](https://github.com/shyuep/miworkshop.git) for
   this workshop by doing:

   ```bash
   git clone https://github.com/shyuep/miworkshop.git
   ```

8. Add your Materials Project API key to your configuration file by typing

   ```bash
   pmg config --add PMG_MAPI_KEY "<type in your API key from Materials Project>"
   ```

7. You may exit your environment by typing:

   On Windows:
   ```bash
   deactivate MIWorkshop
   ```

   On Mac/Linux:
   ```bash
   source deactivate
   ```
   
