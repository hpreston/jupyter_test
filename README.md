# Jupyter Test

Simple experimental repo for building a Docker image for a Jupyter Notebook to teach and illustrate network programmability concepts.  The container would contain all the necessary requirements for the sample Notebook files that are included.  

This basic example targets ACI Toolkit.  

# Getting Started

## Run Published Container

1. Start container

    ```bash
    docker run -it --rm -p 8888:8888 hpreston/jupyter_test
    ```

1. Navigate to the URL output.  

    ```bash
    # Example
    $ docker run -it --rm -p 8888:8888 hpreston/jupyter_test
    [I 15:50:15.408 NotebookApp] Writing notebook server cookie secret to /root/.local/share/jupyter/runtime/notebook_cookie_secret
    [I 15:50:15.437 NotebookApp] Serving notebooks from local directory: /notebook
    [I 15:50:15.437 NotebookApp] 0 active kernels
    [I 15:50:15.437 NotebookApp] The Jupyter Notebook is running at:
    [I 15:50:15.437 NotebookApp] http://0.0.0.0:8888/?token=518558720d734713fabe89a5a6dc4d7f88cf224dc2095df4
    [I 15:50:15.437 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
    [W 15:50:15.438 NotebookApp] No web browser found: could not locate runnable browser.
    [C 15:50:15.438 NotebookApp]

        Copy/paste this URL into your browser when you connect for the first time,
        to login with a token:
            http://0.0.0.0:8888/?token=518558720d734713fabe89a5a6dc4d7f88cf224dc2095df4
    ```

## Running Locally - No Docker

1. Clone down the repo

  ```bash
  git clone https://github.com/hpreston/jupyter_test
  cd jupyter_test
  ```

1. Setup Python Virtual Environment.  Python 2.7 should work as well.  

    ```bash
    virtualenv venv --python=python3.6
    source venv/bin/activate
    pip install jupyter
    ```

1. Start Jupyter.  Should open the web browser window automatically, if it doesn't navigate to the link listed in the output.  

    ```bash
    jupyter notebook
    ```
    
# jupyter_test
