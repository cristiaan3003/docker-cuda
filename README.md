docker-cuda
===========

Minimal container with CUDA drivers as a base for GPU computing.

Installs only the driver without the enourmous toolkit. I use this as a base for Folding and BOINC images, but it could certainly be used elsewhere.

### Usage:

On a host with a CUDA device and drivers.

	docker run \
	  --device=/dev/nvidia0:/dev/nvidia0 \
	  --device=/dev/nvidiactl:/dev/nvidiactl \
	  --device=/dev/nvidia-uvm:/dev/nvidia-uvm \
	  -it \
	  --rm cuda-base

Or, as the base of another image.

	FROM ozzyjohnson/cuda

### Next:

- Surely there's direct link to driver only download somewhere on the developer site. The package I'm using is 900MB.
