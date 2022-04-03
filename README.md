# CMPE 325 Project

A hand-tracking mouse that solely requires the use of a webcam to control.

## Creating an executable

### 1. Virtual environment

Everything should be installed using virtual env's.

1. Navigate to project root

   ```bash
   cd CMPE325Project
   ```

1. Create a virtual environment called `venv`

   For MacOS, the command is:

   ```bash
   python3 -m venv venv
   ```

   But it might be different on Windows. Follow the instructions [here](https://docs.python.org/3/library/venv.html) if you run into problems.

1. Start the virtual environment

   For Mac the command is:

   ```bash
   source venv/bin/activate
   ```

   For Windows, it will be:

   ```bash
   C:\> <venv>\Scripts\activate.bat # cmd.exe Shell
   # or
   PS C:\> <venv>\Scripts\Activate.ps1 # PowerShell
   ```

   Again, follow the instructions [here](https://docs.python.org/3/library/venv.html) if you run into problems.

### 2. Install dependencies

Once you have the virtual env running we can install the required dependencies.

1. First, upgrade Pip

    ```bash
    pip install --upgrade pip
    ```

1. Install dependencies

    ```bash
    pip install -r requirements.txt
    ```

### 3. Test run the app

If everything was installed properly, you should be able to run the app using the command below. It will open a Chrome window (this can take a minute or two).

```bash
# still in the virtual environment
python app.py
```

### 4. Create executable

We use `pyinstaller` to create the executable. Run:

```bash
pyinstaller app.spec --windowed --onefile
```

This should create a folder called `dist/` containing the executable. Test and make sure it runs on your system.


