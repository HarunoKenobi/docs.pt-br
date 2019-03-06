---
title: <udpAnnouncementEndpoint>
ms.date: 03/30/2017
ms.assetid: 5b3fa9c5-f372-4df9-a9d6-1e426063b721
ms.openlocfilehash: 3ffb18fbd410922df4311180ef7af5153ba5c0f5
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57379796"
---
# <a name="udpannouncementendpoint"></a><span data-ttu-id="c2555-101">\<udpAnnouncementEndpoint></span><span class="sxs-lookup"><span data-stu-id="c2555-101">\<udpAnnouncementEndpoint></span></span>
<span data-ttu-id="c2555-102">Este elemento de configuração define um ponto de extremidade padrão que é usado pelos serviços para enviar mensagens de comunicado por uma associação de UDP.</span><span class="sxs-lookup"><span data-stu-id="c2555-102">This configuration element defines a standard endpoint that is used by services to send announcement messages over a UDP binding.</span></span> <span data-ttu-id="c2555-103">Ele tem um contrato fixo e oferece suporte a duas versões de descoberta.</span><span class="sxs-lookup"><span data-stu-id="c2555-103">It has a fixed contract and supports two discovery versions.</span></span> <span data-ttu-id="c2555-104">Além disso, ele tem uma associação de UDP fixa e um valor de endereço padrão, conforme as especificações do WS-Discovery (WS-Discovery de abril de 2005 ou WS-Discovery versão 1.1).</span><span class="sxs-lookup"><span data-stu-id="c2555-104">In addition it has a fixed UDP binding and a default address value as specified in the WS-Discovery specifications (WS-Discovery April 2005 or WS-Discovery version 1.1).</span></span> <span data-ttu-id="c2555-105">Você pode especificar o endereço multicast a ser usado para enviar e receber mensagens de comunicado.</span><span class="sxs-lookup"><span data-stu-id="c2555-105">You can specify the multicast address to use for sending and receiving the announcement messages.</span></span>  
  
<span data-ttu-id="c2555-106">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="c2555-106">\<system.ServiceModel></span></span>  
<span data-ttu-id="c2555-107">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="c2555-107">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c2555-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2555-108">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <announcementEndpoint>
      <standardEndpoint discoveryVersion="WSDiscovery11/WSDiscoveryApril2005"
                        maxAnnouncementDelay="Timespan"
                        multicastAddress="Uri"
                        name="String" />
    </announcementEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c2555-109">Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="c2555-109">Attributes and Elements</span></span>  
 <span data-ttu-id="c2555-110">As seções a seguir descrevem atributos, elementos filho e elementos pai.</span><span class="sxs-lookup"><span data-stu-id="c2555-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c2555-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="c2555-111">Attributes</span></span>  
  
