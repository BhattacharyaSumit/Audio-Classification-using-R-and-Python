# Audio-Classification-using-R-and-Python

This project tries to integrate the powers of R and Python but in a reverse fashion.  Generally, Data is preferred to be wrangled in R and the model flows are created using Python. But in this project, I have wrangled the data using Python (thinkdsp package) and the model is created in R (XGBoost package for experimenting).


### The entire work is done in Colab. 
**To use R in Colab, certains steps are required.** 

**1)** We have to run this code on Colab with runtime selected to Python 2  (with GPU if needed)
```
!apt-get install libssl-dev > /dev/null
!wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
!chmod +x ./Miniconda3-latest-Linux-x86_64.sh
!./Miniconda3-latest-Linux-x86_64.sh -b -p /conda  > /dev/null 2>&1 
!/conda/bin/conda install -c r r-rstan r-irkernel gxx_linux-64 -y -q > /dev/null 2>&1
!/conda/bin/R -e "IRkernel::installspec(name = 'python2', displayname = 'R', user = FALSE)"  > /dev/null 2>&1
!mkdir /root/.R/
!echo "CXX14FLAGS=-O3 -mtune=native -march=native -Wno-ignored-attributes -Wno-deprecated-declarations" > /root/.R/Makevars
import os
os._exit(00)

```

**2)** After the execution of the block, the session will crash. We have to terminate the session using _Runtime -> Manage Sessions_

**3)** Then, we have to Reconnect the session. Now, the new session will begin with R kernel.

