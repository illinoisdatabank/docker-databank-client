# Supported tags and respective `Dockerfile` links

-    [`1.0`, '1' (*1.0/Dockerfile*)](https://github.com/illinoisdatabank/docker-databank-client/blob/master/Dockerfile)

# Quick reference

-    **Maintained by**:  
    [Research Data Service at Illinois](http://www.library.illinois.edu/rds/)

# What is databank-client?

This image supports uploading a file to a draft dataset in Illinois Data Bank, a public access repository for publishing research data from the University of Illinois at Urbana-Champaign. It contains a python script from [the databank client repository on GitHub](https://github.com/medusa-project/databank-client), along with an environment that supports it. For more information, see the [help page for the Illinois Data Bank API](https://databank.illinois.edu/help#api).

# How to use this image

Run the Docker image, attaching the directory your data in as a volume, providing the python script included in the image as a passed in command, with the paramters from your Illinois Data Bank dataset as arguments.

```console
$ docker run --rm -v /host/path-to-data:/tmp/data databank-client python illinois_data_bank_datafile.py my-dataset-identifier my-dataset-token /tmp/data/myfile.csv
```
This will upload your file to your draft dataset and then exit the container.

# License

View license information for [Python 3](https://docs.python.org/3/license.html).

The original work in this image is licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/deed.en_US).
