IMAGE=idia-python-3.6.img

.PHONY: bootstrap

all: bootstrap

${IMAGE}:
	sudo singularity create -s 6000 ${IMAGE}

bootstrap: ${IMAGE}
	sudo singularity bootstrap ${IMAGE} idia-python-3.6.def 

upgrade:
	sudo singularity exec --writable ${IMAGE} apt-get update
	sudo singularity exec --writable ${IMAGE} apt-get upgrade
	sudo singularity exec --writable ${IMAGE} conda update --all 
