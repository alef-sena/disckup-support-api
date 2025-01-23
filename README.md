# ClickUp API

API designed to perform activities with ClickUp by SenseUp.

## Documentation and User Manual

[API de postagem de mensagens no ClickUp (ClickUp API) - Manual do Usuário](https://www.notion.so/senseup/API-de-postagem-de-mensagens-no-ClickUp-ClickUp-API-Manual-do-Usu-rio-faa42f95f72f4c84ae22270fca3c8a0f)

## Endpoints

| Endpoint | Method | Header | Body | Query Params | Response |
|:-:|:-:|:-:|:-:|:-:|:-:|
|`/clickup/task`|`GET`|/|/|`"discordId"= "<discord_user_id>", taskId= "<task_id>"`|`{"name": "<task_name>","url": "<task_url>"}`|
|`/clickup/comment`|`POST`|`'Content-Type': 'application/json'`|`{"discordId": "<discord_user_id>","comment": "<comment>"}`|`taskId: "<task_id>"`|`{"discordUserId": "<discord_user_id>","clickupUserId": <user_id>,"taskId": "<task_id>","taskName": "<task_name>","taskUrl": "<task_url>","comment": [objects_that_form_a_formatted_comment],"attachments": [{"id": "<attachment_id>","name": "<image_name>","url": "<image_url>","contentType": "<image_type>"}]}`|
|`/clickup/mapping`|`GET`|/|/|`"mappingName"= "<mapping_name>"`|`<file_content>`|
