## Boilerplate
This is starter boilerplate use nestjs.


## Dependency
- Prisma ORM
- Swagger
- JWT
- CASL
- Minio


## SETUP PREPARATION
### .env 
```
DATABASE_URL="postgresql://postgres:mypassword@localhost:5432/prismadb-auth?schema=public&connection_limit=5"  
JWT_ACCESS_SECRET = 'HgYdLksz3WMSgWh0CF31z9daZuxK10SK7n94ER9ZtPGRTfCYQO/c/B+jHFVkTp0jmw5ffYktfF97iSF1IidW5w=='  
JWT_ACCESS_EXPIRES_IN = '1h'  
JWT_REFRESH_SECRET = 'b0Sc5QyQVdC3CQkQsuwGjb8ak9xlKG2qIQJvRBV9RJrO43KsDQ7sruXPW3XWpuMtM+vzG18DXtsPt6LLfJcPIw=='  
JWT_REFRESH_EXPIRES_IN = '1h'

MINIO_ENDPOINT='localhost'  
MINIO_PORT=9000  
MINIO_ACCESS_KEY=VzoWvEak63bu5IxbGchv  
MINIO_SECRET_KEY=V5osh50X1vaDNTi5w6YStZ7rxNwE3WFIAoYh7auo  
MINIO_BUCKET_NAME='sample'
```

### MINIO CONFIGURATION
DOWNLOAD : https://min.io/download  
## mac/linux instalation & how to run 
minio server data-minio  
## windows instalation & how to run  
```
PS> Invoke-WebRequest -Uri "https://dl.min.io/server/minio/release/windows-amd64/minio.exe" -OutFile "D:\minio.exe"  
PS> setx MINIO_ROOT_USER minioadmin  
PS> setx MINIO_ROOT_PASSWORD minioadmin  
PS> D:\minio.exe server D:\minio-data --console-address ":9001"  
```




## migrate
npx prisma migrate dev --name init && npx prisma generate && npm run start:dev

## if any changes in prisma schema
1. npx prisma db push
2. npx prisma generate
3. npx prisma db seed  
or
4. npx prisma migrate dev --name revision-02



# INSTALLATION
1. git clone
2. cd boiler-plate-nestjs
3. npm install
4. don't forget config .env
5. FOR WINDOW running command : npm install -g win-node-env
6. running minio server
7. create bucket "sample"
8. npx prisma migrate dev --name init && npx prisma generate && npm run start:dev


# API DOC
open http://localhost:3001/api

# LICENSE
The source code for the site is licensed under the MIT license, which you can find in the MIT-LICENSE.txt file.

All graphical assets are licensed under the [Creative Commons Attributio](https://creativecommons.org/licenses/by/4.0/) Unported License.

# DISCLAMER
This software not support production ready yet, use with your own risk !.  

# OTHERS
## DOCUMENTATION
## How run  
### dev
npm run start:dev  

### build
npm run build  
### start prod
npm run start:prod  
or  
npm run build && npm run start  

## Authenticate 
POST auth/login
Body { "username":"", "password":""}

## Authorize 



## Validating
GET auth/me  
Header  
Cookie refresh='.....'  
Response Status 
- 200 OK


## Refresh Access Token  
GET auth/refresh-token  
Header  
Cookie refresh='.....'
Response Status  
- 200 OK  
- 404  





## Create Resource
nest g resource stories --no-spec  






