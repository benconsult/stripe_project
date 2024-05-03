### STRIPE APP DEMO APP

git branch
//to main
rm -rf .git
git init
git config --global init.defaultBranch main
git add .
git commit -m ""
git remote add main https://github.com/benconsult/stripe_project.git
git push -u origin main

######


# overview
FE - server method - payment gateway

-create free accout, dashboard - developer - API keys
-Docs: Dashboard - payment - accept online payment - custom payment
flow - 
Platform: Web, FE: HTML, Backend: Node

IDEA: FE publishable key communicate with the BE (secret), then the secret key is send as the response.

-copy the publishable key to the index.html in public folder


# flow overview


-copy the publishable key from the API key to project in
public/browser-app.js/ stripe method ''

-controller: name should match what we have in the fetch('/stripe) browser-app.js
-browser-app.js: controls what is passed from the FE

NB: use App.js for post route instead of the route folder
-stripe is in cents, 1999, 19.99
IDEA: 
Just like a we form, HTNL controls presents the form
-JS controls form manipulation
-Controller handles the server method

-what is sent to the controller is payWith(stripe, card, clientsecret)
Refresh the page to get the req.body payload

# controller
//Get waht is returned from the FE - expected payload from stripe
-calculateOrderAmount
-create takes on two properties (amount and currency)
return clientSecret from as response from the server
