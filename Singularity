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

    pip install Cython==0.23.4 numpy h5py==2.5.0 Theano==0.8.0 python-dateutil==2.5.0

    git clone https://bitbucket.org/vboza/deepnano.git
