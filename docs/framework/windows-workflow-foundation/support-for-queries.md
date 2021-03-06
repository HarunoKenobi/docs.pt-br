---
title: Suporte para consultas
ms.date: 03/30/2017
ms.assetid: 093c22f5-3294-4642-857a-5252233d6796
ms.openlocfilehash: db3580d0a29353aac027bddd8f040d3085d674af
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64665296"
---
# <a name="support-for-queries"></a>Suporte para consultas
A instância Store de fluxo de trabalho do SQL registra um conjunto de propriedades conhecidos no armazenamento. Os usuários podem ver para as instâncias com base nessas propriedades. A lista a seguir contém algumas dessas propriedades conhecidas:  
  
- **Nome do site.** Nome do site que contém o serviço.  
  
- **Caminho relativo do aplicativo.** Caminho do aplicativo relativa ao site.  
  
- **Caminho relativo de serviço.** Caminho do serviço relativo para o aplicativo.  
  
- **Nome do serviço.** Nome do serviço.  
  
- **Namespace de serviço.** Nome do namespace que usa o serviço.  
  
- **Computador atual.**  
  
- **Máquina de última**. O computador no qual a instância do serviço de fluxo de trabalho executou a última vez.  
  
> [!NOTE]
>  Para cenários são hospedados usando o host de Serviço de Fluxo de Trabalho, somente as quatro propriedades mais recentes são preenchidas. Para cenários de aplicativo de fluxo de trabalho, apenas a propriedade a última é preenchida.  
  
 O tempo de execução de fluxo de trabalho fornece valores para as primeiras três propriedades. O host de serviço de fluxo de trabalho fornece o valor para o **motivo da suspensão** propriedade. A Store de instância de fluxo de trabalho do SQL em si fornece valores para o **computador atualizado último** propriedade.  
  
 O recurso de Store de instância de fluxo de trabalho do SQL também permite que você especifique as propriedades personalizadas que você deseja armazenar os valores na base de dados de persistência e que você deseja usar em consultas. Para obter mais informações sobre as promoções personalizados, consulte [extensibilidade de Store](store-extensibility.md).  
  
## <a name="views"></a>Exibições  
 O armazenamento de instância contém as seguintes modos de exibição. Ver [esquema de banco de dados de persistência](persistence-database-schema.md) para obter mais detalhes.  
  
### <a name="the-instances-view"></a>O modo de instâncias  
 O modo de instâncias contém os campos seguintes:  
  
1. **ID**  
  
2. **PendingTimer**  
  
3. **CreationTime**  
  
4. **LastUpdatedTime**  
  
5. **ServiceDeploymentId**  
  
6. **SuspensionExceptionName**  
  
7. **SuspensionReason**  
  
8. **ActiveBookmarks**  
  
9. **CurrentMachine**  
  
10. **LastMachine**  
  
11. **ExecutionStatus**  
  
12. **IsInitialized**  
  
13. **IsSuspended**  
  
14. **IsCompleted**  
  
15. **EncodingOption**  
  
16. **ReadWritePrimitiveDataProperties**  
  
17. **WriteOnlyPrimitiveDataProperties**  
  
18. **ReadWriteComplexDataProperties**  
  
19. **WriteOnlyComplexDataProperties**  
  
### <a name="the-servicedeployments-view"></a>O modo de ServiceDeployments  
 O modo de ServiceDeployments contém os campos seguintes:  
  
1. **SiteName**  
  
2. **RelativeServicePath**  
  
3. **RelativeApplicationPath**  
  
4. **ServiceName**  
  
5. **ServiceNamespace**  
  
### <a name="the-instancepromotedproperties-view"></a>O modo de InstancePromotedProperties  
 O modo de InstancePromotedProperties contém os seguintes campos. Para obter detalhes sobre propriedades elevadas, consulte o [extensibilidade de Store](store-extensibility.md) tópico.  
  
1. **InstanceId**  
  
2. **EncodingOption**  
  
3. **PromotionName**  
  
4. **Valor #** (um intervalo de campos da **Value1** à **Value64**).
