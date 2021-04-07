# Pixogram_Cts_FinalProject

Angular: FrontEnd (Conpoenent, service, Routing )
Backend: Spring Boot (Eureka server, Zull, Boot Apis)


Backend
This Zip contains total 5 apis
1. Eureka server
2. Following service (Simple user follower and following) 
3. Media file server (upload file {image/video} in Angular using firebase storage and url of uploaded is passed to backend)
 * add Media data: @PostMapping("/media/create/{userId}/{userName}")
    required: int uid, String title, String description, String tags, String url
    ** uid: user id*
 * get all meid of particular user: @GetMapping("/media/uid/{userId}"
    
4. Zull Server 
5. UserServer (Simple User details username password and email) 

-  Spring boot apis, Jpa for Dao layer
-  No spring Security
-  Spring email and password validation
-  Angular firebase database is used to store file 
 
