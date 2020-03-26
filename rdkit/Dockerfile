FROM continuumio/miniconda3
MAINTAINER iwatobipen <seritaka@gmail.com>

RUN pip install --upgrade pip
RUN conda install -c rdkit/label/beta rdkit -y
RUN conda install -c conda-forge seaborn pandas scikit-learn -y
RUN conda install -c conda-forge networkx jupyter jupyterlab -y
RUN pip install py2cytoscape

WORKDIR /workdir

EXPOSE 8888


ENTRYPOINT ["jupyter-lab", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root", "--NotebookApp.token=''"]

CMD ["--notebook-dir=/workdir"]
