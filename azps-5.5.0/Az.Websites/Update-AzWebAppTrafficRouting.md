---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241493"
---
# <span data-ttu-id="100de-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="100de-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="100de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="100de-102">SYNOPSIS</span></span>
<span data-ttu-id="100de-103">Обновив правило маршрутки до слота.</span><span class="sxs-lookup"><span data-stu-id="100de-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="100de-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="100de-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="100de-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="100de-105">DESCRIPTION</span></span>
<span data-ttu-id="100de-106">С помощью cmdlet **Update-AzWebAppTrafficRouting** можно обновить конфигурацию правила маршрутирования для слота Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="100de-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="100de-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="100de-107">EXAMPLES</span></span>

### <span data-ttu-id="100de-108">Пример 1: обновление правила маршрутки для переноса 15 % производственного трафика в слот Stg</span><span class="sxs-lookup"><span data-stu-id="100de-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="100de-109">Эта команда обновляет правило маршрутки, чтобы перенести 15 % производственного трафика в слот Stg.</span><span class="sxs-lookup"><span data-stu-id="100de-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="100de-110">Пример 2: обновление правила маршрутки для передачи производственного трафика в диапазоны от 50% до 90 % добавочно.</span><span class="sxs-lookup"><span data-stu-id="100de-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="100de-111">Эта команда обновляет правило маршрутки, чтобы переносить производственный трафик в диапазоны от 50% до 90 % добавочно.</span><span class="sxs-lookup"><span data-stu-id="100de-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="100de-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="100de-112">PARAMETERS</span></span>

### <span data-ttu-id="100de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="100de-113">-DefaultProfile</span></span>
<span data-ttu-id="100de-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="100de-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="100de-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="100de-115">-ResourceGroupName</span></span>
<span data-ttu-id="100de-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="100de-116">ResourceGroupName</span></span>
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

### <span data-ttu-id="100de-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="100de-117">-RoutingRule</span></span>
<span data-ttu-id="100de-118">Web App RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="100de-118">Web App RoutingRule.</span></span>
<span data-ttu-id="100de-119">Пример: -RoutingRule @{ActionHostName=$slot. DefaultHostName ; ReroutePercentage=$ReroutePercentage; Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="100de-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="100de-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="100de-120">-WebAppName</span></span>
<span data-ttu-id="100de-121">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="100de-121">WebApp Name</span></span>

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

### <span data-ttu-id="100de-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="100de-122">-Confirm</span></span>
<span data-ttu-id="100de-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="100de-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="100de-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="100de-124">-WhatIf</span></span>
<span data-ttu-id="100de-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="100de-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="100de-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="100de-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="100de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="100de-127">CommonParameters</span></span>
<span data-ttu-id="100de-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="100de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="100de-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="100de-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="100de-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="100de-130">INPUTS</span></span>

### <span data-ttu-id="100de-131">Нет</span><span class="sxs-lookup"><span data-stu-id="100de-131">None</span></span>

## <span data-ttu-id="100de-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="100de-132">OUTPUTS</span></span>

### <span data-ttu-id="100de-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="100de-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="100de-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="100de-134">NOTES</span></span>

## <span data-ttu-id="100de-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="100de-135">RELATED LINKS</span></span>

[<span data-ttu-id="100de-136">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="100de-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="100de-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="100de-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="100de-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="100de-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)