---
title: -win32icon
ms.date: 03/13/2018
helpviewer_keywords:
- win32icon compiler option [Visual Basic]
- -win32icon compiler option [Visual Basic]
- /win32icon compiler option [Visual Basic]
ms.assetid: aecaab01-9353-46c5-941c-6edabd4eff92
ms.openlocfilehash: dc48a8f79aa04892c514917da00b8fd6489695b1
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65593091"
---
# <a name="-win32icon"></a>-win32icon
Insere um arquivo. ico no arquivo de saída. Esse arquivo. ico representa o arquivo de saída no **Explorador de arquivos**.  
  
## <a name="syntax"></a>Sintaxe  
  
```  
-win32icon:filename  
```  
  
## <a name="arguments"></a>Arguments  
  
|Termo|Definição|  
|---|---|  
|`filename`|O arquivo. ico para adicionar ao seu arquivo de saída. Coloque o nome do arquivo entre aspas ("") se ele contiver um espaço.|  
  
## <a name="remarks"></a>Comentários  
 Você pode criar um arquivo. ico com o compilador de recurso do Microsoft Windows (RC). O compilador de recurso é invocado quando você compila um programa do Visual C++; um arquivo. ico é criado a partir do arquivo. rc. O `-win32icon` e `-win32resource` são mutuamente exclusivas.  
  
 Ver [- linkresource (Visual Basic)](../../../visual-basic/reference/command-line-compiler/linkresource.md) para fazer referência a um arquivo de recurso do .NET Framework, ou [-resource (Visual Basic)](../../../visual-basic/reference/command-line-compiler/resource.md) para anexar um arquivo de recurso do .NET Framework. Ver [-win32resource](../../../visual-basic/reference/command-line-compiler/win32resource.md) para importar um arquivo. res.  
  
|Para definir - win32icon no IDE do Visual Studio|  
|---|  
|1.  Selecione um projeto no **Gerenciador de Soluções**. No menu **Projeto**, clique em **Propriedades**. <br />2.  Clique na guia **Aplicativo**.<br />3.  Modificar o valor de **ícone** caixa.|  
  
## <a name="example"></a>Exemplo  
 O seguinte código compila `In.vb` e anexa um arquivo. ico, `Rf.ico`.  
  
```console
vbc -win32icon:rf.ico in.vb  
```  
  
## <a name="see-also"></a>Consulte também

- [Compilador de linha de comando do Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [Linhas de Comando de Compilação de Exemplo](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
