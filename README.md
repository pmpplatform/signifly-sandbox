﻿# Get started
This repository contains a .Net backend and a TypeScript frontend following the demo project in Uniscale.

**Get started with the frontend**
To get start with the frontend run:
Install dependencies
> npm install
Start the frontend
> npm start

This will install dependencies and start the frontend application. You can then switch between runninig against the .Net backend by commenting/uncommenting these lines in the index.tsx file
>      registerAccountInterceptors(i)
>      registerStreamsInterceptors(i)

**Get started with the backend**
To restore the NuGet dependencies you first have to add a source for your company in uniscale. If you navigate into Uniscale under Solution editor -> SDK (tab) -> Package management (tab) -> NuGet (tab) you will find the command line you need to run to add the NuGet registry entry. The command starts with the following
> dotnet nuget add source --name SigniflySandbox --...

Run the full command from that view. After restarting Visual Studio it will have recognized the new registry and it can restore the solution.

When the solution is restored you can right click on the account and messages projects in Visual Studio and select
> Debug -> Start new instance

The two services will then be started and are ready to receive requests. If the two interceptor registration functions are commented out in the frontend the request should start coming into your backend services.
