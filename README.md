![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/229755307/22.2)
# Integration of DevExtreme Reports using .NET Core 6.0 and ReactJS document viewer


This example consists of two parts: 

- A server (back-end) .NET Core 6.0 project that enables [cross-domain requests (CORS)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) (Access-Control-Allow-Origin) and implements a custom web report storage.

- Document Viewer and Report Designer front-end client applications created with the [React JavaScript Library](https://reactjs.org/).

## How to Run the Example

Perform the following steps to run this example:

1. Open the back-end project solution (**/iBizzDxReports**) in Visual Studio and run the project. 

2. Add the necessary DevExtreme Nuget report packages and create a sample report.

3. Once the report is designed, save it as a **.repx** file and store the file in the **/Reports** folder.

4. Run the project, perhaps using a terminal opened at the .NET Core project's root directory.

     ```dotnet run```

5. Open up a terminal in **dx-react-report-designer** either of the React apps included and run:

    ```npm install```

4. Run the command to compile and start the client part:

    ```npm start```

5. Navigate to the React project folder that is the client part's root folder. Open the src\App.js file and change the port number in the **host** setting to the back-end application's port.

6. The client application opens the browser at http://localhost:3000/. It displays the **Document Viewer** with a **React JS** emblem sample report.


> NB: The React emblem carries nothing, it simply displays it as an example.


7. Navigate to the React document viewer, that is **dx-react-document-viewer** folder that is the client part's root folder. Open the src\App.js file and change the port number in the **host** setting to the back-end application's port.

8. Open the console and run the following command:

    ```npm install```

9. Run the command to compile and start the client part:

    ```npm start```

9. The client application opens the browser at http://localhost:3000/. It displays the **Report Designer** with the **Products** report.



## Files to Look At


- [Startup.cs](iBizzDxReports/Startup.cs)
- [ReportDesignerController.cs](iBizzDxReports/Controllers/ReportDesignerController.cs)
- [dx-react-document-viewer/src/App.js](./dx-react-document-viewer/src/App.js)
- [dx-react-report-designer/src/App.js](./dx-react-report-designer/src/App.js)


## Documentation

- [Report Designer's Server-Side Configuration (ASP.NET Core)](https://docs.devexpress.com/XtraReports/400196)
- [Document Viewer Integration in React](https://docs.devexpress.com/XtraReports/119338)
- [Report Designer Integration in React](https://docs.devexpress.com/XtraReports/119339)

## More Examples

- [How to Use the Document Viewer in JavaScript with React Library and Npm Package Manager](https://github.com/DevExpress-Examples/reporting-document-viewer-in-javascript-with-react)
- [How to Use the Report Designer in JavaScript with React Library and Npm Package Manager](https://github.com/DevExpress-Examples/reporting-eud-designer-in-javascript-with-react)
- [How to Print and Export a Report in a React Application without Displaying the Report](https://github.com/DevExpress-Examples/Reporting-React-Print-Without-Preview)

Most work done here is credited to @Boris Zaitsev, @Dmitry Golikov and @Vasily. Extra work done by me was to tweak the code and make it compatible with .NET6.0 and DevExtreme 22.2 components. Credit to DevExtreme Team too.