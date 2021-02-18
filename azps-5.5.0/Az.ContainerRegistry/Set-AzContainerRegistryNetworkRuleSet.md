---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: 4a2292b0b573a5357466f3b240ba3b6df7cf0a1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215521"
---
# <span data-ttu-id="21a9d-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="21a9d-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="21a9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="21a9d-103">Создание или обновление набора правил сети.</span><span class="sxs-lookup"><span data-stu-id="21a9d-103">Create or update a network rule set.</span></span> <span data-ttu-id="21a9d-104">Набор правил можно применять только к реестру Premium.</span><span class="sxs-lookup"><span data-stu-id="21a9d-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="21a9d-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="21a9d-105">SYNTAX</span></span>

### <span data-ttu-id="21a9d-106">AddAddNetworkRuleWithoutInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21a9d-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21a9d-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="21a9d-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21a9d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21a9d-108">DESCRIPTION</span></span>
<span data-ttu-id="21a9d-109">Создание и обновление набора правил сети</span><span class="sxs-lookup"><span data-stu-id="21a9d-109">Create or update a network rule set</span></span>

## <span data-ttu-id="21a9d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="21a9d-110">EXAMPLES</span></span>

### <span data-ttu-id="21a9d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="21a9d-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="21a9d-112">Создайте новый набор правил сети.</span><span class="sxs-lookup"><span data-stu-id="21a9d-112">Create a new network rule set.</span></span>

## <span data-ttu-id="21a9d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21a9d-113">PARAMETERS</span></span>

### <span data-ttu-id="21a9d-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="21a9d-114">-DefaultAction</span></span>
<span data-ttu-id="21a9d-115">Действие по умолчанию может иметь значение "Разрешить" или "Запретить".</span><span class="sxs-lookup"><span data-stu-id="21a9d-115">Default action, could be 'Allow' or 'Deny'</span></span>

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

### <span data-ttu-id="21a9d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a9d-116">-DefaultProfile</span></span>
<span data-ttu-id="21a9d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21a9d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21a9d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21a9d-118">-InputObject</span></span>
<span data-ttu-id="21a9d-119">Input PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="21a9d-119">Input PSNetworkRuleSet</span></span>

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

### <span data-ttu-id="21a9d-120">-NetworkRule</span><span class="sxs-lookup"><span data-stu-id="21a9d-120">-NetworkRule</span></span>
<span data-ttu-id="21a9d-121">Список правил сети</span><span class="sxs-lookup"><span data-stu-id="21a9d-121">List of Network rules</span></span>

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

### <span data-ttu-id="21a9d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a9d-122">CommonParameters</span></span>
<span data-ttu-id="21a9d-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a9d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a9d-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21a9d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a9d-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21a9d-125">INPUTS</span></span>

### <span data-ttu-id="21a9d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="21a9d-126">System.String</span></span>

### <span data-ttu-id="21a9d-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="21a9d-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="21a9d-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="21a9d-128">OUTPUTS</span></span>

### <span data-ttu-id="21a9d-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="21a9d-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="21a9d-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="21a9d-130">NOTES</span></span>

## <span data-ttu-id="21a9d-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21a9d-131">RELATED LINKS</span></span>
