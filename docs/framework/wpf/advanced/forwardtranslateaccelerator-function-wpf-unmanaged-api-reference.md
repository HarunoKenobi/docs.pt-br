---
title: Função ForwardTranslateAccelerator (referência de API não gerenciada WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ForwardTranslateAccelerator
api_location:
- PresentationHost_v0400.dll
ms.assetid: fff47a86-9d9f-4176-9530-10e1876e393f
ms.openlocfilehash: 4bb7e665bb836dc5f95b14f39179f1d4b9f8173d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61960908"
---
# <a name="forwardtranslateaccelerator-function-wpf-unmanaged-api-reference"></a>Função ForwardTranslateAccelerator (referência de API não gerenciada WPF)
Essa API dá suporte à infraestrutura do Windows Presentation Foundation (WPF) e não se destina a ser usado diretamente do seu código.  
  
 Usado pela infraestrutura do Windows Presentation Foundation (WPF) para gerenciamento do windows.  
  
## <a name="syntax"></a>Sintaxe  
  
```cpp  
HRESULT ForwardTranslateAccelerator(  
   MSG* pMsg,   
   VARIANT_BOOL appUnhandled  
)  
```  
  
## <a name="parameters"></a>Parâmetros  
 pMsg  
 Um ponteiro para uma mensagem.  
  
 appUnhandled  
 `true` Quando o aplicativo já tem a oportunidade de manipular a mensagem de entrada, mas não tratada. Caso contrário, `false`.  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** Ver [requisitos de sistema do .NET Framework](../../get-started/system-requirements.md).  
  
 **DLL:**  
  
 No .NET Framework 3.0 e 3.5: PresentationHostDLL.dll  
  
 No .NET Framework 4 e posterior: PresentationHost_v0400.dll  
  
 **Versão do .NET framework:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]  
  
## <a name="see-also"></a>Consulte também

- [Referência de API não gerenciada do WPF](wpf-unmanaged-api-reference.md)
