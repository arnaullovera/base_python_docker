# minimal instalation from debian
# gets curl, conda, 
FROM conda/miniconda3:latest

RUN mkdir projects && \
    mkdir projects/project_name && \
    mkdir projects/project_name/data && \
    mkdir projects/project_name/code && \
    mkdir projects/project_name/settings && \
    mkdir projects/project_name/enviroment && \
    mkdir projects/project_name/outputs

# install dependencies one by one
RUN conda update -n base -c defaults conda && \
    conda install -y -c anaconda scipy && \
    conda install -y -c anaconda numpy && \
    conda install -y -c anaconda pandas && \
    conda install -y -c anaconda scikit-learn
# or create an enviroment from yml file
# COPY envrequirements.yml projects/settings

# COPY data/* projects/data
# COPY src/ /projects/code/

VOLUME /home/arnaullovera/Docker/pyapp/:/projects/project_name/code/

WORKDIR /projects/project_name/

CMD ["python", "code/test.py"]

