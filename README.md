### [![Icono](http://www.iderioja.larioja.org/imagenes/logo_iderioja_56x70.gif)](http://www.iderioja.org)  [Sharing Open Data On GitHub using FME Tool](http://iderioja.github.io/fme_oracle_to_github/ "Oracle to GitHub") 

We use [FME](http://www.safe.com/ "Safe Software") based tool to automatically update geographical git repositories. For that purpose, we designed a workbench with FME to create GeoJSON files from different spatial formats (Oracle database table in our workbench) and host them in a GitHub repository.

GitHub allows us to store [our open data] (https://github.com/iderioja/base_datos_geografica "IDErioja geographic database") and use as a collaborative mapping framework where users can contribute to the edition of the GeoJSON files (geojson.io, Chrome extension). This has huge implications for data collaboration.

The workbench exports Oracle tables to geoJSON, uses the git version control system to manage the versions of the files and the inclusion in Github.

In GitHub repository there is a layer list file [FeatureTypesToRead.txt](https://github.com/iderioja/base_datos_geografica/FeatureTypesToRead.txt "layer list") defining which Oracle tables are read and ultimately translated to geoJSON. FME reads the layer list from GitHub using Python Scripted parameter (git pull).

FME commits updated geoJSON files to GitHub in Shutdown TCL script (git push). 

The project was presented in the [FME International User Conference 2014](http://www.safe.com/fmeuc/automatic-updating-geographical-git-repositories/ "FME 2014 Conference")

More information about IDErioja project is available at:
<br />[www.iderioja.org](http://www.iderioja.org)
<br />[@iderioja](http://twitter.com/iderioja)
