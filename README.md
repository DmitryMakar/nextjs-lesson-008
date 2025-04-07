# nextjs-lesson-008
Learn NextJS. Lesson 8. Static and Dynamic Rendering

Lecture: https://rutube.ru/video/0e8ef44abcd9d254abc31a196da28525/

Presentation: https://dmpsy.club/references/NextJS/lesson_008_static_and_dynamic_rendering_rus.pdf

Pre-requisite: PostgreSQL installed on your host

To verify: pg_config --version

Example output: PostgreSQL 16.8 (Ubuntu 16.8-0ubuntu0.24.04.1)

Postgres User: nexxtapp-db

Postgres Password: <nexxtapp-db_password>

Postgres DB: nexxtapp-db

1. cd nextjs-lesson-008 #change to the project directory
2. pnpm install  #create node modules
3. If seeing Warning on Ignored build scripts:
   pnpm approve-builds # and select all packages to approve and install   
 
4. Add the Postgres DB credentials to the .env file:
   
   nano .env   # add your credentials like (specify your password):

   POSTGRES_HOST=localhost

   POSTGRES_USER=nexxtapp-db

   POSTGRES_PASSWORD=<nexxtapp-db_password>

   POSTGRES_DATABASE=nexxtapp-db

   Ctrl-X # to save changes and close nano
5. pnpm seed # seed the DB and see:
6. Delay the fetchRevenue request by 10 seconds:

     cd app/lib

     cp data.ts.slowedFetchRevenue data.ts   
8. pnpm run dev #Start on the dev server  
7. Verify it works:

    open http://localhost:3000

    open http://localhost:3000/dashboard
   
9. Ctrl-C # to stop the dev server

Optional:
 
10. pnpm run build # Create a production build   
11. pnpm start # start the production 
12. Verify it works (very fast when switching between static pages):

    open http://localhost:3000

    open http://localhost:3000/dashboard
13. Ctrl-C # to stop the prod server


