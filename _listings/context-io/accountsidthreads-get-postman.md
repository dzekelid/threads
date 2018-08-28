{
  "info": {
    "name": "Context.IO Get Accounts Threads",
    "_postman_id": "4240ee1a-7f71-4fb7-99a7-9cd469a9f894",
    "description": "Lists threads on an account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Accounts",
      "item": [
        {
          "id": "4ea786b2-04c1-4c90-912a-fae2bd68a1c2",
          "name": "listAccounts_",
          "request": {
            "url": "http://api.context.io/2.0/accounts?email=%7B%7D&limit=%7B%7D&offset=%7B%7D&status=%7B%7D&status_ok=%7B%7D&token=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists accounts."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "830559cf-d674-420f-9082-5df02f12b80b"
            }
          ]
        },
        {
          "id": "ca1ee6a6-5b28-4399-a81c-9837735b28c7",
          "name": "addAccount_",
          "request": {
            "url": "http://api.context.io/2.0/accounts?email=%7B%7D&first_name=%7B%7D&last_name=%7B%7D&token=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Adds a new account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cf2807b3-29cc-419d-a93a-3069e6b7c59b"
            }
          ]
        },
        {
          "id": "97b18903-dcb0-42a6-b31d-45badb2f08e9",
          "name": "getAccount_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets details about a given account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ffd89268-52ec-4e87-b7ad-1842dd96d86c"
            }
          ]
        },
        {
          "id": "ab62b22b-48b0-4ce5-838f-1c31acba491e",
          "name": "modifyAccount_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id"
              ],
              "query": [
                {
                  "key": "first_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "last_name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Modifies a given account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1bdac309-b556-4915-851b-a681a8f1567d"
            }
          ]
        },
        {
          "id": "79e8bcb7-fd14-490d-bf18-03a98eda4a43",
          "name": "removeAccount_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Removes a given account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0940fc32-3b95-46b0-9162-8fc03922062d"
            }
          ]
        },
        {
          "id": "d8a62375-ba80-403b-afd9-f0798f7c75e5",
          "name": "listAccountConnectTokens_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/connect_tokens"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists connect tokens created for an account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "662587ed-a106-4200-a69b-438d11eec07a"
            }
          ]
        },
        {
          "id": "6b8818de-d7ee-4d32-86e5-2af9f7bd666e",
          "name": "Create_obtainNewAccountConnectToken_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/connect_tokens"
              ],
              "query": [
                {
                  "key": "callback_url",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "email",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "first_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "last_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "service_level",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Obtains a new connect_token for a specific account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5c11e93a-e653-477b-b707-d6a35879b649"
            }
          ]
        },
        {
          "id": "7926b0fa-5d7d-4af6-95d2-ddbed7a36190",
          "name": "getAccountConnectToken_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/connect_tokens/:token"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "token",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a given connect token."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b8d2dfd6-4cf0-4e24-bbc6-8d6a47fc3fee"
            }
          ]
        },
        {
          "id": "5ccecbd9-59a1-42f4-ab44-8b9fae4d3d3e",
          "name": "removeAccountConnectToken_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/connect_tokens/:token"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "token",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Remove a given connect token."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a99cde79-ea1c-4acc-8319-4d37e3b2925d"
            }
          ]
        },
        {
          "id": "050e3594-a5e3-4d61-a6fe-c8fc4e3d73ce",
          "name": "listAccountContacts_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/contacts"
              ],
              "query": [
                {
                  "key": "active_after",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "active_before",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "search",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists contacts in an account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "adaae36f-de51-4a38-b81a-e6a6a0d95647"
            }
          ]
        },
        {
          "id": "5495c605-5731-4cb1-b396-a1eaa3a35571",
          "name": "getAccountContact_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/contacts/:email"
              ],
              "variable": [
                {
                  "id": "email",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a given contact."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "75e2baca-40ec-4af9-b83a-7b7186a52f1a"
            }
          ]
        },
        {
          "id": "95d9d4ea-b2ff-44de-ac80-b74c3d280982",
          "name": "listAccountContactFiles_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/contacts/:email/files"
              ],
              "query": [
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "email",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists files exchanged with a contact. Returns the latest attachments exchanged with one or more email addresses. By \"exchanged with Mr. X\" we mean any file attached to an email received from Mr. X, sent to Mr. X or sent by anyone to both Mr. X and the mailbox owner."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "93ab827f-aabf-4a3c-81a9-cd6d561b6f19"
            }
          ]
        },
        {
          "id": "cd323e7c-690c-4263-b390-9d6b90840a77",
          "name": "listAccountContactMessages_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/contacts/:email/messages"
              ],
              "query": [
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "email",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists messages where a contact is present. Returns the latest email messages exchanged with one or more email addresses. By \"exchanged with Mr. X\" we mean any email received from Mr. X, sent to Mr. X or sent by anyone to both Mr. X and the mailbox owner."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d2b11d78-c16d-430a-96c2-99f981f24c30"
            }
          ]
        },
        {
          "id": "8364b0f4-831e-474b-bace-0b208453103e",
          "name": "listAccountContactThreads_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/contacts/:email/threads"
              ],
              "query": [
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "email",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists threads where a contact is present. Returns the latest email threads exchanged with one or more email addresses. By \"exchanged with Mr. X\" we mean any email received from Mr. X, sent to Mr. X or sent by anyone to both Mr. X and the mailbox owner."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f612ce74-e346-481f-b71e-78456a29168b"
            }
          ]
        },
        {
          "id": "d3f49471-66a9-43ba-93c2-addc314ebaef",
          "name": "listAccountEmailAddresses_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/email_addresses"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists email addresses used by an account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9b331c06-1cf3-4133-aafe-80a83bcff89a"
            }
          ]
        },
        {
          "id": "8e760907-56e6-4b36-8f4b-f0e8731c9eb8",
          "name": "addAccountEmailAddress_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/email_addresses"
              ],
              "query": [
                {
                  "key": "email_address",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Adds a new email address as an alias for an account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a22418ad-d569-4317-a1af-999674d14c06"
            }
          ]
        },
        {
          "id": "c2ab1de7-fa00-41e6-b47f-95cfd485a869",
          "name": "Create_setAccountEmailAddressAsPrimary_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/email_addresses/:email"
              ],
              "query": [
                {
                  "key": "primary",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "email",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Makes this email address the primary one for the account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "74657150-0a3c-4ba6-9d6b-f2c78c567cf4"
            }
          ]
        },
        {
          "id": "a334ceec-3e01-4129-923a-e8e6a719803b",
          "name": "removeAccountEmailAddress_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/email_addresses/:email"
              ],
              "variable": [
                {
                  "id": "email",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Removes an email address form the aliases of an account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6d72737f-0738-47a3-81e8-0a92b309a198"
            }
          ]
        },
        {
          "id": "249d9899-388e-4b05-a531-b9e3eb11d295",
          "name": "listAccountFiles_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/files"
              ],
              "query": [
                {
                  "key": "bcc",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "cc",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "date_after",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "date_before",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "email",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "file_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "from",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "group_by_revisions",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "indexed_after",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "indexed_before",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "to",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists files found as email attachments. List filters: each of the email, to, from, cc and bcc parameters can be set to a comma-separated list of email addresses. These multiple addresses are treated as an OR combination. You can set more than one parameter when doing this call. Multiple parameters are treated as an AND combination."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e92c7a5e-44a9-4594-ab50-a01067476674"
            }
          ]
        },
        {
          "id": "3b069a0d-3626-4325-aa45-b7e01dec963d",
          "name": "getAccountFile_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/files/:fileId"
              ],
              "variable": [
                {
                  "id": "fileId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about a given file."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1a74bdbc-7d37-4746-8e5f-09a7bd70b64a"
            }
          ]
        },
        {
          "id": "4bb41bae-d60b-4aaf-b20c-f33d42096d3c",
          "name": "listComparableAccountFiles_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/files/:fileId/changes"
              ],
              "variable": [
                {
                  "id": "fileId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists files that can be compared with a given file."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5732fd0f-a3d7-4d67-ad39-51abe6eab5fe"
            }
          ]
        },
        {
          "id": "640d3f5b-540a-49d7-add6-9fe996666f30",
          "name": "getAccountFileContent_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/files/:fileId/content"
              ],
              "variable": [
                {
                  "id": "fileId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Downloads a given file. Returns the content a given attachment. On-demand data retrieval: since we do not keep full copies of attachments on our servers, the file has to be retrieved from the IMAP server when this call is made. If the IMAP server is unreachable at the time the call is made, this call will return an error."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e324241d-13c5-4d6b-94c0-a8165c2203dc"
            }
          ]
        },
        {
          "id": "7aa19a31-7cdf-461a-9159-5199b2166faf",
          "name": "listAccountFileRelatedFiles_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/files/:fileId/related"
              ],
              "variable": [
                {
                  "id": "fileId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists other files related to a given file. Returns a list of files that are related to the given file. Currently, relation between files is based on how similar their names are."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b57e5603-fbbf-4c73-87ba-99bc17ef9808"
            }
          ]
        },
        {
          "id": "7702346c-f65f-4168-98f8-38f8844ef85a",
          "name": "listAccountFileRevisions_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/files/:fileId/revisions"
              ],
              "variable": [
                {
                  "id": "fileId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists other revisions of a given file. Returns a list of revisions attached to other emails in the mailbox for a given file. Two files are considered revisions of the same document if their file names are identical outside of revision indicators such as dates, author initials, version numbers and keywords like \"final\" or \"draft\"."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cdaf2cbe-5fa2-4736-ba39-eb869b17172c"
            }
          ]
        },
        {
          "id": "9e790dd2-d7dd-4070-a0d7-a42b5bfa431a",
          "name": "listAccountMessages_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/messages"
              ],
              "query": [
                {
                  "key": "bcc",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "body_type",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "cc",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "date_after",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "date_before",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "email",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "folder",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "from",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "include_body",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "include_flags",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "include_headers",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "indexed_after",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "indexed_before",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "subject",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "to",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists email messages for an account. List filters: each of the email, to, from, cc and bcc parameters can be set to a comma-separated list of email addresses. These multiple addresses are treated as an OR combination. You can set more than one parameter when doing this call. Multiple parameters are treated as an AND combination."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d0de12e3-6b00-45ce-b8e3-4969f5b3e8b8"
            }
          ]
        },
        {
          "id": "c8d1a85b-7350-4b7e-9ccd-1b1c3ab1c52d",
          "name": "getAccountMessage_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/messages/:message_id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "message_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the file, contact and other information about a given email message. As specified in the RFC822, the < and > at the beginning and end of the Message-ID are part of the value and should be included if you're putting an email_message_id in the url."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e34b8338-3698-4773-9db7-9bc13d555e19"
            }
          ]
        },
        {
          "id": "7d3bf964-e18b-4587-8d42-f027f802be95",
          "name": "Create_copyMoveAccountMessage_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/messages/:message_id"
              ],
              "query": [
                {
                  "key": "dst_folder",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "dst_source",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "move",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "message_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Copies or moves a message. Allows you to copy or move a message between folders. If there are more than one sources on the account, you can use this call to copy/move the message between these sources. In this case, the dst_label parameter must identify the source you want to message to be copied/moved to."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a9339ffb-8cc0-4eb0-9545-38975f76534c"
            }
          ]
        },
        {
          "id": "b676e921-dd93-45e5-b398-51177a2d0adc",
          "name": "getAccountMessageBody_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/messages/:message_id/body"
              ],
              "query": [
                {
                  "key": "type",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "message_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches the message body of a given email. On-demand data retrieval: since we do not keep full copies of emails on our servers, this call triggers a connection to the IMAP server to fetch the message. One thing to point out is we do fetch messages in such a way that large files attached to a message won't make any difference in the response time. This call only returns text portions of messages, attachments aren't included. To get a list of attachments on the message, look for the files property in the response of a message instance. To download the content of these attachments, use the files/content call."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d7434d8b-b9c3-49b8-9d7f-6747743c245d"
            }
          ]
        },
        {
          "id": "c1b6025a-55fc-4df3-9658-83684ad28881",
          "name": "getAccountMessageSource_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/messages/:message_id/source"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "message_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches the message source. Returns the raw RFC-822 message source for the message (including attachments) with no parsing or decoding to any portions of the message. On-demand data retrieval: since we do not keep full copies of emails on our servers, this call triggers a connection to the IMAP server to fetch the message. Attachments are part of the message source so they will impact how fast this call responds."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "61bcb6e0-8f19-4075-9109-b97bc7e0fe1f"
            }
          ]
        },
        {
          "id": "4e33374a-dbdb-4a72-863d-6e433f13190b",
          "name": "listAccountMessageFlags_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/messages/:message_id/flags"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "message_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists message flags for an account. On-demand data retrieval: to ensure up-to-date values, flags are not cached by Context.IO. This call triggers a connection to the IMAP server to fetch the current message flags before it returns."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a2daf3fe-befc-4e5b-bbfd-f68063d3d567"
            }
          ]
        },
        {
          "id": "b7af66ec-334c-4509-9a91-83e9964abd75",
          "name": "Create_setAccountMessageFlags_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/messages/:message_id/flags"
              ],
              "query": [
                {
                  "key": "answered",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "deleted",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "draft",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "flagged",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "seen",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "message_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Sets message flags for a given email."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "91ab630d-7f58-4632-b1da-8136f025e0a2"
            }
          ]
        },
        {
          "id": "86007434-d58c-4119-a0e3-f1e985d06377",
          "name": "listAccountMessageHeaders_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/messages/:message_id/headers"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "message_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists complete headers of a given email message. On-demand data retrieval: since we do not keep full copies of emails on our servers, this call triggers a connection to the IMAP server to fetch the message headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "65cd264d-269a-448c-80ee-cde9955e5854"
            }
          ]
        },
        {
          "id": "c5101c0c-7aa2-4888-a1cf-3faa66c9136e",
          "name": "getAccountMessageThread_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/messages/:message_id/thread"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "message_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about all messages of the thread a given message is in. This returns an array with the same structure as getting information on a single message for every message in the thread."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "74766a30-002f-45aa-871c-505a885ae745"
            }
          ]
        },
        {
          "id": "6cc625ef-f5c0-4581-bae0-9f01f1170cfd",
          "name": "listAccountSources_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/sources"
              ],
              "query": [
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "status_ok",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists IMAP sources assigned for an account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b8bbdf35-7782-4344-a3ca-474afbbfda95"
            }
          ]
        },
        {
          "id": "a131cfc2-3300-4a8a-83bc-e0a929745c63",
          "name": "addAccountSource_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/sources"
              ],
              "query": [
                {
                  "key": "email",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "password",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "port",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "provider_consumer_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "provider_token",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "provider_token_secret",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "server",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "service_level",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sync_period",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "type",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "username",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "use_ssl",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Adds an IMAP account to a given account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "67789a9e-9060-4a75-b630-161b1ac7a7b6"
            }
          ]
        },
        {
          "id": "26c38f48-74ac-4b2d-9642-e2a7c263d2d7",
          "name": "getAccountSource_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/sources/:label"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "label",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets parameters and status for an IMAP source."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8868150d-7b71-4123-8a24-73cc53963a8c"
            }
          ]
        },
        {
          "id": "b2911b1e-7906-4156-8442-8e36eca11c39",
          "name": "modifyAccountSource_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/sources/:label"
              ],
              "query": [
                {
                  "key": "password",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "provider_consumer_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "provider_token",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "provider_token_secret",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "service_level",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sync_period",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "label",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Modifies a data source on a given account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "418c9700-aa35-49ec-857e-6567b30880cc"
            }
          ]
        },
        {
          "id": "d80581c2-77bf-40ae-8885-38cd88c655fd",
          "name": "removeAccountSource_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/sources/:label"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "label",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Removes a data source of an account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4c958737-873b-4a02-a0a2-d8e1cbe8be49"
            }
          ]
        },
        {
          "id": "7f71d630-a136-41ca-9546-a3367ff86832",
          "name": "listAccountSourceFolders_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/sources/:label/folders"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "label",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists folders in an IMAP source. Returns folders existing in a given IMAP account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0495eb04-2fb8-47f0-a0c4-cf39c380f2e3"
            }
          ]
        },
        {
          "id": "d6e86f96-277a-46a2-9f08-03b36dd1a902",
          "name": "createAccountSourceFolder_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/sources/:label/folders/:folder"
              ],
              "query": [
                {
                  "key": "delim",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "folder",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "label",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a folder on an IMAP source. A new folder can be added to an IMAP source by PUTting the desired path under the sources/folders resource.\nWorking with server-specific hierarchy delimiters:\nIMAP servers are free to use the character they want as the folder hierarchy delimiter. The bad news is they don't use the same. The good news is you don't need to know this, we take care of it.\n\nThen what is that delim parameter for?\nGood question. By default, we expect you to specify the folder hierarchy using / as the hierarchy delimiter. For example, to create a folder called my folder under the folder base folder, you would call:\nPUT /2.0/accounts/<id>/sources/<label>/folders/base+folder/my+folder\n\nNo matter what's the actual hierarchy delimiter the IMAP server expects, this call will work. However, say you need to use another character as the delimiter, here's how you'd do it:\nPUT /2.0/accounts/<id>/sources/<label>/folders/base+folder.my+folder?delim=.\n\nBoth examples above are equivalent and will have the same result no matter what the IMAP server expects as the actual hierarchy delimiter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "28058aa1-a4a9-41d5-8c1e-85912c4a9844"
            }
          ]
        },
        {
          "id": "ed32b901-be57-4236-a636-703e9d27515f",
          "name": "getAccountSourceSyncStatus_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/sources/:label/sync"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "label",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the sync status of a data source. Returns the timestamps for the last time the source has been synced with the origin mailbox."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8591634d-e28c-475d-aa73-402e902e6b86"
            }
          ]
        },
        {
          "id": "950a5c1c-bbe2-4e28-9e29-b08bc160b5d3",
          "name": "Create_syncAccountSource_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/sources/:label/sync"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "label",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Triggers a sync of a data source. This will start a sync job for the source."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "56b59ce3-a612-4dac-8442-f17993ceeadd"
            }
          ]
        },
        {
          "id": "be8a9fe7-49d1-4028-bc3b-dd6c73d77d71",
          "name": "getAllAccountSourcesSyncStatus_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/sync"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the sync status for all sources of the account. Returns the timestamps for the last time a source has been synced with the origin mailbox."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "57051dd9-e58a-468d-85f9-dd84f200703f"
            }
          ]
        },
        {
          "id": "0ee3e500-115d-4cb1-be89-6cdb94f81c04",
          "name": "Create_syncAllAccountSources_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/sync"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Triggers a sync of all sources on the account. This will start a sync job for all sources under the account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "14c3ce88-39fb-47dd-90b7-012d750b0659"
            }
          ]
        },
        {
          "id": "d206ed0e-a480-48b2-b8ba-13dbe14f876c",
          "name": "listAccountThreads_",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.context.io",
              "path": [
                "2.0",
                "accounts/:id/thr