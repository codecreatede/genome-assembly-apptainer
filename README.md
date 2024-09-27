multi-sif-apptainer

- a multi sif apptainer for the genome assembly coming from the pacbiohifi reads.
- it includes the two genome assembler and one is hifiasm and the other is verkko.
- The benchmark for the assembly for these assemblers are located at my another repository [genomeasembly-pacbiohifi](https://github.com/codecreatede/genomeassembly-pacbiohifi)

- to invoke the hifiasm apptainer 
```
module load singularity
apptainer exec hifiasm.sif hifiasm
```
- to build and invoke the verkko conda based apptainer. I wrote the verkko yaml so that you can directly import and run with in the apptainer. 
```
module load singularity 
apptainer build verkko.sif verkko.def 
echo ".opt/conda/etc/profile.d/conda.sh" >> $ENV_PATH
```
- inspect the images after the build 
```
for i in *.sif; do apptainer inspect ${i}; done
``

Gaurav Sablok