|<span data-ttu-id="c2555-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="c2555-112">Attribute</span></span>|<span data-ttu-id="c2555-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2555-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c2555-114">discoveryVersion</span><span class="sxs-lookup"><span data-stu-id="c2555-114">discoveryVersion</span></span>|<span data-ttu-id="c2555-115">Uma cadeia de caracteres que especifica uma das duas versões do protocolo WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="c2555-115">A string that specifies one of the two versions of WS-Discovery protocol.</span></span> <span data-ttu-id="c2555-116">Os valores válidos são WSDiscovery11 e WSDiscoveryApril2005.</span><span class="sxs-lookup"><span data-stu-id="c2555-116">Valid values are WSDiscovery11 and WSDiscoveryApril2005.</span></span> <span data-ttu-id="c2555-117">Esse valor é do tipo <xref:System.ServiceModel.Discovery.Configuration.AnnouncementEndpointElement.DiscoveryVersion>.</span><span class="sxs-lookup"><span data-stu-id="c2555-117">This value is of type <xref:System.ServiceModel.Discovery.Configuration.AnnouncementEndpointElement.DiscoveryVersion>.</span></span>|  
|<span data-ttu-id="c2555-118">maxAnnouncementDelay</span><span class="sxs-lookup"><span data-stu-id="c2555-118">maxAnnouncementDelay</span></span>|<span data-ttu-id="c2555-119">Um valor de Timespan que especifica o valor máximo para o atraso que o protocolo de descoberta aguardará antes de enviar uma mensagem de saudação.</span><span class="sxs-lookup"><span data-stu-id="c2555-119">A Timespan value that specifies the maximum value for the delay the Discovery protocol will wait before sending a Hello message.</span></span> <span data-ttu-id="c2555-120">As mensagens esperará um valor de tempo aleatório entre 0 e o valor desse atributo antes de serem enviados.</span><span class="sxs-lookup"><span data-stu-id="c2555-120">The messages will wait for a random time value between 0 and the value of this attribute before being sent.</span></span> <span data-ttu-id="c2555-121">Este atributo é usado para definir um atraso de pequeno e aleatório para impedir o excesso de rede quando sai de uma rede e todos os serviços voltam a ficar online ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="c2555-121">This attribute is used to set a small, random delay to prevent network storms when a network goes out and all services come back online at the same time.</span></span>|  
|<span data-ttu-id="c2555-122">multicastAddress</span><span class="sxs-lookup"><span data-stu-id="c2555-122">multicastAddress</span></span>|<span data-ttu-id="c2555-123">Um URI que especifica um endereço de multicast a ser usado para enviar e receber as mensagens de descoberta.</span><span class="sxs-lookup"><span data-stu-id="c2555-123">A URI that specifies a multicast address to use for sending and receiving the discovery messages.</span></span> <span data-ttu-id="c2555-124">O valor padrão é o endereço multicast como em conformidade com a especificação do protocolo.</span><span class="sxs-lookup"><span data-stu-id="c2555-124">The default value is the multicast address as conformant to the protocol specification.</span></span>|  
|<span data-ttu-id="c2555-125">name</span><span class="sxs-lookup"><span data-stu-id="c2555-125">name</span></span>|<span data-ttu-id="c2555-126">Uma cadeia de caracteres que especifica o nome da configuração do ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="c2555-126">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="c2555-127">O nome é usado no `endpointConfiguration` atributo do ponto de extremidade de serviço para vincular a um ponto de extremidade padrão para sua configuração.</span><span class="sxs-lookup"><span data-stu-id="c2555-127">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c2555-128">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c2555-128">Child Elements</span></span>  
  
|<span data-ttu-id="c2555-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="c2555-129">Element</span></span>|<span data-ttu-id="c2555-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2555-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c2555-131">\<udpTransportSettings></span><span class="sxs-lookup"><span data-stu-id="c2555-131">\<udpTransportSettings></span></span>](udptransportsettings.md)|<span data-ttu-id="c2555-132">Uma coleção de configurações que permitem que você configure o transporte UDP para o ponto de extremidade UDP.</span><span class="sxs-lookup"><span data-stu-id="c2555-132">A collection of settings that allow you to configure UDP transport for the UDP endpoint.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c2555-133">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c2555-133">Parent Elements</span></span>  
  
|<span data-ttu-id="c2555-134">Elemento</span><span class="sxs-lookup"><span data-stu-id="c2555-134">Element</span></span>|<span data-ttu-id="c2555-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2555-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c2555-136">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="c2555-136">\<standardEndpoints></span></span>](standardendpoints.md)|<span data-ttu-id="c2555-137">Uma coleção de pontos de extremidade padrão que são definidos previamente os pontos de extremidade com um ou mais das suas propriedades (endereço, associação, contrato) fixo.</span><span class="sxs-lookup"><span data-stu-id="c2555-137">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="c2555-138">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c2555-138">Example</span></span>  
 <span data-ttu-id="c2555-139">O exemplo a seguir demonstra um cliente escuta de comunicado por um UDP padrão de transporte de multicast com o endereço de multicast e UDP multicast transporte com o endereço multicast especificado.</span><span class="sxs-lookup"><span data-stu-id="c2555-139">The following example demonstrates a client listening for announcement over a UDP multicast transport with default multicast address, and UDP multicast transport with specified multicast address.</span></span>  
  
```xml  
<services>
  <service name="ServiceAnnouncementListener">
    <endpoint name="udpAnnouncementEndpointStandard"
              kind="udpAnnouncementEndpoint"
              bindingConfiguration="..." />
    <endpoint name="udpAnnouncementEndpoint2"
              kind="udpAnnouncementEndpoint"
              endpointConfiguration="AnnouncementConfiguration3702"
              bindingConfiguration="..." />
    ...
  </service>
</services>
<standardEndpoints>
  <udpAnnouncementEndpoint>
    <standardEndpoint name="AnnouncementConfiguration2"
                      version="WSDiscoveryApril2005"
                      multicastAddress="soap.udp://239.255.255.250:3703"/>
  </udpAnnouncementEndpoint>
</standardEndpoints>
```  
  
## <a name="see-also"></a><span data-ttu-id="c2555-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c2555-140">See also</span></span>
- <xref:System.ServiceModel.Discovery.UdpAnnouncementEndpoint>