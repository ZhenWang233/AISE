# AISE: A Symbolic Verifier by Synergizing Abstract Interpretation and Symbolic Execution	

AISE is a static verifier that combines abstract interpretation and symbolic execution techniques. The verification approach is based on a verification framework that combines abstract interpretation and symbolic execution in a novel way. 

## Implementation
AISE is implemented mainly based on Clam ([https://github.com/seahorn/clam](https://github.com/seahorn/clam)) and KLEE ([https://github.com/klee/klee](https://github.com/klee/klee)).
we also integrated ESBMC([https://github.com/esbmc/esbmc](https://github.com/seahorn/clam)) to handle programs with float data, because AISE is weak at handling float data. When AISE detects that the program contains float data, it will switch to ESBMC to verify such programs. Once AISE identifies the presence of floating-point data in a program, it will transition to using ESBMC for the verification of such programs. 

This artifact "aise.zip" is for AISE SV-Comp 2024. It's the first time we try to participate in SV-COMP, we only focus on a single category "Reachability-Loops".
The tool is also publicly available at https://doi.org/10.5281/zenodo.10201159.
## Usage

### verify C program
`/bin/aise <input C file>`
e.g. `./bin/aise ./bin/array-1.c`
### version
`./bin/aise --version `

## About AISE
Our approach is new and it is different from related works. Currently, AISE has no publications. The prototype of AISE is very basic, we just implemented fundamental functions, and haven't yet polished the tool at the implementation level. 
