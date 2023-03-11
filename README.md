<p align="center">
<img src="https://imgur.com/KYWdZgN.png alt="Open Budgeteer"/>
</p>
<br />

In this short tutorial, I will show you how to install Open Budgeteer on your Synoogy NAS using Docker. OpenBudgeteer is a budgeting app based on the Bucket Budgeting Principle. It can be used for any typ of financial planning. This tutorial assumes you have Docker installed on your Synology NAS already and it is running.
<br />
<br />

Step 1. Install or Run Docker from the Package Center 

<p>
<img src="https://imgur.com/pVTroSS.png alt="Open Budgeteer"/>
</p>
<br />
<br />

Sep 2. Go to File Station and open the docker folder. Inside the docker folder, create one new folder and name it openbudgeteer. Follow the instructions in the image below. Use lowercase letters only.

<p>
<img src="https://imgur.com/TkvdFWs.png alt="Open Budgeteer"/>
</p>
<br />
<br />

Step 3. Go to Control Panel / Task Scheduler / Create / Scheduled Task / User-defined script. 

<p>
<img src="https://imgur.com/C9fseOh.png alt="Open Budgeteer"/>
</p>
<br />
<br />


Step 4. Once you click on User-defined script, a new window will open. Follow the instructions below:
<br/>
<br />
<br />
    

4b. General: In the Task field type in Install OpenBudgeteer. Uncheck the “Enabled” option. Select root User.
<p>
<img src="https://imgur.com/PPVAsnD.png alt="Open Budgeteer"/>
</p>
<br />
<br />

4c. Schedule: Select Run on the following date then select “Do not repeat“.
<p>
<img src="https://imgur.com/TCoOvXs.png alt="Open Budgeteer"/>
</p>
<br />
<br />

4e. Task Settings: Check “Send run details by email“, add your email then copy paste the code below in the Run command area. After that, click OK.


docker run -d --name=openbudgeteer \
-p 6100:80 \
-e CONNECTION_PROVIDER=sqlite \
-v /volume1/docker/openbudgeteer:/app/database \
--restart=always \
axelander/openbudgeteer

<p>
<img src="https://imgur.com/Bd3aYvr.png alt="Open Budgeteer"/>
</p>
<br />
<br />

Step 5. After you click OK a new warning pop up window will open. Click OK.

<p>
<img src="https://imgur.com/3op4m7H.png alt="Open Budgeteer"/>
</p>
<br />
<br />

Step 6. After you click OK, select your “Install OpenBudgeteer” Task then click the “Run” tab. You will be asked to run Install OpenBudgeteer – click Yes. Follow the instructions in the image below.

<p>
<img src="https://imgur.com/ohjz8xD.png alt="Open Budgeteer"/>
</p>
<br />
<br />

Step 7. The installation process can take up to a few seconds/minutes. It will depend on your Internet speed connection. Now open your browser and type in http://Your-Synology-ip-address:6100 

<p>
<img src="https://imgur.com/B3Oghy3.png alt="Open Budgeteer"/>
</p>
<br />
<br />

Step 8. Click New Account

<p>
<img src="https://imgur.com/aP93hAv.png alt="Open Budgeteer"/>
</p>
<br />
<br />

Step 9. Choose an account name. Click Save.

<p>
<img src="https://imgur.com/ajsyhOZ.png alt="Open Budgeteer"/>
</p>
<br />
<br />


Step 10. Import transactions from your Online Banking account. OpenBudgeteer supports CSV files.

<p>
<img src="https://imgur.com/CJiPwKU.png alt="Open Budgeteer"/>
</p>
<br />
<br />


Here is an example after you have created an account and imported transctions:

<p>
<img src="https://imgur.com/MnVZ67G.png alt="Open Budgeteer"/>
</p>
<br />
<br />


Thank You for looking. For more content, visit my website 










