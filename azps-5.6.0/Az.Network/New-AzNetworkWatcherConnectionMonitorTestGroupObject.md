---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: 4ab9feb0d99bc808cfabb481baf81bb12e050f28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958408"
---
# <span data-ttu-id="5d52e-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="5d52e-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="5d52e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d52e-102">SYNOPSIS</span></span>
<span data-ttu-id="5d52e-103">Создайте группу тестирования монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="5d52e-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="5d52e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5d52e-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d52e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d52e-105">DESCRIPTION</span></span>
<span data-ttu-id="5d52e-106">С New-AzNetworkWatcherConnectionMonitorTestGroupObject создается группа для проверки подключения.</span><span class="sxs-lookup"><span data-stu-id="5d52e-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="5d52e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5d52e-107">EXAMPLES</span></span>

### <span data-ttu-id="5d52e-108">Пример 1. Создание тестовой группы с 2 testConfigurations, w source и 2 конечными точками</span><span class="sxs-lookup"><span data-stu-id="5d52e-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="5d52e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d52e-109">PARAMETERS</span></span>

### <span data-ttu-id="5d52e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d52e-110">-DefaultProfile</span></span>
<span data-ttu-id="5d52e-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d52e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d52e-112">-Destination</span><span class="sxs-lookup"><span data-stu-id="5d52e-112">-Destination</span></span>
<span data-ttu-id="5d52e-113">Список конечных точек назначения.</span><span class="sxs-lookup"><span data-stu-id="5d52e-113">List of destination endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d52e-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="5d52e-114">-Disable</span></span>
<span data-ttu-id="5d52e-115">Флаг, указывающий, отключена ли тестовая группа.</span><span class="sxs-lookup"><span data-stu-id="5d52e-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="5d52e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5d52e-116">-Name</span></span>
<span data-ttu-id="5d52e-117">Имя тестовой группы.</span><span class="sxs-lookup"><span data-stu-id="5d52e-117">The test group name.</span></span>

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

### <span data-ttu-id="5d52e-118">-Source</span><span class="sxs-lookup"><span data-stu-id="5d52e-118">-Source</span></span>
<span data-ttu-id="5d52e-119">Список исходных конечных точек.</span><span class="sxs-lookup"><span data-stu-id="5d52e-119">List of source endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d52e-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d52e-120">-TestConfiguration</span></span>
<span data-ttu-id="5d52e-121">Список тестовой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5d52e-121">List of test configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d52e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d52e-122">-Confirm</span></span>
<span data-ttu-id="5d52e-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d52e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d52e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d52e-124">-WhatIf</span></span>
<span data-ttu-id="5d52e-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d52e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d52e-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5d52e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d52e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d52e-127">CommonParameters</span></span>
<span data-ttu-id="5d52e-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d52e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d52e-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d52e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d52e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d52e-130">INPUTS</span></span>

### <span data-ttu-id="5d52e-131">Нет</span><span class="sxs-lookup"><span data-stu-id="5d52e-131">None</span></span>

## <span data-ttu-id="5d52e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5d52e-132">OUTPUTS</span></span>

### <span data-ttu-id="5d52e-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="5d52e-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="5d52e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5d52e-134">NOTES</span></span>

## <span data-ttu-id="5d52e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d52e-135">RELATED LINKS</span></span>
