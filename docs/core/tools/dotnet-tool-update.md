---
title: Comando dotnet tool update – CLI do .NET Core
description: O comando dotnet tool update atualiza a Ferramenta Global do .NET Core especificada no computador.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: 35a0bd0f85f0beed06d4250d8f195ce4fe4fcca4
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34696683"
---
# <a name="dotnet-tool-update"></a><span data-ttu-id="151f3-103">dotnet tool update</span><span class="sxs-lookup"><span data-stu-id="151f3-103">dotnet tool update</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="151f3-104">Nome</span><span class="sxs-lookup"><span data-stu-id="151f3-104">Name</span></span>

<span data-ttu-id="151f3-105">`dotnet tool update` – atualiza a [Ferramenta Global do .NET Core](global-tools.md) especificada no computador.</span><span class="sxs-lookup"><span data-stu-id="151f3-105">`dotnet tool update` - Updates the specified [.NET Core Global Tool](global-tools.md) on your machine.</span></span>

## <a name="synopsis"></a><span data-ttu-id="151f3-106">Sinopse</span><span class="sxs-lookup"><span data-stu-id="151f3-106">Synopsis</span></span>

```
dotnet tool update <PACKAGE_NAME> <-g|--global> [--configfile] [--framework] [-v|--verbosity]
dotnet tool update <PACKAGE_NAME> <--tool-path> [--configfile] [--framework] [-v|--verbosity]
dotnet tool update <-h|--help>
```

## <a name="description"></a><span data-ttu-id="151f3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="151f3-107">Description</span></span>

<span data-ttu-id="151f3-108">O comando `dotnet tool update` fornece uma maneira de atualizar as Ferramentas Globais do .NET Core no computador para a última versão estável do pacote.</span><span class="sxs-lookup"><span data-stu-id="151f3-108">The `dotnet tool update` command provides a way for you to update .NET Core Global Tools on your machine to the latest stable version of the package.</span></span> <span data-ttu-id="151f3-109">O comando desinstala e reinstala uma ferramenta, atualizando-a efetivamente.</span><span class="sxs-lookup"><span data-stu-id="151f3-109">The command uninstalls and reinstalls a tool, effectively updating it.</span></span> <span data-ttu-id="151f3-110">Para usar o comando, você precisa especificar que deseja atualizar uma ferramenta de uma instalação de todos os usuários usando a opção `--global` ou especificar um caminho para o local em que a ferramenta está instalada usando a opção `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="151f3-110">To use the command, you either have to specify that you want to update a tool from a user-wide installation using the `--global` option or specify a path to where the tool is installed using the `--tool-path` option.</span></span>

## <a name="arguments"></a><span data-ttu-id="151f3-111">Arguments</span><span class="sxs-lookup"><span data-stu-id="151f3-111">Arguments</span></span>

`PACKAGE_NAME`

<span data-ttu-id="151f3-112">Nome/ID do pacote NuGet que contém a Ferramenta Global do .NET Core a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="151f3-112">Name/ID of the NuGet package that contains the .NET Core Global Tool to update.</span></span> <span data-ttu-id="151f3-113">Encontre o nome do pacote usando o comando [dotnet tool list](dotnet-tool-list.md).</span><span class="sxs-lookup"><span data-stu-id="151f3-113">You can find the package name using the [dotnet tool list](dotnet-tool-list.md) command.</span></span>

## <a name="options"></a><span data-ttu-id="151f3-114">Opções</span><span class="sxs-lookup"><span data-stu-id="151f3-114">Options</span></span>

`--add-source <SOURCE>`

<span data-ttu-id="151f3-115">Adiciona outra origem do pacote NuGet a ser usada durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="151f3-115">Adds an additional NuGet package source to use during installation.</span></span>

`--configfile <FILE>`

<span data-ttu-id="151f3-116">O arquivo de configuração do NuGet (*nuget.config*) a ser usado.</span><span class="sxs-lookup"><span data-stu-id="151f3-116">The NuGet configuration (*nuget.config*) file to use.</span></span>

`--framework <FRAMEWORK>`

<span data-ttu-id="151f3-117">Especifica a [estrutura de destino](../../standard/frameworks.md) para a qual atualizar a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="151f3-117">Specifies the [target framework](../../standard/frameworks.md) to update the tool for.</span></span>

`-g|--global`

<span data-ttu-id="151f3-118">Especifica que a atualização destina-se a uma ferramenta de todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="151f3-118">Specifies that the update is for a user-wide tool.</span></span> <span data-ttu-id="151f3-119">Não pode ser combinada com a opção `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="151f3-119">Can't be combined with the `--tool-path` option.</span></span> <span data-ttu-id="151f3-120">Se você não especificar essa opção, especifique a opção `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="151f3-120">If you don't specify this option, you must specify the `--tool-path` option.</span></span>

`-h|--help`

<span data-ttu-id="151f3-121">Imprime uma ajuda breve para o comando.</span><span class="sxs-lookup"><span data-stu-id="151f3-121">Prints out a short help for the command.</span></span>

`--tool-path <PATH>`

<span data-ttu-id="151f3-122">Especifica o local no qual a Ferramenta Global é instalada.</span><span class="sxs-lookup"><span data-stu-id="151f3-122">Specifies the location where the Global Tool is installed.</span></span> <span data-ttu-id="151f3-123">PATH pode ser absoluto ou relativo.</span><span class="sxs-lookup"><span data-stu-id="151f3-123">PATH can be absolute or relative.</span></span> <span data-ttu-id="151f3-124">Não pode ser combinada com a opção `--global`.</span><span class="sxs-lookup"><span data-stu-id="151f3-124">Can't be combined with the `--global` option.</span></span> <span data-ttu-id="151f3-125">Se você não especificar essa opção, especifique a opção `--global`.</span><span class="sxs-lookup"><span data-stu-id="151f3-125">If you don't specify this option, you must specify the `--global` option.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="151f3-126">Define o nível de detalhes do comando.</span><span class="sxs-lookup"><span data-stu-id="151f3-126">Sets the verbosity level of the command.</span></span> <span data-ttu-id="151f3-127">Os valores permitidos são `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` e `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="151f3-127">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

## <a name="examples"></a><span data-ttu-id="151f3-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="151f3-128">Examples</span></span>

<span data-ttu-id="151f3-129">Atualiza a Ferramenta Global [dotnetsay](https://www.nuget.org/packages/dotnetsay/):</span><span class="sxs-lookup"><span data-stu-id="151f3-129">Updates the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool:</span></span>

`dotnet tool update -g dotnetsay`

<span data-ttu-id="151f3-130">Atualiza a Ferramenta Global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) localizada em uma pasta específica do Windows:</span><span class="sxs-lookup"><span data-stu-id="151f3-130">Updates the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool located on a specific Windows folder:</span></span>

`dotnet tool update dotnetsay --tool-path c:\global-tools`

<span data-ttu-id="151f3-131">Atualiza a Ferramenta Global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) localizada em uma pasta específica do Linux/macOS:</span><span class="sxs-lookup"><span data-stu-id="151f3-131">Updates the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool located on a specific Linux/macOS folder:</span></span>

`dotnet tool update dotnetsay --tool-path ~/bin`

## <a name="see-also"></a><span data-ttu-id="151f3-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="151f3-132">See also</span></span>

[<span data-ttu-id="151f3-133">Ferramentas Globais do .NET Core</span><span class="sxs-lookup"><span data-stu-id="151f3-133">.NET Core Global Tools</span></span>](global-tools.md)