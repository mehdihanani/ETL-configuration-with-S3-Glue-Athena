# ETL-configuration-with-S3-Glue-Athena
analyser un fichier client excel qui contient des données clients en utilisant AWS services 

Voici l'architecture qu'on va utiliser : 

<img width="608" alt="image" src="https://github.com/user-attachments/assets/7b37105a-72a7-4f21-9614-c80604417bd5" />


1 - 2 - 3 
- Creating 3 - S3 bucket (ETL source/target - athena store) "standard configuration"
- Create IAM role (create new role) allows Glue (service) to other AWS services (S3) with two policies (S3 and Glue)
- Upload the file(csv) to S3 bucket source, don't forget to add a new folder in the main folder before uploading the file.
- go AWS Glue and create Crawler (un outil qui 'lit' et 'comprend' les données afin de les rendre prêtes à être analysées ou transformées) then create a database table as a target pour placer les métadonnées

4 - 5 - 6 - 7
- Transform the data from Source to Target so we need to create a Job ETL
Otherwise
- you can just query from S3 source.
