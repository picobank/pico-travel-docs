= PicoBank Travel Architecture Documentation Experiment

== Building the documentation

    docker run --rm -it --entrypoint /bin/bash -v ${PWD}:/project rdmueller/doctoolchain:v1.1.0 -c "doctoolchain . -PmainConfigFile=Config.groovy --info  && exit"
