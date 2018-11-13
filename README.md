# Getting started with OpenDoc

## Step 1:
Create a new repo, the name of the repo should follow the convention:
```
opendoc-<name_of_document>
```

## Step 2:
Clone the template repo onto your local machine

```
git clone git@github.com:opengovsg/opendoc-template.git
```

## Step 3: 
Update the remote address for the repo on your local machine

```
git remote set-url origin git@github.com:opengovsg/opendoc-<"name_of_document">.git
```

## Step 4: 
Add your converted markdown files into the root directory of the repo

## Step 5: 
Update the following fields in the _condig.yml file:

| First level     | Second level        | status   | example                                   |
|-----------------|---------------------|----------|-------------------------------------------|
| title           | -                   | required | Supreme Court Practice Directions         |
| elastic_search  | index               | required | opendoc_supreme_court_practice_directions |
| styling_options | primary_brand_color | optional | #113355                                   |
| styling_options | logo_path           | optional | /assets/image/logo.png                    |

## Step 6: 
Commit your changes 

```
git add .
git commit -m <"commit_message">
```

## Step 7:
Push your changes to the remote branch

```
git push origin master
```

## Step 8:
Setup webhook for elasticsearch indexing

1. Go to the settings page of the repository (i.e https://github.com/opendocsg/opendoc-supreme-court-practice-directions/settings)
2. On the left panel, click on the "Webhooks" tab
3. Click on the "Add webhook" button on the top-right corner
4. Fill up the following details in the form provided:

| Field        | Value                                   |
|--------------|-----------------------------------------|
| Payload URL  | https://search.opendoc.sg/push          |
| Content type | application/json                        |
| Secret       | <Approach a member of the opendoc team> |
	
## Step 9:
Setup netlify for production and staging branches
	
