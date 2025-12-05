## Instruction to compile and run:

COnnect to Leonardo with the command:

 ssh <username>

 <insert password>

Run the command:
 
 cd OpenMp

- In thr folder there are some files named "job#XXXX". The number in the name states for the number of threads desired for our simulation.

- In the jobs there are commands to load the modules needed for NetCDF4 and for the compiler and to compile run the code:
  
  module load netcdf-fortran/4.6.1--openmpi--4.1.6--gcc--12.2.0-spack0.22
  module load gcc/12.2.0
  make
  srun ./model

- The command "make" runs the Makefile in the folder to compile the program, while the "srun ./model" command runs the executable

- In the folder there is also a file named "namelist.in". In the file, it is possible to set the domain size, the simulation time and output 
  frequency in input.

- After running it, the output.nc file will be created

- To open the .nc file, it is possible to push the file to a web repo, then pull it to a local system and open it with the command:
  
  ncview output.nc

- Itv is also possible to open a Doxygen docuementation in the current folder by running: 
  doxygen doxy.in

- then open the html folder and open the file files.html

