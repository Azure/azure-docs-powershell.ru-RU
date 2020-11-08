---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236708"
---
# <span data-ttu-id="5215b-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="5215b-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="5215b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5215b-102">SYNOPSIS</span></span>
<span data-ttu-id="5215b-103">Создание нового выделенного кластера eventhub</span><span class="sxs-lookup"><span data-stu-id="5215b-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="5215b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5215b-104">SYNTAX</span></span>

### <span data-ttu-id="5215b-105">ClusterPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5215b-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5215b-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5215b-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5215b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5215b-107">DESCRIPTION</span></span>
<span data-ttu-id="5215b-108">Командлет New-AzEventHubCluster создает выделенный кластер eventhub в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5215b-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="5215b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5215b-109">EXAMPLES</span></span>

### <span data-ttu-id="5215b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5215b-110">Example 1</span></span>
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

<span data-ttu-id="5215b-111">Создает выделенный кластер Eventhub-Cluster-5557 в группе resourcegroup "RSG-Cluster27651" с расположением southcentralus и емкостью как 1</span><span class="sxs-lookup"><span data-stu-id="5215b-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="5215b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5215b-112">PARAMETERS</span></span>

### <span data-ttu-id="5215b-113">-Capacity</span><span class="sxs-lookup"><span data-stu-id="5215b-113">-Capacity</span></span>
<span data-ttu-id="5215b-114">Емкость кластера (SP1), curerntrly, разрешенное значение = 1</span><span class="sxs-lookup"><span data-stu-id="5215b-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="5215b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5215b-115">-DefaultProfile</span></span>
<span data-ttu-id="5215b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5215b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5215b-117">-Location</span><span class="sxs-lookup"><span data-stu-id="5215b-117">-Location</span></span>
<span data-ttu-id="5215b-118">Расположение кластера</span><span class="sxs-lookup"><span data-stu-id="5215b-118">Location of Cluster</span></span>

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

### <span data-ttu-id="5215b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5215b-119">-Name</span></span>
<span data-ttu-id="5215b-120">Имя кластера</span><span class="sxs-lookup"><span data-stu-id="5215b-120">Cluster Name</span></span>

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

### <span data-ttu-id="5215b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5215b-121">-ResourceGroupName</span></span>
<span data-ttu-id="5215b-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5215b-122">Resource Group Name</span></span>

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

### <span data-ttu-id="5215b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5215b-123">-ResourceId</span></span>
<span data-ttu-id="5215b-124">Идентификатор ресурса кластера</span><span class="sxs-lookup"><span data-stu-id="5215b-124">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="5215b-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="5215b-125">-Tag</span></span>
<span data-ttu-id="5215b-126">Хэш-таблицы, представляющие Теги ресурсов для кластеров</span><span class="sxs-lookup"><span data-stu-id="5215b-126">Hashtables which represents resource Tags for Clusters</span></span>

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

### <span data-ttu-id="5215b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5215b-127">-Confirm</span></span>
<span data-ttu-id="5215b-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5215b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5215b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5215b-129">-WhatIf</span></span>
<span data-ttu-id="5215b-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5215b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5215b-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5215b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5215b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5215b-132">CommonParameters</span></span>
<span data-ttu-id="5215b-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5215b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5215b-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5215b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5215b-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5215b-135">INPUTS</span></span>

### <span data-ttu-id="5215b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5215b-136">System.String</span></span>

### <span data-ttu-id="5215b-137">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5215b-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="5215b-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5215b-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5215b-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5215b-139">OUTPUTS</span></span>

### <span data-ttu-id="5215b-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="5215b-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="5215b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="5215b-141">NOTES</span></span>

## <span data-ttu-id="5215b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5215b-142">RELATED LINKS</span></span>
