# tltTotrtOnNanoInstall
#1: nvcc-V installation

install_basics.sh

https://github.com/jkjung-avt/jetson_nano/blob/master/install_basics.sh
#!/bin/bash	
	set -e
	if ! grep 'cuda/bin' ${HOME}/.bashrc > /dev/null ; then
	echo "** Add CUDA stuffs into ~/.bashrc"
	echo >> ${HOME}/.bashrc
	echo "export PATH=/usr/local/cuda/bin:\${PATH}" >> ${HOME}/.bashrc
	echo "export LD_LIBRARY_PATH=/usr/local/cuda/lib64:\${LD_LIBRARY_PATH}" >> ${HOME}/.bashrc
	fi


Jetson Nano上的“ / usr / local / cuda / bin”中应该已经存在“ nvcc”。只需将其添加到您的PATH中即可。
add the following to your ${HOME}/.bashrc
export PATH=/usr/local/cuda/bin:\${PATH}
export LD_LIBRARY_PATH=/usr/local/cuda/lib64:\${LD_LIBRARY_PATH}


参考：https : //github.com/jkjung-avt/jetson_nano/blob/master/install_basics.sh 

Now reload your terminal config :
    source ~/.bashrc
    sudo ldconfig
    
    
    
    
#2:pycuda installation (this repo code)

https://github.com/jkjung-avt/tensorrt_demos/blob/master/ssd/install.sh 

#3:TRT OSS installation

https://docs.nvidia.com/metropolis/TLT/tlt-getting-started-guide/index.html#tensorrt_oss

