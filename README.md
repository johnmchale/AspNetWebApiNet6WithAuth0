# `ASP.NET Web API .NET 6 using auth0`


## Repo

- This is the default `ASP.NET Web API .NET6` project using the WeatherForecast controller to return random weather forecasts
- However, the WeatherForecast controller is protected using auth0
- To try out the repo, you will need to sign up to auth0 and create a API application, then enter your tenant ID in the appsettings.json file

![image](https://user-images.githubusercontent.com/38525955/214659140-dabff5fe-c509-4ffa-af63-175cd7786794.png)

- Enter a name for your application and an identifier (in this case, I used the URL of the running application) and hit Create

<img width="474" alt="image" src="https://user-images.githubusercontent.com/38525955/214660273-fa2df5f0-be79-4c30-b091-9c168c00f70e.png">

- Now, you need to enter your tenant ID in the Domain part of the appsettings.json. The tenant ID can be obtained from the home screeen
- n.b. you need to append .us.auth0.com to the tenant ID (e.g. dev-x999aaaa.us.auth0.com ). The audience will be the identifier you used above

<img width="313" alt="image" src="https://user-images.githubusercontent.com/38525955/214665901-dbbeda11-f40d-4778-8377-9cb5facfd2a2.png">


```sh
"Auth0": {
    "Domain": "dev-x999aaaa.us.auth0.com",
    "Audience": "https://localhost:7028/"
  }
```

