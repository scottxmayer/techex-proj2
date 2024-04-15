FROM python:3.10
WORKDIR /app 
COPY . /app
# RUN pip install --upgrade pip setuptools wheel 
# RUN pip install -v config/h5py/ 
# RUN H5PY_SETUP_REQUIRES=0 pip install .
# RUN brew update && brew install -y \
#        build-essential \
#        libhdf5-dev

COPY ./config/environment.yml . 
FROM continuumio/miniconda3 
#COPY config/environment.yml /app
RUN ls 
RUN conda env create -f /app/environment.yml
RUN /bin/bash -c "source /opt/conda/etc/profile.d/conda.sh && conda activate proj2 && pip install -r config/requirements.txt"

EXPOSE 8000
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]

