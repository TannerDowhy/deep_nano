BootStrap: yum
OSVersion: 7
MirrorURL: http://mirror.centos.org/centos-%{OSVERSION}/%{OSVERSION}/os/$basearch/
Include: yum

%post
    yum -y groupinstall "Development Tools"
    yum -y install zlib-devel
    yum -y install https://centos7.iuscommunity.org/ius-release.rpm
    yum -y update
    yum -y install python-devel
    yum -y install python-pip
    yum -y install hdf5-devel
    yum -y install wget

    pip install Cython==0.23.4 numpy h5py==2.5.0 Theano==0.8.0 python-dateutil==2.5.0 scipy scikit-learn

    git clone https://bitbucket.org/vboza/deepnano.git
    echo -e "\n[global]\nfloatX=float32\n" >> ~/.theanorc
    wget http://www.netlib.org/blas/blas-3.8.0.tgz
    tar xzfv /blas-3.8.0.tgz
    make -C /blas-3.8.0
