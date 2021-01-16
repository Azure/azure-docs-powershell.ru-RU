---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407303"
---
# <span data-ttu-id="ead7e-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="ead7e-101">New-AzPeeringService</span></span>

## <span data-ttu-id="ead7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ead7e-102">SYNOPSIS</span></span>
<span data-ttu-id="ead7e-103">Создает новую службу пиринга.</span><span class="sxs-lookup"><span data-stu-id="ead7e-103">Creates a new peering service.</span></span>

## <span data-ttu-id="ead7e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ead7e-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ead7e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ead7e-105">DESCRIPTION</span></span>
<span data-ttu-id="ead7e-106">Создает службу пиринга.</span><span class="sxs-lookup"><span data-stu-id="ead7e-106">Creates peering service.</span></span>

## <span data-ttu-id="ead7e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ead7e-107">EXAMPLES</span></span>

### <span data-ttu-id="ead7e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ead7e-108">Example 1</span></span>
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

<span data-ttu-id="ead7e-109">Создание объекта службы пиринга с поставщиком и расположением пиринга.</span><span class="sxs-lookup"><span data-stu-id="ead7e-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="ead7e-110">Используйте в наряду `Get-AzPeeringServiceProvider` с и `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="ead7e-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="ead7e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ead7e-111">PARAMETERS</span></span>

### <span data-ttu-id="ead7e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ead7e-112">-AsJob</span></span>
<span data-ttu-id="ead7e-113">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="ead7e-113">Run in the background.</span></span>

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

### <span data-ttu-id="ead7e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead7e-114">-DefaultProfile</span></span>
<span data-ttu-id="ead7e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ead7e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ead7e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ead7e-116">-Name</span></span>
<span data-ttu-id="ead7e-117">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="ead7e-117">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="ead7e-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="ead7e-118">-PeeringLocation</span></span>
<span data-ttu-id="ead7e-119">Физическое расположение, отличаее от региона Azure.</span><span class="sxs-lookup"><span data-stu-id="ead7e-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="ead7e-120">Использование Get-AzPeeringServiceLocation [-Country <country> ]</span><span class="sxs-lookup"><span data-stu-id="ead7e-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

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

### <span data-ttu-id="ead7e-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="ead7e-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="ead7e-122">Имя поставщика услуг пиринга.</span><span class="sxs-lookup"><span data-stu-id="ead7e-122">The peering service provider name.</span></span>
<span data-ttu-id="ead7e-123">Использование Get-AzPeeringServiceProvider для списка</span><span class="sxs-lookup"><span data-stu-id="ead7e-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

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

### <span data-ttu-id="ead7e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead7e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ead7e-125">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ead7e-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="ead7e-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="ead7e-126">-Tag</span></span>
<span data-ttu-id="ead7e-127">Теги, которые нужно связать со службой Microsoft InputObject.</span><span class="sxs-lookup"><span data-stu-id="ead7e-127">The tags to associate with the Microsoft InputObject Service.</span></span>

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

### <span data-ttu-id="ead7e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ead7e-128">-Confirm</span></span>
<span data-ttu-id="ead7e-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ead7e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead7e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead7e-130">-WhatIf</span></span>
<span data-ttu-id="ead7e-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ead7e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ead7e-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ead7e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead7e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead7e-133">CommonParameters</span></span>
<span data-ttu-id="ead7e-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead7e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead7e-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ead7e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead7e-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ead7e-136">INPUTS</span></span>

### <span data-ttu-id="ead7e-137">Нет</span><span class="sxs-lookup"><span data-stu-id="ead7e-137">None</span></span>

## <span data-ttu-id="ead7e-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ead7e-138">OUTPUTS</span></span>

### <span data-ttu-id="ead7e-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="ead7e-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="ead7e-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ead7e-140">NOTES</span></span>

## <span data-ttu-id="ead7e-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ead7e-141">RELATED LINKS</span></span>