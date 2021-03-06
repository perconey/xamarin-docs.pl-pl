---
title: Pojęcia zaawansowane i elementy wewnętrzne
description: Podstawową architekturę za platformy Xamarin.Android i jego projekt interfejsu API.
ms.prod: xamarin
ms.assetid: CC6A0D52-E9FA-4270-B3FA-84660621D6D5
ms.technology: xamarin-android
author: mgmclemore
ms.author: mamcle
ms.date: 10/13/2017
ms.openlocfilehash: 517e21f2decd0dabbd03d752f13831a891ad7138
ms.sourcegitcommit: 945df041e2180cb20af08b83cc703ecd1aedc6b0
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/04/2018
---
# <a name="advanced-concepts-and-internals"></a>Pojęcia zaawansowane i elementy wewnętrzne


##  <a name="architectureandroidinternalsarchitecturemd"></a>[Architektura](~/android/internals/architecture.md)

W tym artykule opisano podstawową architekturę za aplikacji platformy Xamarin.Android. Wyjaśnia sposób uruchamiania aplikacji platformy Xamarin.Android w środowisku wykonywania Mono wraz ze środowiskiem uruchomieniowym Android maszyny wirtualnej, a wyjaśniono takie podstawowe pojęcia jako Android wywoływane otoki i zarządzane wywoływane otoki. 



##  <a name="api-designandroidinternalsapi-designmd"></a>[Projekt interfejsu API](~/android/internals/api-design.md)

Oprócz podstawowych podstawowej biblioteki klas, które są częścią Mono Xamarin.Android jest dostarczany z powiązań dla różnych Android interfejsów API umożliwiają deweloperom tworzenie natywnych aplikacji systemu Android z Mono.

Fundament platformy Xamarin.Android jest aparat międzyoperacyjnego tego world mostków C# innym osobom Java i dostarcza deweloperom dostępu do interfejsów API języka Java z języka C# lub innych języków .NET.



##  <a name="assembliescross-platforminternalsavailable-assembliesmd"></a>[Zestawy](~/cross-platform/internals/available-assemblies.md)

Xamarin.Android jest dostarczany z wielu zestawów. Tak samo, jak Silverlight jest rozszerzona podzbiór pulpitu zestawów platformy .NET, Xamarin.Android jest również rozszerzonej podzbiór kilka Silverlight i pulpitu zestawów platformy .NET. 

