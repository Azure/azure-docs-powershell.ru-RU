---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216585"
---
# <span data-ttu-id="63335-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="63335-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="63335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63335-102">SYNOPSIS</span></span>
<span data-ttu-id="63335-103">Добавьте правило маршрутки в слот.</span><span class="sxs-lookup"><span data-stu-id="63335-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="63335-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="63335-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63335-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63335-105">DESCRIPTION</span></span>
<span data-ttu-id="63335-106">С **помощью cmdlet Add-AzWebAppTrafficRouting** правило маршрутирования добавляется в слот Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="63335-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="63335-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="63335-107">EXAMPLES</span></span>

### <span data-ttu-id="63335-108">Пример 1. Добавление правила маршрутки для передачи 15 % производственного трафика в слот Stg</span><span class="sxs-lookup"><span data-stu-id="63335-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="63335-109">Эта команда добавляет правило маршрутки для передачи 15 % производственного трафика в слот Stg</span><span class="sxs-lookup"><span data-stu-id="63335-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="63335-110">Пример 2. Добавьте правило маршрутки для передачи производственного трафика в диапазоны от 50% до 90 % добавочно.</span><span class="sxs-lookup"><span data-stu-id="63335-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="63335-111">Эта команда добавляет правило маршрутки для передачи производственного трафика в диапазоны от 50% до 90 % добавочно.</span><span class="sxs-lookup"><span data-stu-id="63335-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="63335-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63335-112">PARAMETERS</span></span>

### <span data-ttu-id="63335-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63335-113">-DefaultProfile</span></span>
<span data-ttu-id="63335-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63335-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63335-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63335-115">-ResourceGroupName</span></span>
<span data-ttu-id="63335-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="63335-116">Resource Group Name</span></span>

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

### <span data-ttu-id="63335-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="63335-117">-RoutingRule</span></span>
<span data-ttu-id="63335-118">Web App RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="63335-118">Web App RoutingRule.</span></span>
<span data-ttu-id="63335-119">Пример: -RoutingRule @{ActionHostName=$slot. DefaultHostName ; ReroutePercentage=$ReroutePercentage; Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="63335-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="63335-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="63335-120">-WebAppName</span></span>
<span data-ttu-id="63335-121">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="63335-121">WebApp Name</span></span>

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

### <span data-ttu-id="63335-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63335-122">-Confirm</span></span>
<span data-ttu-id="63335-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63335-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63335-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63335-124">-WhatIf</span></span>
<span data-ttu-id="63335-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63335-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63335-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="63335-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63335-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63335-127">CommonParameters</span></span>
<span data-ttu-id="63335-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63335-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63335-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63335-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63335-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63335-130">INPUTS</span></span>

### <span data-ttu-id="63335-131">Нет</span><span class="sxs-lookup"><span data-stu-id="63335-131">None</span></span>

## <span data-ttu-id="63335-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="63335-132">OUTPUTS</span></span>

### <span data-ttu-id="63335-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="63335-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="63335-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="63335-134">NOTES</span></span>

## <span data-ttu-id="63335-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63335-135">RELATED LINKS</span></span>
[<span data-ttu-id="63335-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="63335-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="63335-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="63335-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="63335-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="63335-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
