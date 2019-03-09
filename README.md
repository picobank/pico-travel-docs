= PicoBank Travel Architecture Documentation Experiment

== Building the documentation

    docker run --rm -it --entrypoint /bin/bash -v ${PWD}:/project rdmueller/doctoolchain:v1.1.0 -c "doctoolchain . -PmainConfigFile=Config.groovy --info  && exit"

For now, pandoc is not included in the Docker image so on MacOSX:

    cd build/docbook/
    pandoc -r docbook -t docx -o ../docx/arc42-template.docx arc42-template.xml
