# mir4-token-generator
Launcher + API to generate valid tokens to launch new instances of the game.

Official Launcher Call Flow:
![mir4-oficial-launcher-process (1)](https://github.com/hernannes/mir4-token-generator/assets/34843858/4b93f2bc-c57c-458d-b5fb-3fe7f6b0cabb)



There is an encryption performed between the launcher and some libraries. 
Once a one-time token is generated, the token is verified by the game client.



The Mir4 Token generator, outsources this process with a modified launcher, with the help of the API, a valid token is generated. 

On the serverside of the API, a library has been created that "breaks" the process of generating tokens, generating a usable token. 

the modified launcher gets this token as an API response and starts a new instance of Mir4, passing the token as a parameter (the game window verifies that it is authentic code and allows the game to be launched)

Follows the flow of creating a new instance using the API

![mir4-modified launcher+api (1)](https://github.com/hernannes/mir4-token-generator/assets/34843858/1f7fe503-0da8-462d-b6bf-3318eda55b68)



After the project is finished, you can use the API in conjunction with your launcher, just sending the data to the API as per the documentation, to get valid tokens.

Ps.: You should send the errors to the API error endpoint, so we can identify changes to the encryption mode in the game instance and release updates. Still, this is optional.
