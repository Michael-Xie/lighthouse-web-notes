# RESTful design


# CRUD w/ Express

## CRUD

aka BREAD (Browse, Read, Edit, Add, Delete)
### **C**reate
#### Create Form - `GET /resource/new`

Show a form to collect information to create the resource

#### Create Resource - `POST /resource`

Takes in data (usually form data or JSON) and creates the resource in the 


### **R**ead
#### Index - `Get /resource`

List all of the given resource

#### Show - `GET /resource/:id`

Displays one of the resource

### **U**pdate

#### Edit Form - `GET /resource/:id/edit`

Dispaly a form prefilled with the given resources data

#### Edit Resource - `PUL /resource/:id`
> N.B. Sometimes you'll also see `PATCH /resource/:id` instead here
Updates the given resource with the data provided (Form or JSON data)

### **D**elete

METHOD PATH are two things needed by server

idempotent - repeated subsequent actions, always produce the same results
- PUT is idempotent and POST is not, prior gives same result while POST will change through subsequent actions (like tweet same message twice, each will have a different id)

nextid = 4
id: nextid++

// nextid gives back current value before incrementing for next use

++nextid gives back incremented value
