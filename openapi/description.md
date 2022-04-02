This is the docs for the **xrv2 API(s)** that were developed by Manash X0PA. 
It starts from April 1st 2022. For previous docs check out the other docs.
If you have any questions or doubts regarding these, contact Manash Sarma
(Manash@x0pa.com).
  
## Import NOTES:

Step 1: Write your path name on ***root.yaml*** file. After creating the path details, we'll be referecing that details file here.

Step2: Write the path details on ***paths/{group}/file.yaml***. 
Then reference this file on the ***root.yaml*** file for that path.

Step 3: Run this following command to preview your docs. It is like a Live Server. You can run it first and edit docs while previewing it.
```bash
openapi preview-docs
```

#### NOTE: 
In order for this command to work, make sure you installed ***"@redocly/openapi-cli"*** package globally with this command
```bash
npm i -g @redocly/openapi-cli
```

Step 4: When your docs are done. Run this following command to compile all files into one single file.
```bash
openapi bundle -o apidocs
```
It will create a ***apidocs.yaml*** file. Now we need to create an HTML file out of it. For that follow the next step.

Step 5: To generate the HTML file, run this following command which will create a ***docs.html*** file.
```bash
npx redoc-cli bundle apidocs.yaml -o docs.html
```

BONUS: Run this **"movedocs.sh** script to automatically copy the **apidocs.yaml** and **docs.html** files to your intended repo.
Now commit your changes and push to your respective repo. Feel free to use this ***docs*** to any of your repo!

With love Manash Sarma!