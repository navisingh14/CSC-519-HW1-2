# CSC-519-HW1-2
Devops HW1part2 - VM provisioning through APIs

### Name:                                                          
Navjot Singh 

### Student Id:
200154743
### Unity Id: 
nsingh9@ncsu.edu


#### Link to the AWS nodejs code
[Click here to go to the provisioning code for AWS](https://github.ncsu.edu/nsingh9/CSC-519-HW1-2/blob/master/AWS/main.js)

#### Link to the Digital Ocean nodejs code
[Click here to go to the provisioning code for AWS](https://github.ncsu.edu/nsingh9/CSC-519-HW1-2/blob/master/DigitalOceanDroplet/main.js)


#### Screencast link:
[Click here to watch the video](https://youtu.be/5-9ZPIWgWlQ)  

### Concepts


1. Define idempotency. Give two examples of an idempotent operation and non-idempotent operation.  
Ans. One of the definitions of the term idempotency is that if an operation is executed once or multiple times, it always produces the same output. For example, GET and DELETE from HTTP protocol are idempotent since getting a value once or multiple times doesn't change the value itself and similarly the case with DELETE as deleting once or multiple times doesn't affect the deleted value. Commands like 'mv a b' and 'ssh-keyscan -H >> .ssh/known_hosts' is not idempotent since after renaming once we won't be able to find the same file again, and similary executing the second command will add multiple lines to the known_hosts file


2. Describe several issues related to management of your inventory.
3. Describe two configuration models. What are disadvantages and advantages of each model?  
Ans. **PULL model**: In this model the clients poll periodically to get the updates from a configuration server.  
**Advantages**: This is better at keeping the assets in sync with periodical polling. Also, this is more scalable since a central server doesn't need to know the map of the entire architecture since each client registers itself independently of the other.  
**Disadvantages**: Different pull based system use different proprietary language which makes it a problem to replicate the changes in the codes used on the client side.  
**PUSH model**: In this model, a configuration server pushes to all the clients whenever there are new changes.  
**Advantages**: This is easier to manage since there's only one central server that does all the work.  
**Disadvantages**: There is no track of the current state of the clients and they can drift from the state without any checks.


4. What are some of the consquences of not having proper configuration management?  
Ans. It decreases efficiencies, stability and control as there is no visibility and tracking of the changes.  
Higher costs as there is no detailed knowledge of all the elements of the configuration which leads to unnecessary duplication.  
Decreased system reliability through slower detection and correction of improper configurations that could negatively impact performance.
Slower problem resolution, thus worsening quality of service and hence .  
Less efficient change management by not knowing what the prior structure is in order to design changes that do not produce new incompatibilities and/or problems.  
