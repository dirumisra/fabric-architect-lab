# RCA-0001 - Fabric CLI Path Collision

## Symptom

Running:

fab auth login

returned:

Can't find any collection named 'fabfile'!

## Investigation

Multiple Python environments and executables were present.

The original `fab` command resolved to a Python Fabric deployment package instead of Microsoft Fabric CLI.

## Root Cause

PATH and Python environment collision between:

- Anaconda base environment
- User Python installation
- Project virtual environment

## Resolution

Created and activated a dedicated project virtual environment:

.venv

Installed Microsoft Fabric CLI inside that environment and verified that:

which fab

resolved to the project virtual environment.

## Preventive Action

Project-specific Python and Fabric automation dependencies must be installed inside the project virtual environment rather than the global or Anaconda base environment.
