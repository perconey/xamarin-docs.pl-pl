---
title: "Osadzanie .NET w języku Java"
description: "Jak używać biblioteki Xamarin .NET w opartych na języku Java natywnego projekt systemu Android"
ms.topic: article
ms.prod: xamarin
ms.assetid: A489EEF3-1008-4257-BF63-FE21D8C23821
ms.technology: xamarin-android
author: mgmclemore
ms.author: mamcle
ms.date: 02/15/2018
ms.openlocfilehash: 1a25f4bc39e39ce58a07ed399082bf13284c16e9
ms.sourcegitcommit: 6cd40d190abe38edd50fc74331be15324a845a28
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/27/2018
---
# <a name="embedding-net-in-java"></a>Osadzanie .NET w języku Java

W niektórych przypadkach możesz dodać do istniejącego projektu systemu Android native biblioteki Xamarin .NET. Aby to zrobić, można użyć [Embeddinator 4000](https://mono.github.io/Embeddinator-4000/) narzędzia, aby włączyć biblioteki .NET do natywnej biblioteki, który można włączyć do natywnych aplikacji systemu Android opartych na języku Java.

 
## <a name="requirements"></a>Wymagania

Aby użyć Embeddinator 4000 z językiem Java w systemie Android, potrzebne następujące elementy:

-   **Android Studio** &ndash; [Android Studio 3.x](https://developer.android.com/studio/preview/index.html) lub nowszym należy zainstalować.

-   **Xamarin.Android** &ndash; [Xamarin.Android 7.4.99](https://jenkins.mono-project.com/view/Xamarin.Android/job/xamarin-android/lastSuccessfulBuild/Azure/) lub nowszym należy zainstalować.

-   **Java Developer Kit** &ndash; [Java 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) lub nowszym należy zainstalować.

-   **Mono** &ndash; [Mono 5.0](http://www.mono-project.com/download/) lub nowszym należy zainstalować.


# <a name="visual-studiotabvswin"></a>[Visual Studio](#tab/vswin)

Visual Studio umożliwia edytowanie i kompilowania kodu C#.

# <a name="visual-studio-for-mactabvsmac"></a>[Visual Studio for Mac](#tab/vsmac)

Visual Studio for Mac można użyć do edycji i kompilowania kodu C#.

-----

 
## <a name="using-the-embeddinator-4000"></a>Przy użyciu Embeddinator 4000

Aby korzystać z biblioteki .NET w macierzystym projekt systemu Android, należy użyć następujących czynności:

1.  Tworzenie projektu biblioteki systemu Android C#.

2.  Zainstaluj Embeddinator-4000 za pośrednictwem pakietu NuGet.

3.  Uruchom Embeddinator w zestawie biblioteki systemu Android.

4.  Użyj wygenerowanego pliku AAR w projekcie języka Java w programie Android Studio.

Te kroki opisano szczegółowo w [Embeddinator 4000](https://mono.github.io/Embeddinator-4000/getting-started-java-android.html) dokumentacji.