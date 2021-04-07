# Pixogram_Cts_FinalProject

Angular: FrontEnd (Conpoenent, service, Routing )
Backend: Spring Boot (Eureka server, Zull, Spring Boot Apis)


<h2>Backend:</h2>

This Zip contains total 5 apis
1. Eureka server
2. Zull Server 
3. Following service  (Simple user follower and following) 
4. Media file server (upload file {image/video} in Angular using firebase storage and url of uploaded is passed to backend)
  - add Media data: @PostMapping("/media/create/{userId}/{userName}")
     - required: int uid, String title, String description, String tags, String url
  - get all media of particular user: @GetMapping("/media/uid/{userId}"
  - get media data of particular ID:  @GetMapping("/media/id/{userId}")
  - Like/UnLike media: @PutMapping("/media/like/{id}/{flag}")
    
5. UserServer (Simple User details username password and email) 
  - Create User : @PostMapping("/user/create")
  - Find User by name: @GetMapping("/user/{name}") 
  - Find user by name for login: @GetMapping("/user/login/{name}") 
  - get user by id: @GetMapping("/user/id/{id}")
  - update user details: @PutMapping("/user/update/{id}") 
   
    
  - - H2 database is used in media-service, user-service
  -  - Spring boot apis, Jpa used for Dao layer
  -    - No spring Security
  -   - For login get the user details using email and the compare the password.
  -     - Angular firebase database is used to store file 

 
<h2>Angular:</h2>

- Compoenets:
  - account-details: to check the user details
  - Followers: get all Followers
  - Following: get all following
  - header: Navigation
  - media: get all media
  - mediadetails: get particular details
  - news feeds: get all the latest news like(latest followers, Recdnt like etc)
  - Search: Search by username
  - upload media: upload the image/video


** const routes: Routes = [
*  {path: "" , component: LoginComponent},
*  {path: "login" , component: LoginComponent},
*  {path: "register", component:RegisterComponent},
*  {path: "uploadmedia", component:UploadMediaComponent},
*  {path: "mediadetails", component: MediadetailComponent},
*  {path: "newsfeed", component:NewsFeedComponent},
*  {path: "accountdetails", component:AccountDetailsComponent},
*  {path: "blockuser", component:BlockUserComponent},
*  {path: "search", component: SearchComponent},
*  {path: "mymedia", component: MyMediaComponent},
*  {path: "header", component:HeaderComponent},
*  {path: "following", component: FollowComponent},
*  {path: "follower", component: FollowerComponent}
