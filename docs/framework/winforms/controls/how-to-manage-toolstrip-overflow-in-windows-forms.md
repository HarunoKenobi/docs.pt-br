---
title: 'Como: Gerenciar o estouro de ToolStrip nos Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], managing overflow
- toolbars [Windows Forms], managing overflow
- examples [Windows Forms], toolbars
- CanOverflow property
ms.assetid: fa10e0ad-4cbf-4c0d-9082-359c2f855d4e
ms.openlocfilehash: 53f610a728925d454a8833a49e705818f027aec5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61913751"
---
# <a name="how-to-manage-toolstrip-overflow-in-windows-forms"></a>Como: Gerenciar o estouro de ToolStrip nos Windows Forms

Quando todos os itens em uma <xref:System.Windows.Forms.ToolStrip> controle não se ajustarem no espaço reservado, você pode habilitar a funcionalidade de estouro em de <xref:System.Windows.Forms.ToolStrip> e determine o comportamento de estouro de determinado <xref:System.Windows.Forms.ToolStripItem>s.

Quando você adiciona <xref:System.Windows.Forms.ToolStripItem>s que exigem mais espaço do que está alocado para o <xref:System.Windows.Forms.ToolStrip> dado o tamanho do formulário atual, um <xref:System.Windows.Forms.ToolStripOverflowButton> aparece automaticamente no <xref:System.Windows.Forms.ToolStrip>. O <xref:System.Windows.Forms.ToolStripOverflowButton> for exibida, e os itens habilitados para estouro são movidos para o menu suspenso de estouro. Isso permite que você personalize e priorizar como seu <xref:System.Windows.Forms.ToolStrip> itens se ajustam a diferentes tamanhos de formulários. Você também pode alterar a aparência dos itens quando eles caem no estouro usando o <xref:System.Windows.Forms.ToolStripItem.Placement%2A> e <xref:System.Windows.Forms.ToolStripOverflow.DisplayedItems%2A?displayProperty=nameWithType> propriedades e o <xref:System.Windows.Forms.ToolStrip.LayoutCompleted> eventos. Se você amplie o formulário no tempo de design ou tempo de execução, mais <xref:System.Windows.Forms.ToolStripItem>s poderão ser exibidos no principal <xref:System.Windows.Forms.ToolStrip> e o <xref:System.Windows.Forms.ToolStripOverflowButton> poderá até desaparecer até que você diminuir o tamanho do formulário.

## <a name="to-enable-overflow-on-a-toolstrip-control"></a>Para habilitar o estouro em um controle ToolStrip

- Certifique-se de que o <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> propriedade não está definida como `false` para o <xref:System.Windows.Forms.ToolStrip>. O padrão é `True`.

     Quando <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> está `True` (padrão), um <xref:System.Windows.Forms.ToolStripItem> é enviada para o menu suspenso de estouro quando o conteúdo do <xref:System.Windows.Forms.ToolStripItem> excede a largura da horizontal <xref:System.Windows.Forms.ToolStrip> ou a altura de uma vertical <xref:System.Windows.Forms.ToolStrip>.

## <a name="to-specify-overflow-behavior-of-a-specific-toolstripitem"></a>Especificar comportamento de estouro de um item ToolStripItem específico

- Defina as <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> propriedade do <xref:System.Windows.Forms.ToolStripItem> para o valor desejado. As possibilidades são `Always`, `Never` e `AsNeeded`. O padrão é `AsNeeded`.

    ```vb
    toolStripTextBox1.Overflow = _
    System.Windows.Forms.ToolStripItemOverflow.Never
    ```

    ```csharp
    toolStripTextBox1.Overflow = _
    System.Windows.Forms.ToolStripItemOverflow.Never;
    ```

## <a name="see-also"></a>Consulte também

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripOverflowButton>
- <xref:System.Windows.Forms.ToolStripItem.Overflow%2A>
- <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A>
- [Visão geral do controle ToolStrip](toolstrip-control-overview-windows-forms.md)
- [Arquitetura de controle do ToolStrip](toolstrip-control-architecture.md)
- [Resumo da tecnologia de ToolStrip](toolstrip-technology-summary.md)
