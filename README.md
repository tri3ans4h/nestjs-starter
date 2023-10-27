## Boilerplate
### Metode digunakan
- Prisma
- Swagger
- Authentication
  - Use Jwt
- Authorization
  - Use Casl


## How run  
### dev
npm run start:dev  

### build
npm run build  
### start prod
npm run start:prod  
or  
npm run build && npm run start  



## Create Resource
nest g resource stories --no-spec  

## example Config
### .env 
DATABASE_URL="postgresql://postgres:mypassword@localhost:5432/prismadb-auth?schema=public&connection_limit=5"  
JWT_ACCESS_SECRET = 'HgYdLksz3WMSgWh0CF31z9daZuxK10SK7n94ER9ZtPGRTfCYQO/c/B+jHFVkTp0jmw5ffYktfF97iSF1IidW5w=='  
JWT_ACCESS_EXPIRES_IN = '1h'  
JWT_REFRESH_SECRET = 'b0Sc5QyQVdC3CQkQsuwGjb8ak9xlKG2qIQJvRBV9RJrO43KsDQ7sruXPW3XWpuMtM+vzG18DXtsPt6LLfJcPIw=='  
JWT_REFRESH_EXPIRES_IN = '1h'  
## migrate
npx prisma migrate dev --name init && npx prisma generate && npm run start:dev

## if any changes in prisma schema
1. npx prisma db push
2. npx prisma generate
3. npx prisma db seed  
or
4. npx prisma migrate dev --name revision-02



# MINIO CONFIGURATION
minio server data-minio
FOR WINDOW
PS> Invoke-WebRequest -Uri "https://dl.min.io/server/minio/release/windows-amd64/minio.exe" -OutFile "D:\minio.exe"
PS> setx MINIO_ROOT_USER minioadmin
PS> setx MINIO_ROOT_PASSWORD minioadmin
PS> D:\minio.exe server D:\minio-data --console-address ":9001"


# INSTALATION
1. git clone
2. cd boiler-plate-nestjs
3. npm install
4. don't forget config .env
5. FOR WINDOW running command : npm install -g win-node-env 
6. npx prisma migrate dev --name init && npx prisma generate && npm run start:dev





