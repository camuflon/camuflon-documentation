# camuflon-documentation
The documentation of the camuflon project

This project has been developed in just **one day** for the [NOI Hackathon SFScon Edition (2021)](https://hackathon.bz.it). 
With some fixes and feature implementation, could be an **already made beta of a real product**.

- Website: [https://camuflon.vercel.app](https://camuflon.vercel.app)
- Api endpoint: [https://camuflon-api.herokuapp.com](https://camuflon-api.herokuapp.com/)
- Api documentation: [https://camuflon.docs.apiary.io](https://camuflon.docs.apiary.io/)
- App: *not available on playstore yet*

## The name

*"He is a large, peaceful ape with delicate movements. He has thick silvery fur, long, thin and silky, covering his sad black eyes. He has the ability to make himself __invisible__"*.

This is why we chose this name, because as a camuflon, our product makes **employees invisible, while their anonymous tracks are still tangible and can be used to make statistics**.

## Project purpose

The purpose of the project was allowing companies to tracks where their employees pass most of their time, like in the office or the machines room. 
With this data many statistics can be calculated, for example to understand if rooms are not used and should be dedicated to other things.
The data are **aggregated** or, in any case, **anonymous**, with the usage of a **pseudo-identifier not correlated to any name**.

## Our solution

Our solution is a **software** and **companies could register to that service** as a monthly paid service. 
It is **already online**, even if the site **lacks several features**, such as the **signup** (working in the API, though) and the rooms' deletion.

We used a sort of **Agile** method to develop it (of course with very **tiny** sprints) and this result could be thought as the result of the first sprint. 
With other two days, the website could be finished and some bugs would be likely fixed, so it would be already made for a **beta**. 
The **API** are already totally working and have a documentation site made with **Apiary**.

Our solution is composed of four parts:
1. The **APIs**, developed with **NodeJS** and **Typescript** and hosted on **Heroku**
2. The **Database**, with **MongoDB** and hosted on **MongoAtlas**
3. The **Website**, developed with **React** and hosted with **Vercel**
4. The **Mobile App**, developed with **ReactNative** and, hence, available both for **IOS** and **Android**

## How it works

1. The company signs up on the [website](https://camuflon.vercel.app), by putting **company name** (will be the username), **email** (will receive a confirmation email) and **password** (recovery is still to be implemented). The signup is available on APIs but not in the website
2. The company logs in (for now, the credentials are: { companyName: "azienda", password: "HackathonBolzano2021!?" })
3. The company does the initial settings (partially available): it can add **beacons** and **rooms**. To each **room** it can **associate one or more beacons' ids**.
4. The company is assigned with a **token** that can see in the website (not visible yet, but present in APIs and DB). This token is given to employees, so that only employees can use the app to report statistics
5. The employees download the mobile app and insert **company name** and **token**. They 