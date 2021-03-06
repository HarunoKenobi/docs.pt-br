---
title: Pintando com imagens, desenhos e visuais
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- brushes [WPF], painting with drawings
- painting [WPF], with drawings
- painting [WPF], with images
- painting with visuals [WPF]
- brushes [WPF], painting with images
- brushes [WPF], painting with visuals
ms.assetid: 779aac3f-8d41-49d8-8130-768244aa2240
ms.openlocfilehash: 304499a6d6dd9d9f5fd51fc84044de5e50393762
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64584741"
---
# <a name="painting-with-images-drawings-and-visuals"></a>Pintando com imagens, desenhos e visuais
Este tópico descreve como usar <xref:System.Windows.Media.ImageBrush>, <xref:System.Windows.Media.DrawingBrush>, e <xref:System.Windows.Media.VisualBrush> objetos para pintar uma área com uma imagem, um <xref:System.Windows.Media.Drawing>, ou um <xref:System.Windows.Media.Visual>.  

<a name="prereqs"></a>   
## <a name="prerequisites"></a>Pré-requisitos  
 Para entender esse tópico, você deve estar familiarizado com os diferentes tipos de pincéis que [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] fornece e seus recursos básicos. Para uma introdução, consulte a [Visão geral de pincéis do WPF](wpf-brushes-overview.md).  
  
<a name="image"></a>   
## <a name="paint-an-area-with-an-image"></a>Pintar uma área com uma imagem  
 Uma <xref:System.Windows.Media.ImageBrush> pinta uma área com um <xref:System.Windows.Media.ImageSource>. O tipo mais comum de <xref:System.Windows.Media.ImageSource> a ser usado com um <xref:System.Windows.Media.ImageBrush> é um <xref:System.Windows.Media.Imaging.BitmapImage>, que descreve um gráfico de bitmap. Você pode usar um <xref:System.Windows.Media.DrawingImage> pintar usando um <xref:System.Windows.Media.Drawing> objeto, mas é mais simples de usar um <xref:System.Windows.Media.DrawingBrush> em vez disso. Para obter mais informações sobre <xref:System.Windows.Media.ImageSource> objetos, consulte a [visão geral de imagens](imaging-overview.md).  
  
 Para pintar com um <xref:System.Windows.Media.ImageBrush>, crie um <xref:System.Windows.Media.Imaging.BitmapImage> e usá-lo para carregar o conteúdo do bitmap. Em seguida, use o <xref:System.Windows.Media.Imaging.BitmapImage> para definir o <xref:System.Windows.Media.ImageBrush.ImageSource%2A> propriedade do <xref:System.Windows.Media.ImageBrush>. Por fim, aplique o <xref:System.Windows.Media.ImageBrush> para o objeto que deseja pintar.  Na [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], você também pode definir o <xref:System.Windows.Media.ImageBrush.ImageSource%2A> propriedade do <xref:System.Windows.Media.ImageBrush> com o caminho da imagem para carregar.  
  
 Assim como todos os <xref:System.Windows.Media.Brush> objetos, um <xref:System.Windows.Media.ImageBrush> pode ser usado para pintar objetos, como formas, painéis, controles e texto. A ilustração a seguir mostra alguns efeitos que podem ser obtidos com um <xref:System.Windows.Media.ImageBrush>.  
  
 ![Exemplos de saída de ImageBrush](./media/wcpsdk-mmgraphics-imagebrushexamples.gif "wcpsdk_mmgraphics_imagebrushexamples")  
Objetos pintados por um ImageBrush  
  
 Por padrão, um <xref:System.Windows.Media.ImageBrush> alonga sua imagem para preencher completamente a área que está sendo pintada, possivelmente distorcendo a imagem se a área pintada tiver uma taxa de proporção diferente do que a imagem. Você pode alterar esse comportamento alterando a <xref:System.Windows.Media.TileBrush.Stretch%2A> propriedade do valor padrão de <xref:System.Windows.Media.Stretch.Fill> à <xref:System.Windows.Media.Stretch.None>, <xref:System.Windows.Media.Stretch.Uniform>, ou <xref:System.Windows.Media.Stretch.UniformToFill>. Porque <xref:System.Windows.Media.ImageBrush> é um tipo de <xref:System.Windows.Media.TileBrush>, você pode especificar exatamente como um pincel de imagem preenche a área de saída e até mesmo cria padrões. Para obter mais informações sobre o advanced <xref:System.Windows.Media.TileBrush> recursos, consulte a [visão geral de TileBrush](tilebrush-overview.md).  
  
