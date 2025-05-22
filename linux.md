# linux
## initialize 
```
sudo cp ./dlc.dat /var/snap/v2raya/43/geoip/geosite.dat
sudo cp ./geoip.dat /var/snap/v2raya/43/geoip/geoip.dat
https://xeno4.top/api/v1/client/subscribe?token=4b4d95cbbb4981c8873bf1da05a5e34d
sudo apt-get update
sudo apt-get upgrade
```

## ROS-NOETIC
```
wget http://fishros.com/install -O fishros && . fishros
```

## install CUDA
```
sudo sh cuda_12.4.0_550.54.14_linux.run

export CUDA_HOME=/usr/local/cuda-12.4
export PATH=$CUDA_HOME/bin:$PATH
export LD_LIBRARY_PATH=$CUDA_HOME/lib64:$LD_LIBRARY_PATH
```

## git
### config git
```
git config --global user.name "zhenzhen1419"
git config --global user.email "xiaodoudou1419@gmail.com"
```
### Failed to connect to github.com port 443
```
git config --global http.proxy 127.0.0.1:20171
git config --global https.proxy 127.0.0.1:20171
```

## conda spatiallm
### ImportError: /lib/x86_64-linux-gnu/libstdc++.so.6: version `GLIBCXX_3.4.29' not found (required by /home/doudou/anaconda3/envs/spatiallm/lib/python3.11/site-packages/torchsparse/backend.cpython-311-x86_64-linux-gnu.so)
```
strings /usr/lib/x86_64-linux-gnu/libstdc++.so.6 | grep GLIBCXX
sudo find / -name "libstdc++.so.6*"
strings /home/zhenzhen/anaconda3/lib/libstdc++.so.6.0.29 | grep GLIBCXX
sudo cp /home/zhenzhen/anaconda3/lib/libstdc++.so.6.0.29 /usr/lib/x86_64-linux-gnu/
sudo rm /usr/lib/x86_64-linux-gnu/libstdc++.so.6
sudo ln -s /usr/lib/x86_64-linux-gnu/libstdc++.so.6.0.29 /usr/lib/x86_64-linux-gnu/libstdc++.so.6
```

## conda pointllm
### install torch
```
pip install transformers==4.28.0
pip install torch==2.0.1 torchvision==0.15.2 torchaudio==2.0.2 --index-url https://download.pytorch.org/whl/cu117
```
### install flash attn
```
pip install flash-attn==2.3.0
pip install numpy==1.23.5
```
