# Watson_integration_test
Para probar integración con Watson Studio. Usando el FinalAssignment del curso DS Tools.

## ACT:
Al principio daba error al tratar de publicar desde Watson Studio: "Publish on GitHub: An error occurred while publishing the notebook Try again later". 

Luego de ver: 
https://stackoverflow.com/questions/64306620/unable-to-publish-jupyter-notebook-from-ibm-watson-studio-to-github-repository

El problema estaba en que la rama en que busca publicar Watson es "master", no "main" que es la predetermninada en GitHub. Por eso no la encontraba. 
La solución fue crear la rama-hija "master", hacerla la default y borrar la rama "main".
Nota: Watson publica en "master" aunque sea una rama hija y sobreescribe el archivo si ya existe. 
