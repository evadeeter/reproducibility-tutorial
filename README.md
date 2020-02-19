# reproducibility-tutorial
foss tutorial feb 2020
    1  cd /scratch
    2  df -h
    3  pwd
    4* get clone "https://github.com/evadeeter/reproducibility-tutorial.git"
    5  git clone "https://github.com/evadeeter/reproducibility-tutorial.git"
    6  ls
    7  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    8  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
    9  ln -s /opt/conda/pkgs/*/bin/* /bin
   10  ln -s /opt/conda/pkgs/*/lib/* /usr/lib
   11  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
   12  /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
   13  /opt/conda/bin/pip install bash_kernel
   14  /opt/conda/bin/pip install ipykernel
   15  /opt/conda/bin/python3 -m bash_kernel.install
# tried some things that didn't work
   16  conda search  jupyterlab
   17  conda search jupyterlab
   18  conda search <jupyterlab>
   19  conda search qiime
   20  conda search htseq
   21  search htseq
   22  /opt/conda  search qiime
   23  /opt/conda search qiime
   24  /opt/conda/bin/conda search qiime
# this one worked because blah blah
   25  /opt/conda/bin/conda search -c bioconda qiime
   26  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   27  /opt/conda/bin/conda search -c bioconda snakemake
   28  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   29  ln -s /opt/conda/lib/* /usr/lib
   30  snakemake --version
   31  ln -s /opt/conda/bin/* /bin
   32  snakemake --version
   33  sudo apt-get update
   34  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   35  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   36  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
   37  sudo apt-get update
   38  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   39  docker run hello-world
   40  cd /scratch/reproducibility-tutorial/
   41  history >>README.md
