---
title: 'Como: Ancorar controles nos Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- Anchor property [Windows Forms], enabling resizable forms
- Windows Forms controls, screen resolutions
- resizing forms [Windows Forms]
- Windows Forms controls, size
- screen resolution and control display
- controls [Windows Forms], anchoring
- forms [Windows Forms], resizing
- Windows Forms, resizing
- controls [Windows Forms], positioning
ms.assetid: 59ea914f-fbd3-427a-80fe-decd02f7ae6d
ms.openlocfilehash: b48761bda2baad4f7d1e6db9b41d73d6d54bc081
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211268"
---
# <a name="how-to-anchor-controls-on-windows-forms"></a>Como: Ancorar controles nos Windows Forms

Se você estiver criando um formulário que o usuário pode redimensionar em tempo de execução, os controles do formulário devem redimensionar e reposicionar corretamente. Para redimensionar controles dinamicamente com o formulário, você pode usar o <xref:System.Windows.Forms.Control.Anchor%2A> propriedade dos controles dos Windows Forms. O <xref:System.Windows.Forms.Control.Anchor%2A> propriedade define uma posição de âncora para o controle. Quando um controle é ancorado a um formulário e esse formulário é redimensionado, o controle mantém a distância entre o controle e as posições de âncora. Por exemplo, se você tiver um <xref:System.Windows.Forms.TextBox> controle é ancorado a esquerda, direita e bordas na parte inferior do formulário, como o formulário é redimensionado, o <xref:System.Windows.Forms.TextBox> controle é redimensionado horizontalmente, de modo que ele mantém a mesma distância dos lados direito e esquerdos do formulário. Além disso, o controle se posiciona verticalmente para que sua localização seja sempre a mesma distância da borda inferior do formulário. Se um controle não estiver ancorado e o formulário for redimensionado, a posição do controle em relação às bordas do formulário será alterada.

O <xref:System.Windows.Forms.Control.Anchor%2A> propriedade interage com o <xref:System.Windows.Forms.Control.AutoSize%2A> propriedade. Para obter mais informações, consulte [Visão Geral da Propriedade AutoSize](autosize-property-overview.md).

## <a name="anchor-a-control-on-a-form"></a>Ancorar um controle em um formulário

1. No Visual Studio, selecione o controle que você deseja ancorar.

    > [!NOTE]
    > É possível ancorar vários controles simultaneamente pressionando a tecla CTRL, clicando em cada controle para selecioná-lo e, em seguida, seguindo o resto desse procedimento.

2. No **propriedades** janela, clique na seta à direita do <xref:System.Windows.Forms.Control.Anchor%2A> propriedade.

     Um editor será exibido e mostra uma cruz.

3. Para definir uma âncora, clique na seção superior, esquerda, direita ou inferior da cruz.

     Os controles estão ancorados na parte superior e esquerda por padrão.

4. Para limpar um lado do controle que foi ancorado, clique nessa parte da cruz.

5. Para fechar o <xref:System.Windows.Forms.Control.Anchor%2A> editor de propriedades, clique no <xref:System.Windows.Forms.Control.Anchor%2A> novamente o nome da propriedade.

Quando o formulário é exibido em tempo de execução, o controle é redimensionado para permanecer posicionado na mesma distância da borda do formulário. A distância da borda ancorada sempre é a mesma distância definida quando o controle é posicionado no Designer de Formulários do Windows.

> [!NOTE]
> Alguns controles, como o <xref:System.Windows.Forms.ComboBox> , têm um limite de altura. Ancorar o controle na parte inferior do formulário ou contêiner não pode forçar o controle a exceder o limite de altura.

Controles herdados devem ser `Protected` para serem ancorados. Para alterar o nível de acesso de um controle, defina sua propriedade `Modifiers` na janela **Propriedades**.

## <a name="see-also"></a>Consulte também

- [Controles dos Windows Forms](index.md)
- [Organizando Controles nos Windows Forms](arranging-controls-on-windows-forms.md)
- [Visão geral da propriedade AutoSize](autosize-property-overview.md)
- [Como: Encaixar controles nos Windows Forms](how-to-dock-controls-on-windows-forms.md)
- [Passo a passo: Organizando controles nos Windows Forms utilizando um FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)
- [Passo a passo: Organizando controles nos Windows Forms utilizando um TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [Passo a passo: Definindo o layout dos Windows Forms controles com preenchimento, margens e a propriedade AutoSize](windows-forms-controls-padding-autosize.md)
