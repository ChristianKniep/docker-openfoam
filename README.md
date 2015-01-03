OpenFOAM Image
=====================


This image holds different versions of OpenFOAM based on multiple distributions.
They are encoded in git tag.

- ```u12.04_of222``` is based on Ubuntu 12.04 and holds OpenFOAM 2.2.2
- ```u14.10_of230``` is based on Ubuntu 14.10 and holds OpenFOAM 2.3.0

## Run

The Image is also capable of running sshd and slurm, but for now I will stick with the simple usage.
Just start a container like this:

```
$ CID=$(docker run -d -v /scratch:/scratch qnib/openfoam:u12)
# Afterwards connect via 'docker exec'
$ docker exec -ti ${CID} bash
cont # source /opt/openfoam*/etc/bashrc
```
