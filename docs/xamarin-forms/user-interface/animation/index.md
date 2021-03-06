---
title: Animacja
description: Platformy Xamarin.Forms zawiera własną infrastrukturę animacji, która jest prosty do tworzenia prostych animacji, będąc również elastyczne do tworzenia złożonych animacji.
ms.prod: xamarin
ms.assetid: AC0B4127-ECA3-44DA-8A24-A2B10A275083
ms.technology: xamarin-forms
author: davidbritch
ms.author: dabritch
ms.date: 07/14/2016
ms.openlocfilehash: 7cff122e7ecc24f5ad93bd863ee422981871f857
ms.sourcegitcommit: 945df041e2180cb20af08b83cc703ecd1aedc6b0
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/04/2018
---
# <a name="animation"></a>Animacja

_Platformy Xamarin.Forms zawiera własną infrastrukturę animacji, która jest prosty do tworzenia prostych animacji, będąc również elastyczne do tworzenia złożonych animacji._

Klasy animacji platformy Xamarin.Forms docelowych inne właściwości elementów wizualnych, typowe Animacja stopniowo zmiana właściwości z jedną wartość na inny w danym okresie czasu. Należy pamiętać, że nie ma interfejsu XAML dla klas animacji platformy Xamarin.Forms. Jednak animacji można hermetyzowane w [zachowania](~/xamarin-forms/app-fundamentals/behaviors/index.md) , a następnie odwołanie z XAML.

## <a name="simple-animationssimplemd"></a>[Proste animacje](simple.md)

[ `ViewExtensions` ](https://developer.xamarin.com/api/type/Xamarin.Forms.ViewExtensions/) Klasy udostępnia metody rozszerzenia, które mogą służyć do tworzenia prostych animacji, które obracanie, skalowanie tłumaczenie i zanikania [ `VisualElement` ](https://developer.xamarin.com/api/type/Xamarin.Forms.VisualElement/) wystąpień. W tym artykule przedstawiono tworzenie i anulowanie animacji przy użyciu `ViewExtensions` klasy.

## <a name="easing-functionseasingmd"></a>[Funkcje easingu](easing.md)

Obejmuje platformy Xamarin.Forms [ `Easing` ](https://developer.xamarin.com/api/type/Xamarin.Forms.Easing/) klasy, która pozwala określić funkcji przenoszenia, która kontroluje sposób przyspieszenia animacji lub spowolnić nich uruchomiony. W tym artykule przedstawiono, jak używać funkcji sterowania tempem zmian wstępnie zdefiniowane i sposób tworzenia niestandardowych funkcji sterowania tempem zmian.

## <a name="custom-animationscustommd"></a>[Niestandardowe animacje](custom.md)

[ `Animation` ](https://developer.xamarin.com/api/type/Xamarin.Forms.Animation/) Klasy jest blokiem konstrukcyjnym wszystkie animacje platformy Xamarin.Forms, za pomocą metod rozszerzenia w [ `ViewExtensions` ](https://developer.xamarin.com/api/type/Xamarin.Forms.ViewExtensions/) klasy utworzenie co najmniej jednego `Animation` obiektów. W tym artykule przedstawiono sposób użycia `Animation` klasa do tworzenia i anulować animacji, synchronizowanie wielu animacji i utworzyć niestandardowe animacji, które animowania właściwości, które nie są animowane przez istniejące metody animacji.

