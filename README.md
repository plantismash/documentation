# plantiSMASH Documentation 

The documentation of the plant genome-mining tool [plantiSMASH](https://plantismash.bioinformatics.nl/) 

To publish the documentation follow the [GitHub workflow](./.github/workflows/publish.yml)

Check the deployment status of the last push at [Deploy MKdocs](https://github.com/plantismash/documentation/actions/workflows/publish.yml)

Visit the website with the documentation at [plantiSMASH documentation](https://plantismash.github.io/documentation/) 

This documentation is originally sources from the [antiSMASH documentation](https://docs.antismash.secondarymetabolites.org/)

### Run Mkdocs locally 

Create a conda environment with the Mkdocs required dependencies 

``` 
conda create -n plantidocs python=3.9
conda activate plantidocs 
pip install -r requirements.txt
```

Start the local MkDocs server:
```
mkdocs serve 
```
Open your browser and go to:
[http://127.0.0.1:8000/](http://127.0.0.1:8000/)

Stop the server: 
```
Ctrl+C
```

### License

See [LICENSE](LICENSE)

### Authors

- Elena Del Pup <elenadelpup@gmail.com>
