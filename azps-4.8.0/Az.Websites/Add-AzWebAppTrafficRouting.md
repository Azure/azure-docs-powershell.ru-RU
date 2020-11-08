---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236920"
---
# <span data-ttu-id="f091a-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f091a-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="f091a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f091a-102">SYNOPSIS</span></span>
<span data-ttu-id="f091a-103">Добавьте правило маршрутизации в гнездо.</span><span class="sxs-lookup"><span data-stu-id="f091a-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="f091a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f091a-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f091a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f091a-105">DESCRIPTION</span></span>
<span data-ttu-id="f091a-106">Командлет **Add-AzWebAppTrafficRouting** добавляет правило маршрутизации в слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="f091a-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="f091a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f091a-107">EXAMPLES</span></span>

### <span data-ttu-id="f091a-108">Пример 1. Добавьте правило маршрутизации для передачи 15% сетевого трафика в гнездо STG</span><span class="sxs-lookup"><span data-stu-id="f091a-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="f091a-109">Эта команда добавляет правило маршрутизации для передачи 15% рабочего трафика в гнездо STG</span><span class="sxs-lookup"><span data-stu-id="f091a-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="f091a-110">Пример 2. Добавьте правило маршрутизации, чтобы передать производственный трафик в STG диапазоны слотов из 50% в 90% в инкрементном режиме.</span><span class="sxs-lookup"><span data-stu-id="f091a-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="f091a-111">Эта команда добавляет правило маршрутизации, чтобы передать производственный трафик в STG диапазоны слотов из 50% в 90% в инкрементном режиме.</span><span class="sxs-lookup"><span data-stu-id="f091a-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="f091a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f091a-112">PARAMETERS</span></span>

### <span data-ttu-id="f091a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f091a-113">-DefaultProfile</span></span>
<span data-ttu-id="f091a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f091a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f091a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f091a-115">-ResourceGroupName</span></span>
<span data-ttu-id="f091a-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f091a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f091a-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="f091a-117">-RoutingRule</span></span>
<span data-ttu-id="f091a-118">Веб-приложение RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="f091a-118">Web App RoutingRule.</span></span>
<span data-ttu-id="f091a-119">Пример:-RoutingRule @ {ActionHostName = $slot. DefaultHostName ; ReroutePercentage = $ReroutePercentage; Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="f091a-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="f091a-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="f091a-120">-WebAppName</span></span>
<span data-ttu-id="f091a-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="f091a-121">WebApp Name</span></span>

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

### <span data-ttu-id="f091a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f091a-122">-Confirm</span></span>
<span data-ttu-id="f091a-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f091a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f091a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f091a-124">-WhatIf</span></span>
<span data-ttu-id="f091a-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f091a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f091a-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f091a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f091a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f091a-127">CommonParameters</span></span>
<span data-ttu-id="f091a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f091a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f091a-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f091a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f091a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f091a-130">INPUTS</span></span>

### <span data-ttu-id="f091a-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="f091a-131">None</span></span>

## <span data-ttu-id="f091a-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f091a-132">OUTPUTS</span></span>

### <span data-ttu-id="f091a-133">Microsoft. Azure. Management. website. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="f091a-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="f091a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="f091a-134">NOTES</span></span>

## <span data-ttu-id="f091a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f091a-135">RELATED LINKS</span></span>
[<span data-ttu-id="f091a-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f091a-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="f091a-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f091a-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="f091a-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f091a-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)