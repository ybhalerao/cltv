FROM jupyter/tensorflow-notebook

USER root

RUN apt-get update --fix-missing
RUN apt-get update
RUN apt-get install -y swig
RUN apt-get install -y python-dev
RUN apt-get install -y curl
RUN apt-get install -y vim
RUN apt-get install -y zip
RUN apt-get install -y unzip
RUN apt-get install -y libssl-dev
RUN apt-get install -y libcurl4-openssl-dev
RUN apt-get install -y python-dev
RUN apt-get install -y s3fs

# create a symlink for development
RUN mkdir /development
RUN chmod 777 /development
RUN ln -s /development /home/jovyan/development

USER $NB_USER

#Amazon
RUN conda install -y boto3
RUN pip install awscli
## Try twice due to an issue with pyYAML
#RUN pip install --no-deps awscli

# Python requirements
RUN pip install wget
RUN pip install html5lib
RUN pip install beautifulsoup4
RUN pip install pycurl
RUN pip install PyMySQL
RUN pip install PyStemmer
RUN pip install snowballstemmer
RUN pip install lxml
RUN pip install isodate
RUN pip install openpyxl
RUN pip install pymc3
RUN pip install lifetimes
