---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 4a76d54e4c8a3abda87fb9fd6de1d4439b051112
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957128"
---
# <span data-ttu-id="90eb9-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="90eb9-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="90eb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="90eb9-103">Создание нового выделенного кластера естрогов</span><span class="sxs-lookup"><span data-stu-id="90eb9-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="90eb9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="90eb9-104">SYNTAX</span></span>

### <span data-ttu-id="90eb9-105">ClusterPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90eb9-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90eb9-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90eb9-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90eb9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90eb9-107">DESCRIPTION</span></span>
<span data-ttu-id="90eb9-108">С New-AzEventHubCluster создается выделенный кластер естрогов в данной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90eb9-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="90eb9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="90eb9-109">EXAMPLES</span></span>

### <span data-ttu-id="90eb9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="90eb9-110">Example 1</span></span>
```powershell
PS C:\>  New-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Location southcentralus -Capacity 1

Id        : /subscriptions/SubId/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag1, Tag1], [ClusterTag2, Tag2]}

```

<span data-ttu-id="90eb9-111">Создание выделенного кластера "Eventhub-Cluster-5557" в группе ресурсов "RSG-Cluster27651" с группировкой "Южный центр" и "Мощность" в качестве 1</span><span class="sxs-lookup"><span data-stu-id="90eb9-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="90eb9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90eb9-112">PARAMETERS</span></span>

### <span data-ttu-id="90eb9-113">-Capacity</span><span class="sxs-lookup"><span data-stu-id="90eb9-113">-Capacity</span></span>
<span data-ttu-id="90eb9-114">Емкость кластера (CU), толчная, разрешенное значение = 1</span><span class="sxs-lookup"><span data-stu-id="90eb9-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90eb9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90eb9-115">-DefaultProfile</span></span>
<span data-ttu-id="90eb9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90eb9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90eb9-117">-Location</span><span class="sxs-lookup"><span data-stu-id="90eb9-117">-Location</span></span>
<span data-ttu-id="90eb9-118">Расположение кластера</span><span class="sxs-lookup"><span data-stu-id="90eb9-118">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90eb9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="90eb9-119">-Name</span></span>
<span data-ttu-id="90eb9-120">Имя кластера</span><span class="sxs-lookup"><span data-stu-id="90eb9-120">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90eb9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90eb9-121">-ResourceGroupName</span></span>
<span data-ttu-id="90eb9-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="90eb9-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90eb9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90eb9-123">-ResourceId</span></span>
<span data-ttu-id="90eb9-124">ИД ресурса кластера</span><span class="sxs-lookup"><span data-stu-id="90eb9-124">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90eb9-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="90eb9-125">-Tag</span></span>
<span data-ttu-id="90eb9-126">Hashtables which represents resource Tags for Clusters</span><span class="sxs-lookup"><span data-stu-id="90eb9-126">Hashtables which represents resource Tags for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90eb9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90eb9-127">-Confirm</span></span>
<span data-ttu-id="90eb9-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="90eb9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90eb9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90eb9-129">-WhatIf</span></span>
<span data-ttu-id="90eb9-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90eb9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90eb9-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="90eb9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90eb9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90eb9-132">CommonParameters</span></span>
<span data-ttu-id="90eb9-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90eb9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90eb9-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90eb9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90eb9-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90eb9-135">INPUTS</span></span>

### <span data-ttu-id="90eb9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="90eb9-136">System.String</span></span>

### <span data-ttu-id="90eb9-137">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="90eb9-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="90eb9-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="90eb9-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="90eb9-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="90eb9-139">OUTPUTS</span></span>

### <span data-ttu-id="90eb9-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="90eb9-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="90eb9-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="90eb9-141">NOTES</span></span>

## <span data-ttu-id="90eb9-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90eb9-142">RELATED LINKS</span></span>
