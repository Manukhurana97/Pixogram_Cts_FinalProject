# Pixogram_Cts_FinalProject

Angular: FrontEnd (Conpoenent, service, Routing )
Backend: Spring Boot (Eureka server, Zull, Boot Apis)


Backend
This Zip contains total 5 apis
1. Eureka server
2. Zull Server 
3. Following service (Simple user follower and following) 
4. Media file server (upload file {image/video} in Angular using firebase storage and url of uploaded is passed to backend)
  - add Media data: @PostMapping("/media/create/{userId}/{userName}")
        - required: int uid, String title, String description, String tags, String url
  - get all media of particular user: @GetMapping("/media/uid/{userId}"
  - get media data of particular ID:  @GetMapping("/media/id/{userId}")
  - Like/UnLike media: @PutMapping("/media/like/{id}/{flag}")
    
5. UserServer (Simple User details username password and email) 
  * Create User : @PostMapping("/user/create")
  * Find User by name: @GetMapping("/user/{name}") 
  * Find user by name for login: @GetMapping("/user/login/{name}") 
  * get user by id: @GetMapping("/user/id/{id}")
  * update user details: @PutMapping("/user/update/{id}") 
   
    
--  H2 database is used in media-service, user-service
--  Spring boot apis, Jpa for Dao layer
--  No spring Security
--  Spring email and password validation
--  Angular firebase database is used to store file 
 
