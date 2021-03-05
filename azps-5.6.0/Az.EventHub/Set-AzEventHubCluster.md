---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3fb0030d6475ab3fb41f78ab1dc1a54870ed2f8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998329"
---
# <span data-ttu-id="079b1-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="079b1-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="079b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="079b1-102">SYNOPSIS</span></span>
<span data-ttu-id="079b1-103">Обновление тега для заданного кластера.</span><span class="sxs-lookup"><span data-stu-id="079b1-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="079b1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="079b1-104">SYNTAX</span></span>

### <span data-ttu-id="079b1-105">ClusterPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="079b1-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="079b1-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="079b1-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="079b1-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="079b1-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="079b1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="079b1-108">DESCRIPTION</span></span>
<span data-ttu-id="079b1-109">Командлет Set-AzEventHubCluster обновляет теги заданного кластера.</span><span class="sxs-lookup"><span data-stu-id="079b1-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="079b1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="079b1-110">EXAMPLES</span></span>

### <span data-ttu-id="079b1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="079b1-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Tag @{"ClusterTag3" = "Tag3"; "ClusterTag4" = "Tag4";}

Id        : /subscriptions/{SubID}/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag3, Tag3], [ClusterTag4, Tag4]}
```

<span data-ttu-id="079b1-112">Обновляет теги для данного кластера.</span><span class="sxs-lookup"><span data-stu-id="079b1-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="079b1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="079b1-113">PARAMETERS</span></span>

### <span data-ttu-id="079b1-114">-Capacity</span><span class="sxs-lookup"><span data-stu-id="079b1-114">-Capacity</span></span>
<span data-ttu-id="079b1-115">Емкость кластера (CU), толчная, разрешенное значение = 1</span><span class="sxs-lookup"><span data-stu-id="079b1-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="079b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="079b1-116">-DefaultProfile</span></span>
<span data-ttu-id="079b1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="079b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="079b1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="079b1-118">-InputObject</span></span>
<span data-ttu-id="079b1-119">Имя кластера</span><span class="sxs-lookup"><span data-stu-id="079b1-119">Cluster Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="079b1-120">-Location</span><span class="sxs-lookup"><span data-stu-id="079b1-120">-Location</span></span>
<span data-ttu-id="079b1-121">Расположение кластера</span><span class="sxs-lookup"><span data-stu-id="079b1-121">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="079b1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="079b1-122">-Name</span></span>
<span data-ttu-id="079b1-123">Имя кластера</span><span class="sxs-lookup"><span data-stu-id="079b1-123">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="079b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="079b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="079b1-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="079b1-125">Resource Group Name</span></span>

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

### <span data-ttu-id="079b1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="079b1-126">-ResourceId</span></span>
<span data-ttu-id="079b1-127">ИД ресурса кластера</span><span class="sxs-lookup"><span data-stu-id="079b1-127">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="079b1-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="079b1-128">-Tag</span></span>
<span data-ttu-id="079b1-129">Hashtables which represents resource Tag for Clusters</span><span class="sxs-lookup"><span data-stu-id="079b1-129">Hashtables which represents resource Tag for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="079b1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="079b1-130">-Confirm</span></span>
<span data-ttu-id="079b1-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="079b1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="079b1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="079b1-132">-WhatIf</span></span>
<span data-ttu-id="079b1-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="079b1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="079b1-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="079b1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="079b1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="079b1-135">CommonParameters</span></span>
<span data-ttu-id="079b1-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="079b1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="079b1-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="079b1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="079b1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="079b1-138">INPUTS</span></span>

### <span data-ttu-id="079b1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="079b1-139">System.String</span></span>

### <span data-ttu-id="079b1-140">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="079b1-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="079b1-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="079b1-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="079b1-142">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="079b1-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="079b1-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="079b1-143">OUTPUTS</span></span>

### <span data-ttu-id="079b1-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="079b1-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="079b1-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="079b1-145">NOTES</span></span>

## <span data-ttu-id="079b1-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="079b1-146">RELATED LINKS</span></span>
