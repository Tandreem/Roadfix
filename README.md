RoadFix — AI-powered roadside assistance

Broke down on the road? RoadFix diagnoses the problem with AI, alerts every verified mechanic nearby at once, and the fastest one to accept comes to you, with live GPS tracking and transparent pricing.

Live demo: https://tandreem.github.io/Roadfix/

App	Link
Customer app	https://tandreem.github.io/Roadfix/roadfix-customer-FINAL.html
Mechanic app	https://tandreem.github.io/Roadfix/roadfix-mechanic-FINAL.html
Admin panel	https://tandreem.github.io/Roadfix/roadfix-admin-FINAL.html
The problem

When a vehicle breaks down, the driver has to guess what's wrong, find a mechanic they can trust, and accept whatever price they're quoted on the spot. This is worst at night, on highways and in unfamiliar areas, which is exactly when people are most vulnerable.

How RoadFix solves it

RoadFix is three apps connected through one realtime backend:

Customer app
AI diagnosis: describe the problem (or add a photo) and Gemini AI suggests the likely faults, the parts needed and a price range before anyone arrives.
Quick Connect: skip the AI questions and reach a nearby mechanic straight away.
First to accept wins: the request goes to every verified mechanic nearby at the same time, and whoever accepts first gets the job.
Transparent pricing: late-night, low-availability and tool-fetch surcharges are always shown with their reason.
Live tracking: follow the mechanic on GPS, chat or call them, and pay by UPI or cash.
Emergency SOS with live location, towing, pre-booking, and an AI Health Monitor (beta) that uses the phone's mic and motion sensor to spot faults early.

Mechanic app
Go online and receive gig alerts showing the issue, the price, your take-home earnings, the parts to carry and the customer's GPS pin.
Accepting a gig is atomic (it uses a Firebase transaction), so two mechanics can never both win the same job.
Update the job status, re-estimate if the diagnosis on-site is different, and add a tool-fetch surcharge when a garage trip is needed.

Admin panel
Live dashboard of active jobs, mechanics online, customers and SOS alerts.
Verify mechanics before they can take jobs.
Finance view: platform fees, mechanic payouts and cash-commission settlement.
Tech stack
Frontend: HTML, CSS and JavaScript (each app is a single file)
Backend: Firebase Realtime Database, Firebase Authentication and Firebase Storage
AI: Google Gemini API
Location: browser Geolocation API and Google Maps links
Hosting: GitHub Pages
Try it
Open the Mechanic app, register, and have an admin verify you in the Admin panel.
Open the Customer app in another browser or on another device, add a vehicle, then use Report issue or Quick connect.
Tap Notify nearby mechanics. The mechanic gets the gig alert and can accept it.

Allow location access in both apps so distance matching and GPS tracking work.

Roadmap
Move AI calls and price calculations to the server (Cloud Functions) and lock down the database with Firebase security rules
Integrated UPI payments
Mobile apps for Android and iOS
Pilot launch in Guwahati with local verified mechanics
Author

Built by Tandreem Trishan Kalita, Army Public School, Basistha, Guwahati.
