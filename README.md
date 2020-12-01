# Blue Prism integration for Onify Hub API

Onify Hub integration (Web API definitions) for Blue Prism via Onify Hub REST API.

## Introduction

## What is Blue Prism?

Blue Prism is a multinational software corporation that pioneered and makes enterprise robotic process automation (RPA) software that provides a digital workforce designed to automate complex, end-to-end operational activities.
_For more information about Blue Prism, please visit https://www.blueprism.com._

## What is Onify?

Onify brings together systems, objects and processes in a simple and searchable interface with 100% control and automation for the underlying systems of record. In practice, this means opening up role-based Self-Service for the users to systems that were previously unavailable to them, thereby increasing agility and cooperation in the organization between silos and with customers.
Onify has been developed with user simplicity first meaning that the user roll-out is almost non-existent and Time to Value is achieved faster.
_For more information about Onify, please visit https://onify.co._

## Use cases & scope

The scope of this Blue Prism Asset is to show Blue Pris can integrate with Onify and how Onify can integrate with Blue Prism.

### Outbound integrations (Blue Prism > Onify)

Here are some example integrations to use Blue Prism with Onify:

* Search and get information about items/objects in Onify
* Create or update items/objects in Onify
* Start and update processes state/status in Onify
* Update agent task log or result in Onify
* Run a connector pipeline to index items/objects in Onify
* Run agent task (script) in Onify
* Create or update users in Onify

### Inbound integrations (Onify > Blue Prism)

* Start a process in Blue Prism via form submit in Onify

### What is included?

Onify Hub API has about 250+ REST API endpoints. We have carefully selected endpoints that we think would add best value to Blue Prism.
Here is a list of the API endpoints that are included in this asset.

> NOTE: If you are missing any API enpoint, you can manually create a Web API definition for it.

#### My endpoints

The My (`api/v2/my/*`) endpoints are used for logged in users in Onify.
Here are the included (my) endpoints:

* `POST /my/login`
* `GET /my/audit`
* `POST /my/audit`
* `GET /my/bulletins`
* `GET /my/processes`
* `GET /my/processes/[id]`
* `GET /my/processes/[id]/status`
* `GET /my/processes/[id]/state`
* `PUT /my/processes/[id]/status/[status]`
* `PUT /my/processes/[id]/state/[state]`
* `POST /my/processes/start/[workflow]`
* `GET /my/items/[workspace]`
* `GET /my/items/[workspace]/[key]`
* `GET /my/items/[workspace]/[key]/events`
* `POST /my/items/[workspace]/[key]/events`
* `GET /my/items/[workspace]/export`
* `GET /my/options/[key]`
* `GET /my/options/tags/[tags]`
* `GET /my/agent/task/[id]/meta`
* `PUT /my/agent/task/[id]/log`
* `GET /my/agent/task/[id]/result`
* `GET /my/agent/task/[id]/events`
* `POST /my/agent/task/[id]/events`
* `GET /my/agent/task/[id]/meta/[key]`
* `POST /my/connector/pipelines/[key]/run`

#### Admin endpoints

The My (`api/v2/admin/*`) endpoints are used for administration and configuration of Onify. User needs to be in the `admin` role to use these endpoints.
Here are the included (admin) endpoints:

* `GET /admin/events`
* `POST /admin/events`
* `GET /admin/events/[id]`
* `GET /admin/items`
* `POST /admin/items`
* `DELETE /admin/items`
* `GET /admin/items/[key]`
* `PUT /admin/items/[key]`
* `PATCH /admin/items/[key]`
* `DELETE /admin/items/[key]`
* `POST /admin/items/import`
* `PUT /admin/items/import`
* `PATCH /admin/items/import`
* `GET /admin/items/export`
* `GET /admin/options`
* `POST /admin/options`
* `GET /admin/options/[key]`
* `PUT /admin/options/[key]`
* `PATCH /admin/options/[key]`
* `DELETE /admin/options/[key]`
* `POST /admin/options/bulk`
* `PUT /admin/options/bulk`
* `DELETE /admin/options/bulk/[tags]`
* `GET /admin/users`
* `POST /admin/users`
* `GET /admin/users/[key]`
* `PUT /admin/users/[key]`
* `PATCH /admin/users/[key]`
* `DELETE /admin/users/[key]`
* `GET /admin/processes`
* `GET /admin/processes/[id]`
* `PUT /admin/processes/[id]`
* `DELETE /admin/processes/[id]`
* `POST /admin/processes/start/[workflow]`
* `GET /admin/processes/export`
* `GET /admin/agents/task/[id]`
* `DELETE /admin/agents/task/[id]`
* `POST /admin/agents/task/[command]`

### Documentation

* Onify REST API reference: https://support.onify.co/reference
* Onify support and documentation: https://support.onify.co

### Pre-Requisites

* Blue Prism version 6.x
* Onify Hub 2.x

## Installation

1. Download .bprelease file(s)
2. In Blue Prism, select `File > Import` 
3. Follow the prompts to select and import .bprelease file
4. Update [Base URL] for the Web API service(s) (in the "System" tab in Blue Prism), eg. `https://onify-api.acme.com`. 

## Getting started

Let´s get started using Onify together with Blue Prism!

## Authentication

Before you use the API endpoints, you need to be authenticated and have `authentication` token. 
To generate a token, use the `POST /my/login` endpoint. Here is a curl example:

```bash
curl -X POST "https://onify-api.acme.com/api/v2/my/login" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"username\": \"usr01\", \"password\": \"passw0rd\"}"
```

### Build a process

Start building your process and start using the Onify Hub API actions!

## Support

* Community/forum: https://support.onify.co/discuss
* Documentation: https://support.onify.co/docs
* Support and SLA: https://support.onify.co/docs/get-support

## Contribute

To contribute to the development of this asset, follow these steps:

1. Fork this repository
2. Import the .bprelease file into Blue Prism
3. Add functionality to the asset
4. Create an updated .bprelease file
5. Update this file (README.md) and include the new functionality
6. Submit a pull request to this repository that includes all changed files
7. The pull request will be reviewed and, if approved, merged into the appropriate branch.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.