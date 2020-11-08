---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066254"
---
# <span data-ttu-id="50d83-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="50d83-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="50d83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50d83-102">SYNOPSIS</span></span>
<span data-ttu-id="50d83-103">Создание тестовой группы монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="50d83-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="50d83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50d83-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50d83-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50d83-105">DESCRIPTION</span></span>
<span data-ttu-id="50d83-106">Командлет New-AzNetworkWatcherConnectionMonitorTestGroupObject создает тестовую группу монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="50d83-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="50d83-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50d83-107">EXAMPLES</span></span>

### <span data-ttu-id="50d83-108">Пример 1: создание тестовой группы с 2 testConfigurations, w Source and 2 конечными точками</span><span class="sxs-lookup"><span data-stu-id="50d83-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="50d83-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50d83-109">PARAMETERS</span></span>

### <span data-ttu-id="50d83-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d83-110">-DefaultProfile</span></span>
<span data-ttu-id="50d83-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50d83-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50d83-112">-Destination</span><span class="sxs-lookup"><span data-stu-id="50d83-112">-Destination</span></span>
<span data-ttu-id="50d83-113">Список конечных точек назначения.</span><span class="sxs-lookup"><span data-stu-id="50d83-113">List of destination endpoints.</span></span>

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

### <span data-ttu-id="50d83-114">-Отключение</span><span class="sxs-lookup"><span data-stu-id="50d83-114">-Disable</span></span>
<span data-ttu-id="50d83-115">Флаг, указывающий на то, что группа тестов отключена.</span><span class="sxs-lookup"><span data-stu-id="50d83-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="50d83-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="50d83-116">-Name</span></span>
<span data-ttu-id="50d83-117">Имя тестовой группы.</span><span class="sxs-lookup"><span data-stu-id="50d83-117">The test group name.</span></span>

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

### <span data-ttu-id="50d83-118">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="50d83-118">-Source</span></span>
<span data-ttu-id="50d83-119">Список конечных точек источника.</span><span class="sxs-lookup"><span data-stu-id="50d83-119">List of source endpoints.</span></span>

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

### <span data-ttu-id="50d83-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="50d83-120">-TestConfiguration</span></span>
<span data-ttu-id="50d83-121">Список конфигураций теста.</span><span class="sxs-lookup"><span data-stu-id="50d83-121">List of test configuration.</span></span>

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

### <span data-ttu-id="50d83-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50d83-122">-Confirm</span></span>
<span data-ttu-id="50d83-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="50d83-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50d83-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50d83-124">-WhatIf</span></span>
<span data-ttu-id="50d83-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="50d83-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50d83-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="50d83-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50d83-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d83-127">CommonParameters</span></span>
<span data-ttu-id="50d83-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50d83-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d83-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50d83-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d83-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50d83-130">INPUTS</span></span>

### <span data-ttu-id="50d83-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="50d83-131">None</span></span>

## <span data-ttu-id="50d83-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50d83-132">OUTPUTS</span></span>

### <span data-ttu-id="50d83-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="50d83-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="50d83-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="50d83-134">NOTES</span></span>

## <span data-ttu-id="50d83-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50d83-135">RELATED LINKS</span></span>
