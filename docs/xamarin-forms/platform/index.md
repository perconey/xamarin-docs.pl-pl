---
title: Funkcje platformy
description: Korzystać z funkcji specyficznych dla platformy z platformy Xamarin.Forms
ms.prod: xamarin
ms.assetid: 2C6CE42C-E380-4BB9-90CC-D0F4E60C4C03
ms.technology: xamarin-forms
author: davidbritch
ms.author: dabritch
ms.date: 12/20/2017
ms.openlocfilehash: fd46411f3662652ef26addc76f273d6071401a6f
ms.sourcegitcommit: bc39d85b4585fcb291bd30b8004b3f7edcac4602
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2018
---
# <a name="platform-features"></a>Funkcje platformy

Platformy Xamarin.Forms umożliwia wprowadzają funkcje specyficzne dla platformy przy użyciu i jest rozszerzalny [efekty](~/xamarin-forms/app-fundamentals/effects/index.md), [niestandardowe moduły renderowania](~/xamarin-forms/app-fundamentals/custom-renderer/index.md), [DependencyService](~/xamarin-forms/app-fundamentals/dependency-service/index.md), [MessagingCenter](~/xamarin-forms/app-fundamentals/messaging-center.md)itd.

## <a name="androidandroidindexmd"></a>[Android](android/index.md)

Ten przewodnik opisuje sposób implementowania projektu materiałów, aktualizując istniejących aplikacji platformy Xamarin.Forms Android.

## <a name="application-indexing-and-deep-linkingdeep-linkingmd"></a>[Indeksowanie aplikacji i tworzenie linku do strony docelowej](deep-linking.md)

Indeksowanie aplikacji umożliwia aplikacji, które w przeciwnym razie mogłyby zapomniane, po kilku używa pozostanie odpowiednich przez znajdujących się w wynikach wyszukiwania. Bezpośrednich połączeń umożliwia aplikacjom na odpowiadanie na wynik wyszukiwania, które zwykle zawiera dane aplikacji, przechodząc na stronę odwołanie z link bezpośredni.

## <a name="device-classdevicemd"></a>[Klasa urządzenia](device.md)

Jak używać `Device` klasy w celu utworzenia zachowanie specyficzne dla platformy w kodzie udostępnionego i interfejs użytkownika (w tym przy użyciu kodu XAML). Obejmuje również `BeginInvokeOnMainThread` co jest niezbędne, modyfikując formantów interfejsu użytkownika z wątki w tle.

## <a name="iosiosindexmd"></a>[iOS](ios/index.md)

Niektóre style z systemem iOS można wykonać za pomocą **Info.plist** i `UIAppearance` interfejsu API. Ten przewodnik zawiera przykłady obejmują funkcje systemu iOS 9 w aplikacji systemu iOS rozwiązania platformy Xamarin.Forms, w tym przez wyszukiwanie Core Spotlight.

## <a name="gtkgtkmd"></a>[GTK](gtk.md)

Platformy Xamarin.Forms ma teraz obsługę podglądu GTK # aplikacji.

## <a name="macmacmd"></a>[Mac](mac.md)

Platformy Xamarin.Forms ma teraz obsługę podglądu macOS aplikacji.

## <a name="wpfwpfmd"></a>[WPF](wpf.md)

Platformy Xamarin.Forms ma teraz obsługę podglądu dla aplikacji Windows Presentation Foundation (WPF).

## <a name="native-formsnative-formsmd"></a>[Formularze natywne](native-forms.md)

Formularze natywnego Zezwalaj platformy Xamarin.Forms [ `ContentPage` ](https://developer.xamarin.com/api/type/Xamarin.Forms.ContentPage/)-pochodnych stron, które mają być używane przez projektów natywnych Xamarin.iOS, Xamarin.Android i systemu Windows platformy Uniwersalnej.

## <a name="native-viewsnative-viewsindexmd"></a>[Widoki natywne](native-views/index.md)

Natywny widoków z systemem iOS, Android i platformy uniwersalnej systemu Windows można odwoływać się bezpośrednio z platformy Xamarin.Forms. W widokach natywny można ustawić właściwości i procedury obsługi zdarzeń i współdziałają z widokami platformy Xamarin.Forms.

## <a name="platform-specificsplatform-specificsindexmd"></a>[Szczegóły platformy](platform-specifics/index.md)

Szczegóły platformy pozwalają na korzystanie z funkcji, które są dostępne tylko na danej platformie, bez konieczności niestandardowe moduły renderowania lub efekty.

## <a name="pluginspluginsmd"></a>[Wtyczki](plugins.md)

Są dostępne w witrynie Github, Nuget i magazynie składników Xamarin pomóc wydłużyć aplikacji platformy Xamarin.Forms szerokiej gamy dodatki typu open source.

## <a name="windowswindowsindexmd"></a>[Windows](windows/index.md)

Platformy Xamarin.Forms obsługuje cztery różne typy projekt dla systemu Windows:

* Windows Phone 8 Silverlight (oryginalnej platformy Windows obsługiwana przez platformy Xamarin.Forms),
* Windows Phone 8.1 (WinRT)
* Windows 8.1 (WinRT), a
* Platforma uniwersalna systemu Windows (Windows 10).

W tej sekcji opisano różnice między nimi i sposobu dodawania ich do istniejącego rozwiązania platformy Xamarin.Forms.
