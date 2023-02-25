---
layout: post
title: A Data Project
description: A new, practical, and useful portfolio project
image: /assets/images/jungle.bmp
date: 2023-02-24 18:52:00 -0500
---

### A NEW PROJECT, NEW DATA, AND THE PLANNING PHASE!

---

&emsp;I’m designing and creating a piece of software that leverages economic data from Oldschool Runescape in order to make a profit. The data is retrieved from the OSRS Grand Exchange API. I will be documenting the whole lifecycle of this project, and using it for a portfolio piece. I will be acting as both client, and development team for this project. Here is the scenario..

---

&emsp;The client wishes for a piece of software that allows them to make informed decisions pertaining to the buying and reselling of Oldschool Runescape items for a profit. They require visualized historical price/volume data for each item in order to make these decisions. As the amount of items within the game are too large to manually sort through, the client has also requested that there is a sorting feature that will display the most profitable trades first. The client wishes for this data to be visualized in a way that is easy to access and use.

&emsp;After an examination of the client’s requests, the development team has decided that this project can be implemented in an effective and elegant manner. Upon further research, it was discovered that Jagex supplies users with an API that delivers both live, and historical Oldschool Runescape Grand Exchange price/volume data. It was also discovered that a mapping containing information about every item in the game is also delivered by the API upon request.

&emsp;We have observed that we can leverage the aforementioned data to assist in achieving every project requirement the client is seeking. As for an accessible and simple interface to access the data, the development team has decided to serve it in a web page rendered with ReactJS. The application will need to be able to “see” a list of all of the items in the game, this will be solved by storing the item mappings within a JSON file stored in an AWS S3 bucket. All live/historical price data for an item can be acquired upon loading the corresponding webpage by utilizing the Axios library to make HTTP requests to the API. After data is acquired from the Oldschool Runescape API, it can then be visualized using a React.js graphing library called Recharts. The development team has chosen to use the Recharts library due to it being an open source solution, meaning that all of the code inside it is non-proprietary and is maintained by the community. Due to the use of dynamic, live data - there will be no need for a database within this project. The requirement for a database has been satisfied by the use of AWS S3 to store the list of item mappings. The development team has come up with this simple diagram to depict the client-server architecture of the project.

<img style="display: block; margin-left: auto; margin-right: auto; width: 50%;" src="/assets/images/server_architecture.png" alt="Client-server architecture">

---

&emsp;The next post in this series will cover the feasibility of the client's idea, and if having this data could be used to gain a profit or not.  This will be tested by buying/selling items using the data supplied by the Oldschool Runescape API manually, and taking metrics to determine the effectiveness of the process.

Sincerely, \\
The Development Team (elidevo).