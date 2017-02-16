# JWT-OAuth2.0-Auth-Server

This test project contains following setup:
1. Authorization Server: An OAuth2 server which generates the token and get converted to JWT token.

# How to start

1.Make sure you have maven installed
2. Make sure you have java 1.8 installed
3. Checkout the source code
4. Run "mvn clean install"

# Start the auth server

1. Inside "JWT-OAuth2.0-Auth-Server" execute "mvn spring-boot:run"

# Playing with the set up 
All access tokens can be decoded via http://jwt.io Just copy and insert the "access_token" content

#Getting access token via POSTMAN

1. Open the post man and set the method as POST 
2. Paste the following the URL in the request url  (make sure the Authorization server is up and running)
http://concur:concur@localhost:9000/dkom/oauth/token?redirect_uri=http://localhost:9001/dkom/&response_type=code&client_id=nirmal&client_secret=nirmal&username=admin&password=admin&grant_type=password
3. Set the Header Key as Content-Type and value as application/x-www-form-urlencoded
4. Hit the Send Request.

#Sample Response from Autherization Server

{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE0ODcyNjgyMTgsInVzZXJfbmFtZSI6ImFkbWluIiwiYXV0aG9yaXRpZXMiOlsiUk9MRV9BRE1JTiIsIlJPTEVfVVNFUiJdLCJqdGkiOiI2NDFiYTg2MC0yOTMyLTQxNWItYTIwMC0wMTFjYWJjZGE5NWQiLCJjbGllbnRfaWQiOiJuaXJtYWwiLCJzY29wZSI6WyJyZWFkIl19.bQK7eQvMVgRwcZaOyVaOUzoelDePyGrbWa6vUNLNOD4",
  
  "token_type": "bearer",
  
  "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyX25hbWUiOiJhZG1pbiIsInNjb3BlIjpbInJlYWQiXSwiYXRpIjoiNjQxYmE4NjAtMjkzMi00MTViLWEyMDAtMDExY2FiY2RhOTVkIiwiZXhwIjoxNDg5ODE3MDE4LCJhdXRob3JpdGllcyI6WyJST0xFX0FETUlOIiwiUk9MRV9VU0VSIl0sImp0aSI6IjBkNzRjZDVlLWRmMGEtNDM0MC04OTQxLWVhNTE5NWYyYWMyNiIsImNsaWVudF9pZCI6Im5pcm1hbCJ9.pWDFs17E-LQw4M7TpWcJbCal2hZbtwJZltAzKdqZwIo",
  
  "expires_in": 43199,
  
  "scope": "read",
  
  "jti": "641ba860-2932-415b-a200-011cabcda95d"
}




