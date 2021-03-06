---
title: "CreatePoint | Microsoft Docs"
description: "Returns a GeoJSON Point record. The result of a CreatePoint can be used as input to other Geospatial functions."
applies_to: 
  - "Azure"
services: stream-analytics
author: jasonwhowell
manager: kfile

ms.service: stream-analytics
ms.topic: reference
ms.assetid: b49facae-be27-4e6b-a2e8-299d6f9c41e4
caps.latest.revision: 4
ms.workload: data-services
ms.date: 02/01/2017
ms.author: jasonh
---

# CreatePoint
  Returns a GeoJSON Point record. The result of a CreatePoint can be used as input to other Geospatial functions.  
  
 **Syntax**  
  
```  
CreatePoint (latitude, longitude)  
```  
  
## Argument  
 **Latitude**  
  
 Is the latitude of a geographic point, value must be float.  
  
 **Longitude**  
  
 Is the longitude of a geographic point, value must be float.  
  
## Return Type  
 Returns a GeoJSON point record with Point as type and an array with latitude and longitude as coordinates.  
  
## Example  
  
```SQL  
 SELECT  
     CreatePoint(input.latitude, input.longitude)  
FROM input  
  
```  
  
### Input Example  
  
|latitude|longitude|  
|--------------|---------------|  
|3.0|-10.2|  
|-87.33|20.2321|  
  
### Output Example  
 {"type" : "Point", "coordinates" : [-10.2, 3.0]}  
  
 {"type" : "Point", "coordinates" : [20.2321, -87.33]}  
  
## See Also  

  
  
