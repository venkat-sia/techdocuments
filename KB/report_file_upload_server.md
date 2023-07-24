### current state
 - file upload server 
   - fileupload & processing are done in the same server
   - user uploads the file 
   - file is stored in the NFS 
   - server returns the response to the user 
   - server immediately starts the file processing asynchronously
 
- issue  
  - too many open connections and the servers shuts down

- temporary solution
  - increase the number of file upload server instances to 5

### new state 
- split the servers 
  - file upload
  - file processing 

- fileupload
  - user uploads the file 
  - file is stored in the NFS 
  - server sends the file processing message to MQ
  - server returns the response to the user 
  - please keep the number of instances to 3 

- file processing
  - listen to the file processing queue
  - limit the number of consumers in each instance 
  - scale the number of instances when there are many in the queue 
  - start with number of instances 2 
 
