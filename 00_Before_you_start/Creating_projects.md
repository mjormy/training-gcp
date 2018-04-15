Once you've created an account you can create a project in GCP.

A project will include every GCP component you will use. You can create different projects that can interact with each other.
This is recommended, since different kinds of projects will have different processing and storage needs. Your task will be to identify this specific needs to tune up each project.

You don't need to install the SDK to create projects, but you'll need it for atuomation and autonomy.

## Create a new project

You need 2 fields in order to create a project: `projectId` and `name`

1. From the Console

Go to the project list, you'll have a list of your current projects and an option to create a new one.

2. Via POST
```
curl 'https://cloudresourcemanager.googleapis.com/v1/projects?key=[YOUR_API_KEY]' \
  -X POST \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  --data-binary '{"name":"my-first-project"}' \
  --compressed
```
 3. From your code

Reference: 
- Method: projects.create
https://cloud.google.com/resource-manager/reference/rest/v1/projects/create