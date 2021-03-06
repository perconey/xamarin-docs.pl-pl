---
title: Dane i usługi w chmurze
description: Stabilizacji i wskazówki dotyczące wdrażania
ms.prod: xamarin
ms.assetid: 945719F7-7CE6-4207-BF0F-23195125FC84
ms.technology: xamarin-ios
author: bradumbaugh
ms.author: brumbaug
ms.date: 06/13/2017
ms.openlocfilehash: 81aebe5fd7431e578b75c5b61e1d2c92ce546909
ms.sourcegitcommit: 945df041e2180cb20af08b83cc703ecd1aedc6b0
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/04/2018
---
# <a name="data-and-cloud-services"></a>Dane i usługi w chmurze


##  <a name="data-accessiosdata-clouddataindexmd"></a>[Dostęp do danych](~/ios/data-cloud/data/index.md)

Większość aplikacji ma pewne wymagania w celu zapisywania danych na urządzeniu lokalnie. Jeśli nie jest trivially małe ilości danych, zwykle wymaga bazę danych i warstwy danych w aplikacji do zarządzania dostępem do bazy danych. iOS ma aparat bazy danych Sqlite "wbudowane" i dostęp do danych zostało uproszczone dzięki platformy Xamarin w, który jest dostarczany z dostawcy danych SQLite.

##  <a name="icloudiosdata-cloudintroduction-to-icloudmd"></a>[iCloud](~/ios/data-cloud/introduction-to-icloud.md)

Magazyn iCloud interfejsu API w systemie iOS 5 umożliwia aplikacji, aby zapisać użytkownika dokumenty i dane specyficzne dla aplikacji w lokalizacji centralnej i uzyskiwać dostęp do tych elementów z wszystkich urządzeń użytkownika.

##  <a name="cloudkitiosdata-cloudintro-to-cloudkitmd"></a>[CloudKit](~/ios/data-cloud/intro-to-cloudkit.md)

CloudKit framework upraszcza tworzenie aplikacji tego dostępu do usługi iCloud. Obejmuje to pobieranie danych aplikacji i zasobów prawa, jak również mogą bezpiecznie przechowywać informacji o aplikacji. Ten zestaw zapewnia warstwę anonimowość zezwalając na dostęp do aplikacji przy użyciu ich identyfikatorów iCloud bez udostępniania informacji osobistych.