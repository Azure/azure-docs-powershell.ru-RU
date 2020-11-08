---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078796"
---
# <span data-ttu-id="24b96-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="24b96-101">New-AzPeeringService</span></span>

## <span data-ttu-id="24b96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24b96-102">SYNOPSIS</span></span>
<span data-ttu-id="24b96-103">Создание новой службы пиринга.</span><span class="sxs-lookup"><span data-stu-id="24b96-103">Creates a new peering service.</span></span>

## <span data-ttu-id="24b96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24b96-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24b96-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24b96-105">DESCRIPTION</span></span>
<span data-ttu-id="24b96-106">Создает службу пиринга.</span><span class="sxs-lookup"><span data-stu-id="24b96-106">Creates peering service.</span></span>

## <span data-ttu-id="24b96-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24b96-107">EXAMPLES</span></span>

### <span data-ttu-id="24b96-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="24b96-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="24b96-109">Создает объект службы пиринга с расположением поставщика и пиринга.</span><span class="sxs-lookup"><span data-stu-id="24b96-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="24b96-110">Использование в conjuction с `Get-AzPeeringServiceProvider` и `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="24b96-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="24b96-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24b96-111">PARAMETERS</span></span>

### <span data-ttu-id="24b96-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24b96-112">-AsJob</span></span>
<span data-ttu-id="24b96-113">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="24b96-113">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b96-114">-DefaultProfile</span></span>
<span data-ttu-id="24b96-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24b96-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24b96-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="24b96-116">-Name</span></span>
<span data-ttu-id="24b96-117">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="24b96-117">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b96-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="24b96-118">-PeeringLocation</span></span>
<span data-ttu-id="24b96-119">Физическое расположение отличается от региона Azure.</span><span class="sxs-lookup"><span data-stu-id="24b96-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="24b96-120">Использование Get-AzPeeringServiceLocation [-Country <country> ]</span><span class="sxs-lookup"><span data-stu-id="24b96-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b96-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="24b96-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="24b96-122">Имя поставщика услуг пиринга.</span><span class="sxs-lookup"><span data-stu-id="24b96-122">The peering service provider name.</span></span>
<span data-ttu-id="24b96-123">Использование Get-AzPeeringServiceProvider командлета для списка</span><span class="sxs-lookup"><span data-stu-id="24b96-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b96-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b96-124">-ResourceGroupName</span></span>
<span data-ttu-id="24b96-125">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="24b96-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b96-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="24b96-126">-Tag</span></span>
<span data-ttu-id="24b96-127">Теги, связываемые со службой Microsoft InputObject.</span><span class="sxs-lookup"><span data-stu-id="24b96-127">The tags to associate with the Microsoft InputObject Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b96-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24b96-128">-Confirm</span></span>
<span data-ttu-id="24b96-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="24b96-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b96-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24b96-130">-WhatIf</span></span>
<span data-ttu-id="24b96-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="24b96-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24b96-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24b96-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b96-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b96-133">CommonParameters</span></span>
<span data-ttu-id="24b96-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24b96-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b96-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24b96-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b96-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24b96-136">INPUTS</span></span>

### <span data-ttu-id="24b96-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="24b96-137">None</span></span>

## <span data-ttu-id="24b96-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24b96-138">OUTPUTS</span></span>

### <span data-ttu-id="24b96-139">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringService)</span><span class="sxs-lookup"><span data-stu-id="24b96-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="24b96-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="24b96-140">NOTES</span></span>

## <span data-ttu-id="24b96-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24b96-141">RELATED LINKS</span></span>