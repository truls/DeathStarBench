# DeathStarBench fork information

This fork of DeathStarBench targets arm64 compatibility. It tracks
upstream except for the following:

 - luajit (dependency of wrk2) has been bumped to version
   2.1.0-beta3 which supports arm64
 - x86-specific include has been removed form wrk2
 - docker files have been updated to reference trulsa/ dockerhub images
   which are compiled for arm64
 - wrk2 has been consolidated in the tools/wrk2 folder and the
   benchmarking scripts for the individual benchmarks can be found in
   the tools/wrk2/scripts folder
 - An arm64 build of wrk2 including the benchmarking scripts is
   available from the trulsa/wrk2 docker iamge. The wrk2 folder is
   located at `/wrk2` in the image. To use it, invoke the wrk2
   commands as
   ```
   docker run --rm --network host trulsa/wrk2 /wrk2/wrk
   ```


Original readme follows.

# DeathStarBench

Open-source benchmark suite for cloud microservices. DeathStarBench includes five end-to-end services, four for cloud systems, and one for cloud-edge systems running on drone swarms.

## End-to-end Services <img src="microservices_bundle4.png" alt="suite-icon" width="40"/>

* Social Network (released)
* Media Service (released)
* Hotel Reservation (released)
* E-commerce site (in progress)
* Banking System (in progress)
* Drone coordination system (in progress)

## License & Copyright

DeathStarBench is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, version 2.

DeathStarBench is being developed by the [SAIL group](http://sail.ece.cornell.edu/) at Cornell University.

## Publications

More details on the applications and a characterization of their behavior can be found at ["An Open-Source Benchmark Suite for Microservices and Their Hardware-Software Implications for Cloud and Edge Systems"](http://www.csl.cornell.edu/~delimitrou/papers/2019.asplos.microservices.pdf), Y. Gan et al., ASPLOS 2019.

If you use this benchmark suite in your work, we ask that you please cite the paper above.


## Beta-testing

If you are interested in joining the beta-testing group for DeathStarBench, send us an email at: <microservices-bench-L@list.cornell.edu>
