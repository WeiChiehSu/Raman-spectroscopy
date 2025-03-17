# Raman-spectroscopy

We use quantum espresso 7.3.1 version to calculate material superconditivy.

After installing quantum espresso, we need to install oneapi to auxiliary operating software.

# download oneapi

wget https://registrationcenter-download.intel.com/akdlm/irc_nas/18445/l_BaseKit_p_2022.1.1.119_offline.sh

wget https://registrationcenter-download.intel.com/akdlm/irc_nas/18438/l_HPCKit_p_2022.1.1.97_offline.sh

# compile oneapi

sh ./l_BaseKit_p_2022.1.1.119_offline.sh

sh ./l_HPCKit_p_2022.1.1.97_offline.sh

When we finish installing oneapi, we can start to install quantum espresso

# download quantum espresso 7.3.1

wget https://www.quantum-espresso.org/rdm-download/488/v7-3-1/c58c7d0b6d8913a0fccbbae906f6ab55/qe-7.3.1-ReleasePack.tar.gz

tar zxvf qe-7.3.1-ReleasePack.tar.gz

cd qe-7.3.1

source ~/intel/oneapi/setvars.sh

./configure

make all

make epw

When we finish installing quantum espresso, we need to install QERaman

# download QERaman

git clone https://github.com/nguyen-group/QERaman.git

source ~/intel/oneapi/setvars.sh

make pw pp ph

cd QERaman/src

make all
