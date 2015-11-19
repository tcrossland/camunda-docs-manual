---

title: 'Deployment View'
weight: 15

menu:
  main:
    identifier: "user-guide-cockpit-deployment-view"
    parent: "user-guide-cockpit"

---

{{< img src="../img/cockpit-deployments-page.png" title="Cockpit Deployment View" >}}

The deployment view of Cockpit shows an overview of all deployments, their resources and the content of these resources. It allows the deletion of existing deployments as well as redeployment of old resources. You can see the content of resources within deployments and download single resources.

# Search

In order to find the deployment you are looking for, you can use the search field at the top of the list of deployments. Similar to the search on the [cockpit dashboard]({{< relref "webapps/cockpit/dashboard.md#search" >}}) and the [tasklist]({{< relref "webapps/tasklist/dashboard.md#search-for-tasks" >}}) you are able to search deployments using an array of available criteria.

You can search by unique ID, name (which does not need to be unique across all deployments), time of deployment and source. The deployment source can be provided when a deployment is created. A deployment that is created by the application during startup will have this property set to process application. If a deployment is made directly in Cockpit (for example using the [dmn live editing]({{< relref "webapps/cockpit/dmn-live-editing.md" >}}) feature), the property will be set to Cockpit, and so on. You can also search for deployments that have no deployment source set und the `Source undefined` criterium.

Independently of your search you can set the ordering of the deployment list using the sorting parameter above the search field. You are able to order by ID, Name and deployment time. You can change the ordering (ascending and descending) by clicking on the arrow on the right side of the sorting criterium.

# Delete

To delete a deployment, hover over the deployment to show the deletion icon {{< glyphicon name="trash" >}}. Before deleting the deployment you can specify whether to also delete instances of resources in this deployment (e.g. running or historic process instances).

# Redeploy

You can redeploy an old deployment to increase the version of all definitions contained in the deployment and therefore overwriting any changed that happened to the definition since the original deployment. To do so, click on de redeploy icon {{< glyphicon name="open" >}} that appears when hovering over a deployment. All contained resources in this deployment will be redeployed. For every contained process, case, or decision definition a new version will be created. This new version will be then the latest version of all definitions with the same key.

You can also redeploy only a single resource within the deployment. To do so, navigate to the resource and click the {{< glyphicon name="open" text=" Redeploy">}} button to redeploy only this single resource.

# Definition Resources

For definition resources, you can see a preview of the diagram or the table on the right side of the page as well as the version number of the definitions contained in this resource. On the bottom of the page, there is a list of definitions with a link to the respective definition pages. The enterprise version also includes the possibility to [edit DMN tables within Cockpit]({{< relref "webapps/cockpit/dmn-live-editing.md" >}}).
