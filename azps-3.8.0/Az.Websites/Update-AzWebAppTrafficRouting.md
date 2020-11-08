---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072588"
---
# <span data-ttu-id="ad775-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="ad775-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="ad775-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad775-102">SYNOPSIS</span></span>
<span data-ttu-id="ad775-103">Обновите правило маршрутизации до ячейки.</span><span class="sxs-lookup"><span data-stu-id="ad775-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="ad775-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad775-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad775-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad775-105">DESCRIPTION</span></span>
<span data-ttu-id="ad775-106">Командлет **Update-AzWebAppTrafficRouting** обновляет конфигурацию правила маршрутизации для области веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="ad775-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="ad775-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad775-107">EXAMPLES</span></span>

### <span data-ttu-id="ad775-108">Пример 1. Обновите правило маршрутизации, чтобы передать 15% рабочего трафика в гнездо STG</span><span class="sxs-lookup"><span data-stu-id="ad775-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="ad775-109">Эта команда обновляет правило маршрутизации для передачи 15% сетевого трафика в Stgный слот.</span><span class="sxs-lookup"><span data-stu-id="ad775-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="ad775-110">Пример 2. Обновите правило маршрутизации, чтобы передать производственный трафик в STG диапазоны слотов из 50% в 90% в инкрементном режиме.</span><span class="sxs-lookup"><span data-stu-id="ad775-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="ad775-111">Эта команда обновляет правило маршрутизации, чтобы передать производственный трафик в STG диапазоны слотов от 50% до 90% в инкрементном режиме.</span><span class="sxs-lookup"><span data-stu-id="ad775-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="ad775-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad775-112">PARAMETERS</span></span>

### <span data-ttu-id="ad775-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad775-113">-DefaultProfile</span></span>
<span data-ttu-id="ad775-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad775-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad775-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad775-115">-ResourceGroupName</span></span>
<span data-ttu-id="ad775-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad775-116">ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad775-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="ad775-117">-RoutingRule</span></span>
<span data-ttu-id="ad775-118">Веб-приложение RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="ad775-118">Web App RoutingRule.</span></span>
<span data-ttu-id="ad775-119">Пример:-RoutingRule @ {ActionHostName = $slot. DefaultHostName ; ReroutePercentage = $ReroutePercentage; Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="ad775-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad775-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="ad775-120">-WebAppName</span></span>
<span data-ttu-id="ad775-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="ad775-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad775-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad775-122">-Confirm</span></span>
<span data-ttu-id="ad775-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad775-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad775-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad775-124">-WhatIf</span></span>
<span data-ttu-id="ad775-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad775-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad775-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad775-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad775-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad775-127">CommonParameters</span></span>
<span data-ttu-id="ad775-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad775-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad775-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad775-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad775-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad775-130">INPUTS</span></span>

### <span data-ttu-id="ad775-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="ad775-131">None</span></span>

## <span data-ttu-id="ad775-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad775-132">OUTPUTS</span></span>

### <span data-ttu-id="ad775-133">Microsoft. Azure. Management. website. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="ad775-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="ad775-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad775-134">NOTES</span></span>

## <span data-ttu-id="ad775-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad775-135">RELATED LINKS</span></span>

[<span data-ttu-id="ad775-136">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="ad775-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="ad775-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="ad775-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="ad775-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="ad775-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)