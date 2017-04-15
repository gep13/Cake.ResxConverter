[![Build status](https://ci.appveyor.com/api/projects/status/05yua0ol0wwu0jo9?svg=true
)](https://ci.appveyor.com/project/jzeferino/cake-resxconverter/)   

Cake.ResxConverter
===================

<p align="center">
  <img src="https://github.com/jzeferino/Cake.ResxConverter/blob/master/art/icon.png?raw=true"/>
</p>

Cake.ResxConverter allows [ResxConverter](https://github.com/jzeferino/ResxConverter) use in a [Cake](http://cakebuild.net/) script.

### Usage
```c#
#addin "Cake.ResxConverter"

Task("Run")
  .Does(() =>
{
  // The path for the folder with resx files.
  var resxFolder = "src/Shared/Resources"; 
  
  // Convert the resx files to android into the specified folder.
  ResxConverter.ConvertToAndroid(resxFolder, "artifacts/generated/android");
  
  // Convert the resx files to ios into the specified folder.
  ResxConverter.ConvertToiOS(resxFolder, "artifacts/generated/ios");
});
```

### License
[MIT Licence](LICENSE) 
