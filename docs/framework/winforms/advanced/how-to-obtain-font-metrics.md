---
title: 'Como: obter métricas de fontes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- fonts [Windows Forms], obtaining metrics
- font metrics [Windows Forms], obtaining
ms.assetid: ff7c0616-67f7-4fa2-84ee-b8d642f2b09b
ms.openlocfilehash: 75177b609f14d335aa57aba77d647827f50a8692
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65881846"
---
# <a name="how-to-obtain-font-metrics"></a>Como: obter métricas de fontes
O <xref:System.Drawing.FontFamily> classe fornece os seguintes métodos que recuperam várias métricas de uma combinação de estilo/família específica:  
  
- <xref:System.Drawing.FontFamily.GetEmHeight%2A>(FontStyle)  
  
- <xref:System.Drawing.FontFamily.GetCellAscent%2A>(FontStyle)  
  
- <xref:System.Drawing.FontFamily.GetCellDescent%2A>(FontStyle)  
  
- <xref:System.Drawing.FontFamily.GetLineSpacing%2A>(FontStyle)  
  
 Os números retornados por esses métodos são em unidades de design de fonte, portanto, eles são independentes do tamanho e das unidades de um determinado <xref:System.Drawing.Font> objeto.  
  
 A ilustração a seguir mostra várias métricas:
  
 ![Ilustração de métricas de fonte: ascendente e descendente espaçamento entre linhas.](./media/how-to-obtain-font-metrics/various-font-metrics.png)  
  
## <a name="example"></a>Exemplo  
 O exemplo a seguir exibe as métricas para o estilo normal da família de fontes Arial. O código também cria uma <xref:System.Drawing.Font> objeto (com base na família Arial) com 16 pixels de tamanho e exibe as métricas (em pixels) para esse determinado <xref:System.Drawing.Font> objeto.  
  
 A ilustração a seguir mostra a saída do exemplo de código:
  
 ![Saída do código de exemplo de métricas de fonte Arial.](./media/how-to-obtain-font-metrics/example-output-code-arial-font.png)  
  
 Observe as duas primeiras linhas de saída na ilustração anterior. O <xref:System.Drawing.Font> objeto retorna um tamanho de 16 e o <xref:System.Drawing.FontFamily> object retorna uma altura de 2.048. Esses dois números (16 e 2.048) são a chave para a conversão entre unidades de design de fonte e as unidades (em pixels nesse caso) do <xref:System.Drawing.Font> objeto.  
  
 Por exemplo, você pode converter o ascendente de unidades de design em pixels da seguinte maneira:  
  
 ![Fórmula mostrando a conversão de unidades de design em pixels](./media/how-to-obtain-font-metrics/convert-font-units-example.png)  
  
 O código a seguir posiciona o texto verticalmente, definindo o <xref:System.Drawing.PointF.Y%2A> membro de dados de um <xref:System.Drawing.PointF> objeto. A coordenada y é aumentada em `font.Height` para cada nova linha de texto. O <xref:System.Drawing.Font.Height%2A> propriedade de um <xref:System.Drawing.Font> object retorna o espaçamento entre linhas (em pixels) para esse determinado <xref:System.Drawing.Font> objeto. Neste exemplo, o número retornado por <xref:System.Drawing.Font.Height%2A> é 19. Observe que esse é o mesmo número (arredondado para um número inteiro) obtido ao converter a métrica de espaçamento entre linhas em pixels.  
  
 Observe que a altura em (também chamada de tamanho ou tamanho em) não é a soma do ascendente e do descendente. A soma do ascendente e do descendente é chamada a altura da célula. A altura da célula menos o entrelinhamento interno é igual à altura em. A altura da célula mais o entrelinhamento externo é igual ao espaçamento entre linhas.  
  
 [!code-csharp[System.Drawing.FontsAndText#71](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#71)]
 [!code-vb[System.Drawing.FontsAndText#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#71)]  
  
## <a name="compiling-the-code"></a>Compilando o código  
 O exemplo anterior foi projetado para uso com o Windows Forms e requer <xref:System.Windows.Forms.PaintEventArgs> `e`, que é um parâmetro de <xref:System.Windows.Forms.PaintEventHandler>.  
  
## <a name="see-also"></a>Consulte também

- [Elementos Gráficos e Desenho nos Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Usando fontes e texto](using-fonts-and-text.md)