<a name="fillingpanelwithimage"></a>   
## <a name="example-paint-an-object-with-a-bitmap-image"></a>Exemplo: Pintar um objeto com uma imagem de Bitmap  
 O exemplo a seguir usa uma <xref:System.Windows.Media.ImageBrush> para pintar o <xref:System.Windows.Controls.Panel.Background%2A> de um <xref:System.Windows.Controls.Canvas>.  
  
 [!code-xaml[BrushOverviewExamples_snip#GraphicsMMImageBrushAsCanvasBackgroundExampleWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/ImageBrushExample.xaml#graphicsmmimagebrushascanvasbackgroundexamplewholepage)]  
  
 [!code-csharp[BrushOverviewExamples_procedural_snip#GraphicsMMImageBrushAsCanvasBackgroundExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/CSharp/ImageBrushExample.cs#graphicsmmimagebrushascanvasbackgroundexamplewholepage)]
 [!code-vb[BrushOverviewExamples_procedural_snip#GraphicsMMImageBrushAsCanvasBackgroundExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/visualbasic/imagebrushexample.vb#graphicsmmimagebrushascanvasbackgroundexamplewholepage)]  
  
<a name="drawingbrushintro"></a>   
## <a name="paint-an-area-with-a-drawing"></a>Pintar uma área com um desenho  
 Um <xref:System.Windows.Media.DrawingBrush> lhe permite pintar uma área com formas, texto, imagens e vídeo. As formas dentro de um pincel de desenho podem ser próprios pintadas com uma cor sólida, gradiente, imagem ou até mesmo outro <xref:System.Windows.Media.DrawingBrush>. A ilustração a seguir demonstra alguns usos de um <xref:System.Windows.Media.DrawingBrush>.  
  
 ![Exemplos de saída de DrawingBrush](./media/wcpsdk-mmgraphics-drawingbrushexamples.png "wcpsdk_mmgraphics_drawingbrushexamples")  
Objetos pintados por um DrawingBrush  
  
 Um <xref:System.Windows.Media.DrawingBrush> pinta uma área com um <xref:System.Windows.Media.Drawing> objeto. Um <xref:System.Windows.Media.Drawing> objeto descreve o conteúdo visível, como uma forma, bitmap, vídeo ou uma linha de texto. Diferentes tipos de desenhos descrevem diferentes tipos de conteúdo. A seguir está uma lista dos diferentes tipos de objetos de desenho.  
  
- <xref:System.Windows.Media.GeometryDrawing> – Desenha uma forma.  
  
- <xref:System.Windows.Media.ImageDrawing> – Desenha uma imagem.  
  
- <xref:System.Windows.Media.GlyphRunDrawing> – Desenha texto.  
  
- <xref:System.Windows.Media.VideoDrawing> – Reproduz um arquivo de áudio ou vídeo.  
  
- <xref:System.Windows.Media.DrawingGroup> – Desenha outros desenhos. Use um grupo de desenhos para combinar outros desenhos em um único desenho composto.  
  
 Para obter mais informações sobre <xref:System.Windows.Media.Drawing> objetos, consulte a [visão geral de objetos de desenho](drawing-objects-overview.md).  
  
 Como uma <xref:System.Windows.Media.ImageBrush>, um <xref:System.Windows.Media.DrawingBrush> alonga seu <xref:System.Windows.Media.DrawingBrush.Drawing%2A> para preencher sua área de saída. Você pode substituir esse comportamento alterando a <xref:System.Windows.Media.TileBrush.Stretch%2A> propriedade da sua configuração padrão de <xref:System.Windows.Media.Stretch.Fill>. Para obter mais informações, consulte a propriedade <xref:System.Windows.Media.TileBrush.Stretch%2A>.  
  
<a name="fillingareawithdrawingbrushexample"></a>   
## <a name="example-paint-an-object-with-a-drawing"></a>Exemplo: Pintar um objeto com um desenho  
 O exemplo a seguir mostra como pintar um objeto com um desenho de três elipses. Um <xref:System.Windows.Media.GeometryDrawing> é usado para descrever as elipses.  
  
 [!code-xaml[BrushOverviewExamples_snip#GraphicsMMDrawingBrushAsButtonBackgroundExample](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/DrawingBrushExample.xaml#graphicsmmdrawingbrushasbuttonbackgroundexample)]  
  
 [!code-csharp[BrushOverviewExamples_procedural_snip#GraphicsMMDrawingBrushAsButtonBackgroundExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/CSharp/DrawingBrushExample.cs#graphicsmmdrawingbrushasbuttonbackgroundexample1)]
 [!code-vb[BrushOverviewExamples_procedural_snip#GraphicsMMDrawingBrushAsButtonBackgroundExample1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/visualbasic/drawingbrushexample.vb#graphicsmmdrawingbrushasbuttonbackgroundexample1)]  
  
<a name="visualbrushsection"></a>   
## <a name="paint-an-area-with-a-visual"></a>Pintar uma área com um visual  
 O mais versátil e eficiente de todos os pincéis, o <xref:System.Windows.Media.VisualBrush> pinta uma área com um <xref:System.Windows.Media.Visual>. Um <xref:System.Windows.Media.Visual> é um tipo de gráfico de baixo nível que serve como o predecessor de vários componentes gráficos úteis. Por exemplo, o <xref:System.Windows.Window>, <xref:System.Windows.FrameworkElement>, e <xref:System.Windows.Controls.Control> classes são todos os tipos de <xref:System.Windows.Media.Visual> objetos. Usando um <xref:System.Windows.Media.VisualBrush>, você pode pintar áreas com praticamente qualquer [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] objeto gráfico.  
  
> [!NOTE]
>  Embora <xref:System.Windows.Media.VisualBrush> é um tipo de <xref:System.Windows.Freezable> do objeto, ele não pode ser congelado (somente leitura) quando seu <xref:System.Windows.Media.VisualBrush.Visual%2A> propriedade é definida como um valor diferente de `null`.  
  
 Há duas maneiras para especificar o <xref:System.Windows.Media.VisualBrush.Visual%2A> conteúdo de um <xref:System.Windows.Media.VisualBrush>.  
  
- Criar um novo <xref:System.Windows.Media.Visual> e usá-lo para definir o <xref:System.Windows.Media.VisualBrush.Visual%2A> propriedade do <xref:System.Windows.Media.VisualBrush>. Por exemplo, consulte o [exemplo: Pintar um objeto com um Visual](#examplevisualbrush1) seção a seguir.  
  
- Usar existente <xref:System.Windows.Media.Visual>, que cria uma imagem duplicada do destino <xref:System.Windows.Media.Visual>. Você pode usar o <xref:System.Windows.Media.VisualBrush> para criar efeitos interessantes, como reflexão e ampliação. Por exemplo, consulte o [exemplo: Criar um reflexo](#examplevisualbrush2) seção.  
  
 Quando você define uma nova <xref:System.Windows.Media.VisualBrush.Visual%2A> para um <xref:System.Windows.Media.VisualBrush> e que <xref:System.Windows.Media.Visual> é uma <xref:System.Windows.UIElement> (por exemplo, um painel ou controle), o sistema de layout é executado no <xref:System.Windows.UIElement> e seus elementos filho quando o <xref:System.Windows.Media.VisualBrush.AutoLayoutContent%2A> propriedade é definida como `true`. No entanto, a raiz <xref:System.Windows.UIElement> é essencialmente isolado do restante do sistema: estilos e layout externo não podem permear esse limite. Portanto, você deve especificar explicitamente o tamanho da raiz <xref:System.Windows.UIElement>, porque seu único pai é o <xref:System.Windows.Media.VisualBrush> e, portanto, ele não é possível dimensionar automaticamente para a área que está sendo pintada. Para mais informações sobre o layout em [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)], consulte [Layout](../advanced/layout.md).  
  
 Como o <xref:System.Windows.Media.ImageBrush> e <xref:System.Windows.Media.DrawingBrush>, um <xref:System.Windows.Media.VisualBrush> alonga seu conteúdo para preencher sua área de saída. Você pode substituir esse comportamento alterando a <xref:System.Windows.Media.TileBrush.Stretch%2A> propriedade da sua configuração padrão de <xref:System.Windows.Media.Stretch.Fill>. Para obter mais informações, consulte a propriedade <xref:System.Windows.Media.TileBrush.Stretch%2A>.  
  
<a name="examplevisualbrush1"></a>   
## <a name="example-paint-an-object-with-a-visual"></a>Exemplo: Pintar um objeto com um Visual  
 No exemplo a seguir, vários controles e um painel são usados para pintar um retângulo.  
  
 [!code-xaml[BrushOverviewExamples_snip#GraphicsMMVisualBrushAsRectangleBackgroundExample](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/VisualBrushExample.xaml#graphicsmmvisualbrushasrectanglebackgroundexample)]  
  
 [!code-csharp[BrushOverviewExamples_procedural_snip#GraphicsMMVisualBrushAsRectangleBackgroundExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/CSharp/VisualBrushExample.cs#graphicsmmvisualbrushasrectanglebackgroundexample1)]
 [!code-vb[BrushOverviewExamples_procedural_snip#GraphicsMMVisualBrushAsRectangleBackgroundExample1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_procedural_snip/visualbasic/visualbrushexample.vb#graphicsmmvisualbrushasrectanglebackgroundexample1)]  
  
<a name="examplevisualbrush2"></a>   
## <a name="example-create-a-reflection"></a>Exemplo: Criar uma reflexão  
 O exemplo anterior mostrou como criar um novo <xref:System.Windows.Media.Visual> para uso como um plano de fundo. Você também pode usar um <xref:System.Windows.Media.VisualBrush> para exibir um visual existente; essa funcionalidade permite que você produza efeitos visuais interessantes, como reflexões e ampliações. O exemplo a seguir usa uma <xref:System.Windows.Media.VisualBrush> para criar um reflexo de um <xref:System.Windows.Controls.Border> que contém vários elementos. A ilustração a seguir mostra a saída que esse exemplo produz.  
  
 ![Um objeto Visual de refletidas](./media/graphicsmm-visualbrush-reflection-small.jpg "graphicsmm_visualbrush_reflection_small")  
Um objeto visual refletido  
  
 [!code-csharp[visualbrush_markup_snip#GraphicsMMVisualBrushReflectionExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/visualbrush_markup_snip/CSharp/ReflectionExample.cs#graphicsmmvisualbrushreflectionexamplewholepage)]
 [!code-vb[visualbrush_markup_snip#GraphicsMMVisualBrushReflectionExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/visualbrush_markup_snip/visualbasic/reflectionexample.vb#graphicsmmvisualbrushreflectionexamplewholepage)]
 [!code-xaml[visualbrush_markup_snip#GraphicsMMVisualBrushReflectionExampleWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/visualbrush_markup_snip/XAML/ReflectionExample.xaml#graphicsmmvisualbrushreflectionexamplewholepage)]  
  
 Para outros exemplos que mostram como ampliar partes da tela e como criar reflexões, consulte o [Exemplo do VisualBrush](https://go.microsoft.com/fwlink/?LinkID=160049).  
  
<a name="tilebrush"></a>   
## <a name="tilebrush-features"></a>Recursos do TileBrush  
 <xref:System.Windows.Media.ImageBrush>, <xref:System.Windows.Media.DrawingBrush>, e <xref:System.Windows.Media.VisualBrush> são tipos de <xref:System.Windows.Media.TileBrush> objetos. <xref:System.Windows.Media.TileBrush> objetos oferecem uma grande quantidade de controle sobre como uma área é pintada com uma imagem, desenho ou visual. Por exemplo, em vez de apenas pintar uma área com uma única imagem alongada, você pode pintá-la com uma série de blocos de imagens que criam um padrão.  
  
 Um <xref:System.Windows.Media.TileBrush> tem três componentes principais: conteúdo, blocos e a área de saída.  
  
 ![Componentes de TileBrush](./media/wcpsdk-mmgraphics-defaultcontentprojection2.png "wcpsdk_mmgraphics_defaultcontentprojection2")  
Componentes de um TileBrush com um único bloco  
  
 ![Componentes de um TileBrush lado a lado](./media/graphicsmm-tiledprojection.png "graphicsmm_tiledprojection")  
Componentes de um TileBrush com vários blocos  
  
 Para obter mais informações sobre os recursos lado a lado do <xref:System.Windows.Media.TileBrush> objetos, consulte a [visão geral de TileBrush](tilebrush-overview.md).  
  
## <a name="see-also"></a>Consulte também

- <xref:System.Windows.Media.ImageBrush>
- <xref:System.Windows.Media.DrawingBrush>
- <xref:System.Windows.Media.VisualBrush>
- <xref:System.Windows.Media.TileBrush>
- [Visão geral de TileBrush](tilebrush-overview.md)
- [Visão geral de pincéis do WPF](wpf-brushes-overview.md)
- [Visão geral da geração de imagens](imaging-overview.md)
- [Visão geral dos objetos de desenho](drawing-objects-overview.md)
- [Visão geral de máscaras da opacidade](opacity-masks-overview.md)
- [Visão geral de renderização de gráficos do WPF](wpf-graphics-rendering-overview.md)
- [Exemplo de ImageBrush](https://go.microsoft.com/fwlink/?LinkID=160005)
- [Exemplo de VisualBrush](https://go.microsoft.com/fwlink/?LinkID=160049)
