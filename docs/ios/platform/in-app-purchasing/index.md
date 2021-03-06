---
title: Zakup w aplikacji
description: aplikacje systemu iOS sprzedać cyfrowe produktów i usług przy użyciu interfejsów API zestawu magazynu. Produkty są tworzone i zarządzane w portalu Connect iTunes. Apple zarządza przetwarzanie transakcji i zatwierdza wszystkie produkty przed ich można sprzedać, a opłaty opłaty za każdą transakcję (obecnie 30%). Firma Apple wymaga, że używasz zakupu w aplikacji dla żadnej cyfrowe sprzedaży w aplikacji, ale nie można używać go sprzedaży fizycznych towarów lub usług-cyfrowego. Aplikacje, które oferują opcje płatności alternatywny cyfrowe produkty i usługi są prawdopodobnie odrzucane. Ten dokument wyjaśniono, jak skonfigurować aplikację tak, aby użyć zestawu magazynu i zawiera przykłady najbardziej typowych scenariuszy zakupów w aplikacji platformy Xamarin.iOS.
ms.prod: xamarin
ms.assetid: B41929D8-47E4-466D-1F09-6CC3C09C83B2
ms.technology: xamarin-ios
author: bradumbaugh
ms.author: brumbaug
ms.openlocfilehash: 7a8dec6051caeba55c45df29c085ecfcddd160d2
ms.sourcegitcommit: 945df041e2180cb20af08b83cc703ecd1aedc6b0
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/04/2018
---
# <a name="in-app-purchasing"></a>Zakup w aplikacji

_aplikacje systemu iOS sprzedać cyfrowe produktów i usług przy użyciu interfejsów API zestawu magazynu. Produkty są tworzone i zarządzane w portalu Connect iTunes. Apple zarządza przetwarzanie transakcji i zatwierdza wszystkie produkty przed ich można sprzedać, a opłaty opłaty za każdą transakcję (obecnie 30%). Firma Apple wymaga, że używasz zakupu w aplikacji dla żadnej cyfrowe sprzedaży w aplikacji, ale nie można używać go sprzedaży fizycznych towarów lub usług-cyfrowego. Aplikacje, które oferują opcje płatności alternatywny cyfrowe produkty i usługi są prawdopodobnie odrzucane. Ten dokument wyjaśniono, jak skonfigurować aplikację tak, aby użyć zestawu magazynu i zawiera przykłady najbardziej typowych scenariuszy zakupów w aplikacji platformy Xamarin.iOS._


aplikacje systemu iOS sprzedać cyfrowe produktów lub usług przy użyciu StoreKit — zestaw interfejsów API dostarczonych przez system iOS, które komunikują się z serwerami firmy Apple do przeprowadzania transakcji finansowych z użytkownikiem za pośrednictwem ich Apple ID. Interfejsy API StoreKit dotyczy głównie podczas pobierania informacji o produkcie i przeprowadzanie transakcji — nie składnik interfejsu użytkownika. Aplikacje, które implementują zakupu w aplikacji należy Tworzenie interfejsu użytkownika i śledzić zakupione elementy kodu niestandardowego, aby zapewnić użytkownikowi wymaganych produktów lub usług.

Dostarczanie funkcji zakupu w aplikacji wymaga kilku kroków:

-  **Konfigurowanie aplikacji** — aplikacji profilu inicjowania obsługi administracyjnej, należy skonfigurować poprawnie.
-  **Tworzenie produktów** — opisy produktu i ceny muszą być tworzone w portalu Connect iTunes.
-  **Implementowanie StoreKit** — StoreKit interfejsu API musi zostać wdrożone zgodnie z typów są sprzedanych produktów.
-  **Tworzenie interfejsu użytkownika i samych produktów** — produkty muszą zostać zaimplementowane, łącznie z mechanizmów śledzenia każdego zakupu i tworzenia kopii zapasowej i przywracania ich w razie potrzeby.
-  **Monitorowanie sprzedaży i uzyskania środków** — Użyj informacji dostarczonych przez iTunes Connect, aby monitorować trendy sprzedaży i śledzić przychodów.


Tym dokumencie wyjaśniono, jak wykonać te kroki w ramach zapewnienia zakupy w aplikacjach za pomocą platformy Xamarin.iOS.


## <a name="requirements"></a>Wymagania

Aby obsługiwać zakupu w aplikacji należy użyć Xamarin.iOS 5.0 lub nowszej Xcode 7 lub nowszym.

## <a name="contents"></a>Spis treści

 * [Konfiguracja i podstawowe informacje dotyczące zakupów w aplikacji](~/ios/platform/in-app-purchasing/in-app-purchase-basics-and-configuration.md)

 * [Omówienie zestawu Store Kit i pobieranie informacji o produkcie](~/ios/platform/in-app-purchasing/store-kit-overview-and-retreiving-product-information.md)

 * [Zakup produktów, które można wykorzystać](~/ios/platform/in-app-purchasing/purchasing-consumable-products.md)

 * [Zakup produktów, których nie można wykorzystać](~/ios/platform/in-app-purchasing/purchasing-non-consumable-products.md)

 * [Transakcje i weryfikacja](~/ios/platform/in-app-purchasing/transactions-and-verification.md)

 * [Subskrypcje i raportowanie](~/ios/platform/in-app-purchasing/subscriptions-and-reporting.md)


## <a name="summary"></a>Podsumowanie

Ten artykuł ma wprowadzono koncepcję zakupu w aplikacji, opisano sposób konfigurowania aplikacji w taki sposób, aby wykorzystać go i przedstawione przykłady użycia platformy Xamarin.iOS. Pokrywającego:

-  **System iOS w portalu inicjowania obsługi** — wskazówki dotyczące włączania w aplikacji zakupu funkcji.
-  **Połącz iTunes** — Konfigurowanie produktów, sprzedaż w aplikacji.
-  **Przechowywanie zestawu** — wyjaśnienie klasy używane do tworzenia funkcji zakupu w aplikacji.
-  **Kodowanie aplikacji do zakupu** — przykłady sposobu tworzenia zakupu w aplikacji do aplikacji platformy Xamarin.iOS.
-  **Raportowanie** — Przegląd statystyk dostępne za pośrednictwem programu iTunes Connect.


## <a name="related-links"></a>Linki pokrewne

- [InAppPurchaseSample](https://developer.xamarin.com/samples/StoreKit/)
- [W Podręczniku programowania w języku zakupu aplikacji](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/StoreKitGuide/Introduction.html)
- [Przewodnik dewelopera Connect iTunes](https://developer.apple.com/library/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/iTunesConnect_Guide.pdf)
- [Odwołanie do zestawu platformy magazynu](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/StoreKit_Collection/StoreKit_Collection.pdf)
- [Identyfikatory produktu zakupu w aplikacji pytań i odpowiedzi](https://developer.apple.com/library/ios/#qa/qa1329/_index.html)
- [Uwaga techniczna zakupu w aplikacji](https://developer.apple.com/library/ios/#technotes/tn2259/_index.html)
- [Twoje zgłoszenie pierwszy App Store](https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/Introduction/Introduction.html)
- [Centrum zasobów magazynu aplikacji](https://developer.apple.com/appstore/index.html)
- [Wskazówki dotyczące przesyłania sklepu z aplikacjami](https://developer.apple.com/appstore/resources/submission/tips.html)
- [Wytyczne dotyczące sklepu App Store](https://developer.apple.com/appstore/resources/approval/guidelines.html)
- [Zarządzanie aplikacjami](https://developer.apple.com/appstore/resources/managing/index.html)
