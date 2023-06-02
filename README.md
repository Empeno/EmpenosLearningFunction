## Table of Contents

- [Deployment slots](#deployment-slots)
   - [What is deployemnt slots in Azure?](#what-is-azure-functions)
   - [What is an Azure Function deployment slot?](#what-is-an-azure-function-deployment-slot)
   - [How are functions affected when swapping deployment slots?](#how-are-functions-affected-when-swapping-deployment-slots)
   - [How to create a deployment slot?](#how-to-create-a-deployment-slot)
   - [How to swap deployment slots?](#how-to-swap-deployment-slots)
   - [How to delete a deployment slot?](#how-to-delete-a-deployment-slot)
   - [How to configure deployment slots?](#how-to-configure-deployment-slots)
   - [How to monitor deployment slots?](#how-to-monitor-deployment-slots)
   - [How to view deployment slot settings?](#how-to-view-deployment-slot-settings)
   - [How to view deployment slot logs?](#how-to-view-deployment-slot-logs)
   - [How to view deployment slot metrics?](#how-to-view-deployment-slot-metrics)
   - [How to view deployment slot usage?](#how-to-view-deployment-slot-usage)
   - [How to deploy to a deployment slot?](#how-to-deploy-to-a-deployment-slot)



## Deployment slots
### What is deployemnt slots in Azure?
Deployment slots are live apps with their own hostnames. App content and configurations elements can be swapped between two deployment slots, including the production slot.

### What is an Azure Function deployment slot?
Azure Functions deployment slots are a great way to apply changes to a function app without affecting the production version of the app. Common use cases for deployment slots include:

* Staged publishing: In this approach, you deploy a function app to a staging slot, then swap into production slot after testing is complete.
* Testing in production: In this approach, you deploy a function app to a slot that is already serving production traffic. You then test the app in the slot before swapping into production.
* Blue-green deployment: This approach uses two identical deployment slots, and gradually shifts traffic from one slot to the other by using the App Service provider's own traffic distribution mechanism. This approach enables you to validate app changes in a staging deployment slot before swapping it with the production slot.

### How are functions affected when swapping deployment slots?

* Traffic redirection is seamless; no requests are dropped because of a swap. This seamless behavior is a result of the next function triggers being routed to the swapped slot.
* Currently executing function are terminated during the swap. Please review [Improve the performance and reliability of Azure Functions](https://learn.microsoft.com/en-us/azure/azure-functions/performance-reliability#write-functions-to-be-stateless) to learn how to write stateless and defensive functions.


### How to create a deployment slot?
1. Open the Azure portal and navigate to your function app.
2. Select Deployment slots in the left navigation.
3. Select Add Slot.
4. In the Add a slot dialog box, give the slot a name, and select whether to clone app configuration from another existing deployment slot. Select Add to continue.
5. After the slot is added, select Close to close the dialog box.

### How to swap deployment slots?
1. Open the Azure portal and navigate to your function app.
2. Select Deployment slots in the left navigation.
3. Select Swap.
4. In the Swap dialog box, select the Source slot and the Destination slot. Select Swap to continue.
5. After the swap is complete, select Close to close the dialog box.

### How to delete a deployment slot?
1. Open the Azure portal and navigate to your function app.
2. Select Deployment slots in the left navigation.
3. Select the slot you want to delete.
4. Select Delete.
5. In the Delete dialog box, select Delete to confirm the deletion.

### How to configure deployment slots?
1. Open the Azure portal and navigate to your function app.
2. Select Deployment slots in the left navigation.
3. Select the slot you want to configure.
4. Select Configuration.
5. Configure the settings you want to change. For more information, see Configure function app settings.
6. Select Save.

### How to monitor deployment slots?
1. Open the Azure portal and navigate to your function app.
2. Select Deployment slots in the left navigation.
3. Select the slot you want to monitor.
4. Select Monitor.
5. Select the metrics you want to monitor. For more information, see Monitor Azure Functions.
6. Select Save.

### How to view deployment slot settings?
1. Open the Azure portal and navigate to your function app.
2. Select Deployment slots in the left navigation.
3. Select the slot you want to view.
4. Select Properties.

### How to view deployment slot logs?
1. Open the Azure portal and navigate to your function app.
2. Select Deployment slots in the left navigation.
3. Select the slot you want to view.
4. Select Logs.

### How to view deployment slot metrics?
1. Open the Azure portal and navigate to your function app.
2. Select Deployment slots in the left navigation.
3. Select the slot you want to view.
4. Select Metrics.

### How to view deployment slot usage?
1. Open the Azure portal and navigate to your function app.
2. Select Deployment slots in the left navigation.
3. Select the slot you want to view.
4. Select Usage.

### How to deploy to a deployment slot?
1. Open the Azure portal and navigate to your function app.
2. Select Deployment slots in the left navigation.
3. Select the slot you want to deploy to.
4. Select Deployment Center.
5. Select the source you want to deploy from. For more information, see Deploy to Azure Functions.
6. Select Continue.
7. Configure the settings you want to change. For more information, see Configure function app settings.
8. Select Save.

