# 4-Qubit Grover Implementation

Minimal implementation of Grover’s algorithm on a 4-qubit system.

Originally written in 2020. Quantum libraries (notably Qiskit) have since evolved, so parts of the codebase may be outdated and require refactoring to run on current versions.

## Overview

This project implements Grover’s search algorithm using explicit circuit construction and state evolution.

Focus:
- amplitude amplification dynamics
- behaviour across iterations
- small-scale, fully observable system

This is not meant as a production-ready quantum application, but as a controlled setting to study search/optimisation behaviour.

## Notes on Implementation

- Built at a time when Qiskit APIs differed significantly from current versions  
- Some components may break under latest releases  
- Refactoring to modern Qiskit is required  

## Related Work

A more formal and complete implementation can be found here:  
http://www.diva-portal.org/smash/get/diva2:1214481/FULLTEXT01.pdf

## Status

Archived prototype. Useful as:
- reference implementation  
- starting point for updated versions  
- simple testbed for algorithmic behaviour  

## TODO

- Refactor to latest Qiskit API  
- Add reproducible experiments / outputs  
- Clean structure and modularise circuit components  
