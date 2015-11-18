# django_social_followers


# Getting started

[Create a FACEBOOK App]  (https://developers.facebook.com/apps/) and get your App ID and App Secret

[Create an INSTAGRAM App] (https://instagram.com/developer/clients/manage/ ) and get your Client ID and Client Secret

[Create a TWITTER app] (https://apps.twitter.com/) and get your Consumer Key, Consumer Secret, Access Token and Access Token Secret

**Add your social settings to settings.py**

```javascript
  
  FACEBOOK_SETTINGS = {
    'CLIENT_ID': 'XXXXX',
    'CLIENT_SECRET': 'XXXX',
    'GRANT_TYPE': 'client_credentials'
  }
  
  INSTAGRAM_SETTINGS = {
    'CLIENT_ID': 'XXXXXX',
    'CLIENT_SECRET': 'XXXXX'
  }

  TWITTER_SETTINGS = {
    'CONSUMER_KEY': 'XXXX',
    'CONSUMER_SECRET_KEY': 'XXXX',
    'ACCESS_TOKEN_KEY': 'XXXX',
    'ACCESS_TOKEN_SECRET_KEY':'XXXXXXX'
  }
  
```

**Add code to fetch followers**

```
from django_social_followers.social import SocialFollowers
social_followers = SocialFollowers()

facebook_followers = social_followers.get_facebook_followers('WillAndSkill')
instagram_followers = social_followers.get_instagram_followers('389223200')
twitter_followers = social_followers.get_twitter_followers('_willandskill')

print facebook_followers, instagram_followers, twitter_followers

```

**INSTAGRAM USER ID**

[Get your Instagram user id] (http://jelled.com/instagram/lookup-user-id)
