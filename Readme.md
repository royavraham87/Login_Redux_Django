# login
## login, register, token
    "pip install djangorestframework-simplejwt" - a command for installing the security and token

    in the setting.py  (backend).. 
    from datetime import timedelta

    copies from the document

now copy the urls file from "myproj" to the "base"
now I copy this line: "path('blog/', include('blog.urls'))"
and change it to this line: "path('', include('base.urls'))" and add import include. this will allow the project to know the URLs from the base.

now I go to the URLs in the base, delete the existing paths and add the Login path (page 19 in Eyal's page):
"path('login/', views.MyTokenObtainPairView.as_view())," this connects my login to the project.
now I add this import from the page: "from rest_framework_simplejwt.views import TokenObtainPairView" to the URLs.py in the application (base)
and i change the path a little to "path('login/', TokenObtainPairView.as_view()),"- not sure why???

now need to install rest framework with this command: 
"pip install djangorestframework"
copy a line to the settings

now we added a simple code ("index") for rest API (in the views.py- in the app).
and now if i added this sample i need to add the path for "index" in the URLs.py in the base
"path('', views.index),"+ an import "from . import views" there was an autofix but it didnt work (. means on this current library). now this is my homepage!

now i have the login and i can access it with "POST" but i don't have a user right now so i need to create the supperuser. after we create a supperuser i can do "login" with this supperuser and get the token!!!
now we succesfully configured the server!

*** we finished the backend. now we move to the frontend

we went to the App.js in the front
we deleted Everything and wrote "rafce"- we got a minimal file in my style of writing.
now i only need to create the "login" i create "user name" and "password" with *input* and a button for the login. 
now we moved what we wrote here to a new component called "Login.js" we wrote rafce and pasted the code inside the login component. now we returned to the "App.js" and connected the "Login.js" component with  <Login/>

