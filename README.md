# mvt
Minimum Variability Timescale, from Golkhou et al.

from haar_power_mod import haar_power_mod
from numpy import loadtxt

file='grb_lc.txt.gz'
t,r,dr = loadtxt(file,unpack=True,usecols=(0,2,3))

haar_power_mod(r,dr,min_dt=1.e-4,max_dt=100.,tau_bg_max=0.01,nrepl=2,doplot=True,bin_fac=4,zerocheck=False,afactor=1.,snr=3.,verbose=True,weight=True,file='test')
