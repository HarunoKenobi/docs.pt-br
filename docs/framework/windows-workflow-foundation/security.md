---
title: Segurança
ms.date: 03/30/2017
ms.assetid: 737ec121-bfc5-4b75-a504-2d53c2c8af39
ms.openlocfilehash: d82ad52dd24dbfcb66887693563b08c995baa63a
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64619488"
---
# <a name="security"></a>Segurança
A instância Store de fluxo de trabalho do SQL usa as seguintes funções de segurança de base de dados para proteger o acesso a informações do estado da instância na base de dados de persistência.  
  
- **System.Activities.DurableInstancing.InstanceStoreUsers**. Essa função tem acesso de leitura e gravação para a exibição e a direita públicas de execução procedimentos armazenados que estão envolvidos na criação, em carregar e salvar em instâncias.  
  
- **System.Activities.DurableInstancing.InstanceStoreObservers**. Essa função tem acesso somente leitura modos de exibição públicas.  
  
- **System.Activities.DurableInstancing.WorkflowActivationUsers**. Essa função tem direitos de execução procedimentos armazenados que estão envolvidos no processo de ativação da instância. Para obter mais informações sobre a ativação de instância, consulte [ativação de instância](instance-activation.md). A conta de usuário em que um host genérico (como o serviço de gerenciamento de fluxo de trabalho [!INCLUDE[dublin](../../../includes/dublin-md.md)]) executa deve ser adicionada à essa função de base de dados.  
  
 Para obter mais informações sobre a segurança para armazenamentos de persistência com tela de aplicativo do Windows Server, consulte [configuração de segurança para armazenamentos de persistência na tela do aplicativo](https://go.microsoft.com/fwlink/?LinkId=201208)  
  
> [!CAUTION]
>  Um cliente que tenha acesso a seus próprios dados de instância no armazenamento de instância tem acesso a todas as outras instâncias no mesmo armazenamento de instância. O armazenamento de instância não suporta especificar permissões de segurança no nível da instância. Você deve criar armazenamentos separados de instância e mapear grupos/usuários diferentes para ter acesso aos armazenamentos diferentes.
