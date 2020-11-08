---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3e78e302aafb3e59293f04ade7035e5b4ebbd84c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249069"
---
# <span data-ttu-id="f83b2-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="f83b2-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="f83b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f83b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f83b2-103">Обновляет тег для данного кластера.</span><span class="sxs-lookup"><span data-stu-id="f83b2-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="f83b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f83b2-104">SYNTAX</span></span>

### <span data-ttu-id="f83b2-105">ClusterPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f83b2-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f83b2-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f83b2-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f83b2-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f83b2-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f83b2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f83b2-108">DESCRIPTION</span></span>
<span data-ttu-id="f83b2-109">Командлет Set-AzEventHubCluster обновляет теги в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="f83b2-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="f83b2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f83b2-110">EXAMPLES</span></span>

### <span data-ttu-id="f83b2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f83b2-111">Example 1</span></span>
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

<span data-ttu-id="f83b2-112">Обновляет теги данного кластера.</span><span class="sxs-lookup"><span data-stu-id="f83b2-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="f83b2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f83b2-113">PARAMETERS</span></span>

### <span data-ttu-id="f83b2-114">-Capacity</span><span class="sxs-lookup"><span data-stu-id="f83b2-114">-Capacity</span></span>
<span data-ttu-id="f83b2-115">Емкость кластера (SP1), curerntrly, разрешенное значение = 1</span><span class="sxs-lookup"><span data-stu-id="f83b2-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="f83b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f83b2-116">-DefaultProfile</span></span>
<span data-ttu-id="f83b2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f83b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f83b2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f83b2-118">-InputObject</span></span>
<span data-ttu-id="f83b2-119">Имя кластера</span><span class="sxs-lookup"><span data-stu-id="f83b2-119">Cluster Name</span></span>

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

### <span data-ttu-id="f83b2-120">-Location</span><span class="sxs-lookup"><span data-stu-id="f83b2-120">-Location</span></span>
<span data-ttu-id="f83b2-121">Расположение кластера</span><span class="sxs-lookup"><span data-stu-id="f83b2-121">Location of Cluster</span></span>

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

### <span data-ttu-id="f83b2-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f83b2-122">-Name</span></span>
<span data-ttu-id="f83b2-123">Имя кластера</span><span class="sxs-lookup"><span data-stu-id="f83b2-123">Cluster Name</span></span>

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

### <span data-ttu-id="f83b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f83b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="f83b2-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f83b2-125">Resource Group Name</span></span>

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

### <span data-ttu-id="f83b2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f83b2-126">-ResourceId</span></span>
<span data-ttu-id="f83b2-127">Идентификатор ресурса кластера</span><span class="sxs-lookup"><span data-stu-id="f83b2-127">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="f83b2-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="f83b2-128">-Tag</span></span>
<span data-ttu-id="f83b2-129">Хэш-таблицы, представляющие тег ресурсов для кластеров</span><span class="sxs-lookup"><span data-stu-id="f83b2-129">Hashtables which represents resource Tag for Clusters</span></span>

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

### <span data-ttu-id="f83b2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f83b2-130">-Confirm</span></span>
<span data-ttu-id="f83b2-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f83b2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f83b2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f83b2-132">-WhatIf</span></span>
<span data-ttu-id="f83b2-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f83b2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f83b2-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f83b2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f83b2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83b2-135">CommonParameters</span></span>
<span data-ttu-id="f83b2-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f83b2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83b2-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f83b2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83b2-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f83b2-138">INPUTS</span></span>

### <span data-ttu-id="f83b2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f83b2-139">System.String</span></span>

### <span data-ttu-id="f83b2-140">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f83b2-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f83b2-141">Microsoft. Azure. Commands. EventHub. Models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="f83b2-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="f83b2-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f83b2-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f83b2-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f83b2-143">OUTPUTS</span></span>

### <span data-ttu-id="f83b2-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="f83b2-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="f83b2-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f83b2-145">NOTES</span></span>

## <span data-ttu-id="f83b2-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f83b2-146">RELATED LINKS</span></span>
