---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: 4a2292b0b573a5357466f3b240ba3b6df7cf0a1e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245578"
---
# <span data-ttu-id="bc5a3-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="bc5a3-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="bc5a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc5a3-102">SYNOPSIS</span></span>
<span data-ttu-id="bc5a3-103">Создание или обновление множества сетевых правил.</span><span class="sxs-lookup"><span data-stu-id="bc5a3-103">Create or update a network rule set.</span></span> <span data-ttu-id="bc5a3-104">Наборы правил можно применять только к реестру Premium.</span><span class="sxs-lookup"><span data-stu-id="bc5a3-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="bc5a3-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc5a3-105">SYNTAX</span></span>

### <span data-ttu-id="bc5a3-106">AddAddNetworkRuleWithoutInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bc5a3-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc5a3-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="bc5a3-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc5a3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc5a3-108">DESCRIPTION</span></span>
<span data-ttu-id="bc5a3-109">Создание или обновление множества сетевых правил</span><span class="sxs-lookup"><span data-stu-id="bc5a3-109">Create or update a network rule set</span></span>

## <span data-ttu-id="bc5a3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc5a3-110">EXAMPLES</span></span>

### <span data-ttu-id="bc5a3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc5a3-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="bc5a3-112">Создание нового комплекта сетевых правил.</span><span class="sxs-lookup"><span data-stu-id="bc5a3-112">Create a new network rule set.</span></span>

## <span data-ttu-id="bc5a3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc5a3-113">PARAMETERS</span></span>

### <span data-ttu-id="bc5a3-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="bc5a3-114">-DefaultAction</span></span>
<span data-ttu-id="bc5a3-115">Действие по умолчанию — "разрешить" или "запретить"</span><span class="sxs-lookup"><span data-stu-id="bc5a3-115">Default action, could be 'Allow' or 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: AddAddNetworkRuleWithoutInputObject
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc5a3-116">-DefaultProfile</span></span>
<span data-ttu-id="bc5a3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc5a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5a3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc5a3-118">-InputObject</span></span>
<span data-ttu-id="bc5a3-119">Ввод PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="bc5a3-119">Input PSNetworkRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5a3-120">-NetworkRule</span><span class="sxs-lookup"><span data-stu-id="bc5a3-120">-NetworkRule</span></span>
<span data-ttu-id="bc5a3-121">Список сетевых правил</span><span class="sxs-lookup"><span data-stu-id="bc5a3-121">List of Network rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc5a3-122">CommonParameters</span></span>
<span data-ttu-id="bc5a3-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc5a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc5a3-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc5a3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc5a3-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc5a3-125">INPUTS</span></span>

### <span data-ttu-id="bc5a3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bc5a3-126">System.String</span></span>

### <span data-ttu-id="bc5a3-127">Microsoft. Azure. Commands. ContainerRegistry. Models. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bc5a3-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="bc5a3-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc5a3-128">OUTPUTS</span></span>

### <span data-ttu-id="bc5a3-129">Microsoft. Azure. Commands. ContainerRegistry. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="bc5a3-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="bc5a3-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc5a3-130">NOTES</span></span>

## <span data-ttu-id="bc5a3-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc5a3-131">RELATED LINKS</span></span>
