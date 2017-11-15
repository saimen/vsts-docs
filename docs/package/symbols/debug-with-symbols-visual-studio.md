---
title: Debug with symbols in Visual Studio
description: Debug with symbols in Visual Studio using the Symbol Server in VSTS Package Management
ms.assetid: 318323C4-5B2F-45DE-A834-CCE03C670F8C
ms.prod: vs-devops-alm
ms.technology: vs-devops-package
ms.manager: douge
ms.author: amullans
ms.date: 10/18/2017
---

# Debug with symbols in Visual Studio

[!INCLUDE [](../_shared/availability-symbols.md)]

Symbol servers enable debuggers to automatically retrieve the correct symbol files without knowing product names, build numbers or package names. To learn more about symbols, read the [concept page](/vsts/package/concepts/symbols); to publish symbols, see [this page](/vsts/build-release/symbols/index). To use symbols in WinDbg, see [this page](debug-with-symbols-windbg.md).

## Add the symbol server to Visual Studio

To debug with symbols, select and add the VSTS symbol server to your Visual Studio environment using the Tools->Options->Debugger->Symbols page.

![Add VSTS Symbol Server in VS Debugger](_img/vsdebugger1.jpg)

In the **Connect to VSTS Symbol Server** dialog, select the VSTS account to which the symbols have been published and the corresponding user identity that has access to this VSTS account. 

![Connect to VSTS Symbol Server](_img/connectsymbolserver.png)

Click **Connect** in the above dialog. The VSTS Symbol Server is now remembered by Visual Studio. When a debugging session begins, Visual Studio will be able to get symbols from VSTS.

![Add VSTS Symbol Server in VS Debugger](_img/vsdebugger2.png)