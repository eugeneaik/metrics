# Description
This is a simple python script for monitoring system resourses - cpu or mem
# Dependencies
* python3
* psutil
* sys
# Installation
    git clone https://github.com/eugeneaik/metrics
    pip3 install psutil
# Examples
    $ ./metrics cpu
    user 161870.31
    nice 71764.77
    system 76578.02
    idle 20290328.55
    iowait 34188.62
    irq 0.0
    softirq 2609.51
    steal 0.0
    guest 0.0
    guest_nice 0.0

    $ ./metrics mem
    total 2088427520
    available 1231040512
    percent 41.1
    used 441147392
    free 494047232
    active 847405056
    inactive 547627008
    buffers 314208256
    cached 839024640
    shared 232751104
    slab 124375040
# Docker
It is possible to run a script as a docker container
## Build images
    docker build -t metrics .
## Run
    docker run --pid=host --volume /:/host  metrics mem
    docker run --pid=host --volume /:/host  metrics cpu
