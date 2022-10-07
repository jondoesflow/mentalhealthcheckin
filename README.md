# INTRODUCTION

I was asked by Microsoft to write a blog post on their Humans of IT series - https://techcommunity.microsoft.com/t5/humans-of-it-blog/guest-blog-6-ways-to-maintain-and-foster-your-tech-superpower/ba-p/1120971

This is an evolved version of the first version of this app that I made (https://github.com/jondoesflow/mentalhealthcheckinpowerapp).  Along the way I have improved it, moving away from a SharePoint back end to Dataverse. Also, it is now packed into a solution.

Thanks for reading.

# Mental Health Check In solution
This is a mental health check in application built in the Power Platform. It comprises of four main elements:

1. "Are you ok" Canvas App.  Allows a user to submit how they are feeling and get signposted to various Mental Health charities that can help in times of crisis.
2. "Resources" Model-Driven app. Allows back end support staff to add mental health charities and other organisations that they see fit, that can then be surfaced inside the Canvas app.
3. "Mental Health" Dataverse table.  Records the entries created from the "Are you ok" Canvas app.
4. "Resources" Dataverse table.  Mental health charities that are surfaced into the "Are you ok" Canvas app for signposting for users.

# Changes to previous iteration

1. Moved away from SharePoint backend to Dataverse.
2. "Are you ok" Canvas app Check In button now pushes data directly to "Mental Health" Dataverse table via a PATCH function.

# Licensing requirements

To use this application you will need a Power Apps Per User or Power Apps Per App license.

# Installation

1. Download the managed or unmanaged solution from the repo and browse to https://make.powerapps.com and go to Solutions and Import.
2. Once the solution has installed, click into it and expand the Tables section. 
3. Choose the Resources Dataverse table and click Import > Import data from Excel, in the ribbon.
4. Click upload.
5. Browse to the jdfresources.csv file and open it
6. Wait till you see "Mapping is successful"
7. Click Import
8. Verify that some data exists by refreshing the Power Apps studio page

# Smoke Test

1. Click on the Apps section of the solution, and play the Are you Ok Canvas app (you may be asked to start a Power Apps trial if you do not have a license at this point).
2. Allow the app to capture your location.
3. Allow the permissions
4. Submit an entry into the app, and check the data in the Mental Health table
5. Click on the More info button to be taken to the signposting area, verify that data is present.
