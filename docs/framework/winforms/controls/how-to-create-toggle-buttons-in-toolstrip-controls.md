---
title: 'Como: Criar botões de alternância em controles ToolStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toggle buttons [Windows Forms], creating
- examples [Windows Forms], toolbars
- ToolStrip control [Windows Forms], creating toggle buttons
ms.assetid: d9c197df-4c65-43f2-beee-b68b52b2befc
ms.openlocfilehash: 21da5564bfeec01d448c23d3e734bdd16fc1566b
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64666428"
---
# <a name="how-to-create-toggle-buttons-in-toolstrip-controls"></a>Como: Criar botões de alternância em controles ToolStrip
Quando um usuário clica em um botão de alternância, ele é exibido em baixo-relevo e retém a aparência em baixo-relevo até que o usuário clica no botão novamente.  
  
### <a name="to-create-a-toggling-toolstripbutton"></a>Para criar um alternância ToolStripButton  
  
- Use um código como o exemplo de código a seguir. Esse código supõe que o formulário contém um <xref:System.Windows.Forms.ToolStrip> controle e que seus <xref:System.Windows.Forms.ToolStrip.Items%2A> coleção contém um <xref:System.Windows.Forms.ToolStripButton> chamado `toolStripButton1`. Ele também pressupõe que você tenha um manipulador de eventos chamado `toolStripButton1_CheckedChanged`.  
  
    ```vb  
    toolStripButton1.CheckOnClick = True  
    toolStripButton1.CheckedChanged AddressOf _  
    EventHandler(toolStripButton1_CheckedChanged);  
    ```  
  
    ```csharp  
    toolStripButton1.CheckOnClick = true;  
    toolStripButton1.CheckedChanged += new _  
    EventHandler(toolStripButton1_CheckedChanged);  
    ```  
  
## <a name="see-also"></a>Consulte também

- <xref:System.Windows.Forms.ToolStripButton>
- [Visão geral do controle ToolStrip](toolstrip-control-overview-windows-forms.md)
