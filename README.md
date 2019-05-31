# PicoBank Travel Architecture Documentation Experiment


##  Building the documentation

    docker run --rm -it --entrypoint /bin/bash -v ${PWD}:/project rdmueller/doctoolchain:v1.1.0 -c "doctoolchain . -PmainConfigFile=/Config.groovy -PdocDir=/project -PpdfThemeDir=/project/src/docs/pdfTheme generatePDF --info && exit"
    
For now, pandoc is not included in the Docker image so on MacOSX:

    cd build/docbook/
    pandoc -r docbook -t docx -o ../docx/arc42-template.docx arc42-template.xml

## Dependencies

### Included

* [C4 PlantUML](https://github.com/RicardoNiepel/C4-PlantUML)
* [Azure PlantUML](https://github.com/RicardoNiepel/Azure-PlantUML)

### To look into

* https://github.com/Roemer/plantuml-office
