Para ver una lista detalladas del total de Tags vaya [[Tag List#Tags List Count|Aqui]]
### Personal

| Type | Name        | Purpose                                                         |
| ---- | ----------- | --------------------------------------------------------------- |
|      | #Finanzas   | Informacion sobre finanzas personal y cosas que aprender        |
|      | #Personales | Temas personas, Tareas o mas                                    |
|      | #Leer       | Informacion para leer ya sea articulos o libros                 |
|      | #Investigar | Investigar sobre algo nuevo                                     |
|      | #Videos     |                                                                 |
|      | #Daily      | Este Tags se utiliza para las notas diarias                     |
|      | #Unique     | Este se utiliza para notas unicas que no tengan ningun otro tag |
|      | #Weekly     | Este Tags se utiliza para las notas Semanales                   |
|      | #Monthly    | Notas Mensuales                                                 |
|      | #BookNotes  |                                                                 |


### Study Project Management

| Type       | Name               | Purpose                                           |
| ---------- | ------------------ | ------------------------------------------------- |
| Salesforce | #ProjectManagement | Identificar el contenido relacionado a Salesforce |
|            | #PmNotes           |                                                   |
### Study 

| Type       | Name                                    | Purpose                                         |
| ---------- | --------------------------------------- | ----------------------------------------------- |
| Flashcards | #ProjectManagementReview<br>#Flashcards | Este tag es usado para identificar flashcardads |
|            | #ProjectManagementReview                |                                                 |
|            |                                         |                                                 |
|            |                                         |                                                 |
|            |                                         |                                                 |
### Tags List Count 

```dataviewjs
const EXCLUDED_FOLDERS = ["folder 1", "folder 2", "folder 3"];
const fields = {};

for (let [path, metadata] of app.vault.getMarkdownFiles().map(file => [file.path, app.metadataCache.getFileCache(file)])) {
  if (!EXCLUDED_FOLDERS.some(folder => path.startsWith(folder))) {
    (metadata.tags || []).forEach(tag => {
      fields[tag.tag] = (fields[tag.tag] || 0) + 1;
    });    
  }
}

dv.header(3, 'Tags');
dv.list(Object.keys(fields)
  .sort((a, b) => fields[b] - fields[a])
  .map(tag => `${tag} (${fields[tag]} notes)`));
  ```

