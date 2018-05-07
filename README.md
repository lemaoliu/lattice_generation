# lattice generation from a kbest list using srilm toolkit

## Running 
```
./nbest-lattice -rescore data/kbest.res -dump-posteriors -write data/lattice.res -use-mesh
```
where best-lattice is a exe file in srilm toolkit, lattice.res is the output lattice, and kbest.res is the input kbest file as follows:
```
(0.33) cat sat the mat
(0.33) cat sitting on the mat
(0.33) hat on a mat
```
then the file in lattice.res is as follows:
```
name kbest.res
numaligns 5
posterior 1
align 0 cat 0.6666666666666666 hat 0.3333333333333333
align 1 *DELETE* 0.6666666666666666 sitting 0.3333333333333333
align 2 on 0.6666666666666666 sat 0.3333333333333333
align 3 the 0.6666666666666666 a 0.3333333333333333
align 4 mat 1
```
