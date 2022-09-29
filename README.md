# Machine Learning for Coders

## Getting Started
- Download **64-bit** version of [Python](https://www.python.org/downloads/). You will want Python 3.7 or newer.
    - If you're on Windows [here](https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe) is a direct link for Python 3.9.
- Find the path where you installed it. If you did a basic installation it should be under `C:\Users\%username%\AppData\Local\Programs\Python\`. Go there and double check that you have a folder with whatever version you just installed.
- Add Python to your `PATH`.
    - Hit the windows key and type `env` and select `Edit the system environment variables`. 
    - Next, click `Environment Variables` and then under `System Variables` find your `PATH` variable and double click it.
    - Click new and type `C:\Users\%username%\AppData\Local\Programs\Python\Python39` (assuming you did Python39) and hit enter.
    - Click new and type `C:\Users\%username%\AppData\Local\Programs\Python\Python39\Scripts` (assuming you did Python39) and hit enter.
    - @NOTE: If you have multiple versions of Python3.x installed you will have problems. If you want to get around those issues you can rename one of your python.exe installations to something like python37 or python39 to differentiate them within the environment variables. Otherwise when you type `python` at the command line, it will use whatever is found first within your environment. This would instead make it so you can type `python37` or `python39` to specify a version.
- Open command prompt (`windows key + r`, type `cmd` and hit `enter`)
- Clone the repository by typing `git clone https://github.com/Chrispresso/ML-for-coders.git` into your command prompt. 
- Type `cd ML-for-coders` into command prompt
    - If you don't have git, download it from [https://git-scm.com/downloads](https://git-scm.com/downloads)
- Run `pip install -r requirements.txt --force-reinstall` or, if you're using multiple versions of Python run `python3 -m pip install -r requirements.txt --force-reinstall`.
    - The `--force-reinstall` is helpful if you previously had a 32-bit version of Python and are moving to the 64-bit version. Otherwise `pip` may use a cached version, which you don't want.
- Launch jupyter notebook. If you have issues you can check the [docs](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/execute.html). Open a command prompt and type `jupyter notebook` , or if you have multiple versions of Python you can run `python3 -m notebook` .
- Navigate through the Jupyter Notebook UI to find the folder within the repository you just cloned and select the `.ipynb` that you wish to run. This should open the notebook in a new browser window. Although in a browser window, this is running locally on your machine now. Each "cell" within the notebook can be ran individuall by hitting `shift + enter`. The \[in\] cells consist of code to be ran, and the \[out\]  consist of the output after running the cell. If there's text in \[out\] then it means I've uploaded a notebook with my saved output to show you what you can expect. Be sure to still run the code within the \[in\].

## FAQ
1. Why is `pip` timing out?<br/>
You are most likely behind a firewall. If you are you have a couple of options. The first is to set HTTP_PROXY and HTTPS_PROXY within your environment variables, restart the terminal and try again. The second option is you can pass in `--proxy` flag with `pip`. For example: `python3 -m pip install --proxy <proxy> -r requirements.txt` .

2. Installing results in one or more incompatible packages.<br/>
It's possible you have an older version of package A and the installation of package B is now requiring a newer version. You can get around this by passing in the `--force-reinstall` flag to `pip` like so: `python3 -m pip install -r requirements.txt --force-reinstall` .


3. I get `ERROR: Could not install packages due to an EnvironmentError: [WinError 5] Access is denied:`<br/>
You can either re-run with `--user` flag for `pip` or you can start the terminal as admin and re-run (recommended).