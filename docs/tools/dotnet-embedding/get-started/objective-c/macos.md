---
title: Wprowadzenie do korzystania z macOS
ms.prod: xamarin
ms.assetid: AE51F523-74F4-4EC0-B531-30B71C4D36DF
ms.technology: xamarin-cross-platform
author: topgenorth
ms.author: toopge
ms.date: 11/14/2017
ms.openlocfilehash: f75ced921cd240e280b5dd6f7366ccceefb5e40e
ms.sourcegitcommit: bc39d85b4585fcb291bd30b8004b3f7edcac4602
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2018
---
# <a name="getting-started-with-macos"></a>Wprowadzenie do korzystania z macOS


## <a name="what-you-will-need"></a>Dane będą potrzebne

* Postępuj zgodnie z instrukcjami wyświetlanymi w [wprowadzenie do języka Objective-C](~/tools/dotnet-embedding/get-started/objective-c/index.md) przewodnik.

## <a name="hello-world"></a>Cześć ludzie

Najpierw należy utworzyć przykład prostego Witaj świecie w języku C#.

### <a name="create-c-sample"></a>Tworzenie przykładowej C#

Otwórz program Visual Studio dla komputerów Mac, Utwórz nowy projekt biblioteki klas Mac o nazwie **hello z csharp**i zapisać go do **~/Projects/hello-from-csharp**.

Zastąp kod w `MyClass.cs` pliku następującym fragmentem kodu:

```csharp
using AppKit;
public class MyNSView : NSTextView
{
    public MyNSView ()
    {
        Value = "Hello from C#";
    }
}
```

Skompiluj projekt. Wynikowy zestaw zostanie zapisany jako **~/Projects/hello-from-csharp/hello-from-csharp/bin/Debug/hello-from-csharp.dll**.

### <a name="bind-the-managed-assembly"></a>Powiązanie zestawu zarządzanego

Uruchom embeddinator pozwala utworzyć strukturę macierzystego dla zestawu zarządzanego:

```shell
cd ~/Projects/hello-from-csharp
objcgen ~/Projects/hello-from-csharp/hello-from-csharp/bin/Debug/hello-from-csharp.dll --target=framework --platform=macOS-modern --abi=x86_64 --outdir=output -c --debug
```

Platformę zostaną umieszczone w **~/Projects/hello-from-csharp/output/hello-from-csharp.framework**.

### <a name="use-the-generated-output-in-an-xcode-project"></a>Użyj wygenerowanych danych wyjściowych w projekcie Xcode

Otwórz program Xcode i Utwórz nową aplikację Cocoa. Nadaj mu nazwę **hello z csharp** i wybierz **Objective-C** języka.

Otwórz **~/Projects/hello-from-csharp/output** katalogu w wyszukiwanie, wybierz **hello z csharp.framework**, przeciągnij je do projektu Xcode i upuść ją po prostu powyżej **hello z języka csharp**  folderu w projekcie.

![Przeciągnij i upuść framework](macos-images/hello-from-csharp-mac-drag-drop-framework.png)

Upewnij się, że **skopiować elementy w razie potrzeby** zostanie zaznaczona w oknie dialogowym, które pojawia się, a następnie kliknij przycisk **Zakończ**.

![Kopiuje elementy w razie potrzeby](macos-images/hello-from-csharp-mac-copy-items-if-needed.png)

Wybierz **hello z csharp** projektu i przejdź do **hello z csharp** docelowego **ogólne** kartę. W **binarnych osadzonego** Dodaj **hello z csharp.framework**.

![Osadzone pliki binarne](macos-images/hello-from-csharp-mac-embedded-binaries.png)

Otwórz **ViewController.m**i Zastąp zawartość z:

```objc
#import "ViewController.h"

#include "hello-from-csharp/hello-from-csharp.h"

@implementation ViewController

- (void)viewDidLoad {
    [super viewDidLoad];
    
    MyNSView *view = [[MyNSView alloc] init];
    view.frame = CGRectMake(0, 200, 200, 200);
    [self.view addSubview: view];
}

@end
```

Na koniec Uruchom projekt Xcode i zostaną wyświetlone informacje podobne:

![Witaj z działających w symulatorze próbki C#](macos-images/hello-from-csharp-mac.png)

Przykład więcej pełny i lepiej wyglądających jest dostępny [tutaj](https://github.com/mono/Embeddinator-4000/tree/objc/samples/mac/weather).
