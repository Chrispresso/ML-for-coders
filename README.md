# Machine Learning for Coders

## Getting Started
- Download 64-bit version of [Python](https://www.python.org/downloads/). You will want Python 3.7 or newer.
- Clone the repository: `git clone https://github.com/Chrispresso/ML-for-coders.git`
- Within the root of this repository run `pip install -r requirements.txt` or, if you're using multiple versions of Python run `python3 -m pip install -r requirements.txt` .
- Launch jupyter notebook. If you have issues you can check the [docs](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/execute.html). Open a command prompt and type `jupyter notebook` , or if you have multiple versions of Python you can run `python3 -m notebook` .
- Navigate through the Jupyter Notebook UI to find the folder within the repository you just cloned and select the .ipynb that you wish to run. This should open the notebook in a new browser window. Although in a browser window, this is running locally on your machine now. Each "cell" within the notebook can be ran individuall by hitting `shift + enter`. The \[in\] cells consist of code to be ran, and the \[out\]  consist of the output after running the cell. If there's text in \[out\] then it means I've uploaded a notebook with my saved output to show you what you can expect. Be sure to still run the code within the \[in\].

## FAQ
1. Why is `pip` timing out?<br/>
You are most likely behind a firewall. If you are you have a couple of options. The first is to set HTTP_PROXY and HTTPS_PROXY within your environment variables, restart the terminal and try again. The second option is you can pass in `--proxy` flag with `pip`. For example: `python3 -m pip install --proxy <proxy> -r requirements.txt` .

2. Installing results in one or more incompatible packages.<br/>
It's possible you have an older version of package A and the installation of package B is now requiring a newer version. You can get around this by passing in the `--force-reinstall` flag to `pip` like so: `python3 -m pip install -r requirements.txt --force-reinstall` .


3. I get `ERROR: Could not install packages due to an EnvironmentError: [WinError 5] Access is denied:`<br/>
You can either re-run with `--user` flag for `pip` or you can start the terminal as admin and re-run (recommended).