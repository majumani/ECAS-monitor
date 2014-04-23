ECAS-monitor
============

Checking the Electronic Client Application Status (ECAS) from CIC website can be painful because it does not come with a notification function. The update time is also random which does not reflect the actual status. Your status could update in midnight. Therefore, people check their ECAS a hundred times per day when they anxiously wait for their status update, wasting their time while bothering CIC servers.

To relive the applicants from desperate waiting and checking, and to reduce the load of CIC servers (because ), I develop a small tool called ECAS-monitor. It automatically checks ECAS for applicants every few hours, and sends the user an email alerts when a status update is detected. Your can start to use this tool after you are able to check you status over ECAS, i.e., after you can see the line:

* We received your application for permanent residence on YYYY-MM-DD.

When a new status has been added, the software will detect it. Known status that can be detected includes but is not limited to:

* We started processing your application on YYYY-MM-DD.
* Medical results have been received.
* A decision has been made on your application. The office will contact you concerning this decision.

To start using the tools, you first need to change the configuration file `config.txt` and input your own information. Then you need to have `Node.js` runtime environment installed on your computer (node and npm). To run this tool, Windows users can directly double-click "start.bat". Alternatively, if you want to run manually or you are using another OS, go to the directory of this tool and run:

```bash
$ npm start
```

You are done. Keep the program running so that it works for you all the time. 

Note: All your personal information is transmitted over the Internet securely using HTTPS. But it is saved in `config.txt` locally on your computer in plain text. So it is your responsibility to protect the file.
