## Linkedin-Connector
This module facilitates the implementation of Single Sign-On (SSO) using LinkedIn as the Identity Provider (IDP). Along with LinkedIn SSO, this module offers functionalities that can be utilized to perform operations related to LinkedIn posts and sharing.
## Dependency
   •	Encryption
   •	OIDC Module
   •	Community Commons
   •	Nanoflow Commons
## Configuration
  ### a.LinkedIn Developer portal 
        •	Log in to the LinkedIn developers’ site at https://www.linkedin.com/developer/apps.
        •	Click Create App and complete the entire information.
        •	Specify your company name or create a new company page. Click Create App.
        •	The App Settings is displayed. Complete the company verification process.
        •	Add the below list of the Products in product tab.
                •	Share on LinkedIn.
                •	Sign in with LinkedIn.
                •	Sign in with LinkedIn v2.
        •	Select the Auth tab. In Oauth 2.0 settings add Mendix application Redirect URL.
        •	Generate access token with(email, openid, profile, r_emailaddress, r_liteprofile, w_member_social)all permissions. And store that token in Mendix as  Constant.
        •   To create a token manually, you can visit the following URL: https://www.linkedin.com/developers/tools/oauth
        •	Check auth tab, the OAuth 2.0 scopes all are added.
  ### b.	OIDC 

        •	Add an Encryption key with 32 charaters. 
        •	Create new page and call OIDC.Snip_Configuration snippet. Set page visibility to admin.
        •	Add that page in navigation. Login as admin and create new OIDC configuration.
        •	Enter your Client ID, Client Secret key and add below Endpoits/URLs in respective fields as shown below.
  
             # authorization_endpoint:  "https://www.linkedin.com/oauth/v2/authorization"
             # token_endpoint:          "https://www.linkedin.com/oauth/v2/accessToken"
             # userinfo_endpoint:       "https://api.linkedin.com/v2/userinfo"
             # jwks_uri:                "https://www.linkedin.com/oauth/openid/jwks" 
             # issuer:                  ”https://www.linkedin.com”
             # Scopes:                  email, openid, profile, r_emailaddress, r_liteprofile, w_member_social
   ### c.	LinkedIn connector 
        •	Enable anonymous user and set as guest user role.
        •	Add Linkedin_Connector/SSO_Login_Page in navigationrole-based home page for guest user role.
        •	Add Post_snippet in your required page, set visibility for user. And add that page in role-based home page for User.
        •	Run the application. Use sign in with LinkedIn option. And start posts and share functionality.
  `
                


        
