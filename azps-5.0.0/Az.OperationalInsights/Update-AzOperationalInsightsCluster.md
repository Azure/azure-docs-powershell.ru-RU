---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247571"
---
# <span data-ttu-id="b4bb7-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="b4bb7-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="b4bb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bb7-103">обновить кластер</span><span class="sxs-lookup"><span data-stu-id="b4bb7-103">update cluster</span></span>

## <span data-ttu-id="b4bb7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4bb7-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4bb7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4bb7-105">DESCRIPTION</span></span>
<span data-ttu-id="b4bb7-106">обновить кластер</span><span class="sxs-lookup"><span data-stu-id="b4bb7-106">update cluster</span></span>

## <span data-ttu-id="b4bb7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4bb7-107">EXAMPLES</span></span>

### <span data-ttu-id="b4bb7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4bb7-108">Example 1</span></span>
```powershell
Update-AzOperationalInsightsCluster -ResourceGroupName azps-test-group -ClusterName yabo-cluster10 -Location eastus -SkuName CapacityReservation -SkuCapacity 1200 -KeyVaultUri {uri} -KeyName {key-name} -KeyVersion {version}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Updating
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="b4bb7-109">Обновление кластера с помощью свойств и конфигурации хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="b4bb7-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="b4bb7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4bb7-110">PARAMETERS</span></span>

### <span data-ttu-id="b4bb7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4bb7-111">-AsJob</span></span>
<span data-ttu-id="b4bb7-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b4bb7-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bb7-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="b4bb7-113">-ClusterName</span></span>
<span data-ttu-id="b4bb7-114">Имя кластера.</span><span class="sxs-lookup"><span data-stu-id="b4bb7-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bb7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4bb7-115">-DefaultProfile</span></span>
<span data-ttu-id="b4bb7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4bb7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bb7-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b4bb7-117">-KeyName</span></span>
<span data-ttu-id="b4bb7-118">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="b4bb7-118">Key Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bb7-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="b4bb7-119">-KeyVaultUri</span></span>
<span data-ttu-id="b4bb7-120">Универсальный код ресурса (URI) для хранилища ключей, "очистить защиту" и "обратимое удаление", должны быть включены для этого keyvault</span><span class="sxs-lookup"><span data-stu-id="b4bb7-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bb7-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="b4bb7-121">-KeyVersion</span></span>
<span data-ttu-id="b4bb7-122">Версия ключа</span><span class="sxs-lookup"><span data-stu-id="b4bb7-122">Key Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bb7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4bb7-123">-ResourceGroupName</span></span>
<span data-ttu-id="b4bb7-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4bb7-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bb7-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b4bb7-125">-SkuCapacity</span></span>
<span data-ttu-id="b4bb7-126">SKU Capacity</span><span class="sxs-lookup"><span data-stu-id="b4bb7-126">Sku Capacity</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bb7-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b4bb7-127">-SkuName</span></span>
<span data-ttu-id="b4bb7-128">Имя SKU, теперь может быть только "CapacityReservation"</span><span class="sxs-lookup"><span data-stu-id="b4bb7-128">Sku Name, now can be 'CapacityReservation' only</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CapacityReservation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bb7-129">-Теги</span><span class="sxs-lookup"><span data-stu-id="b4bb7-129">-Tags</span></span>
<span data-ttu-id="b4bb7-130">Теги кластера</span><span class="sxs-lookup"><span data-stu-id="b4bb7-130">Tags of the cluster</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bb7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4bb7-131">-Confirm</span></span>
<span data-ttu-id="b4bb7-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4bb7-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bb7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4bb7-133">-WhatIf</span></span>
<span data-ttu-id="b4bb7-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4bb7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4bb7-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4bb7-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bb7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bb7-136">CommonParameters</span></span>
<span data-ttu-id="b4bb7-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4bb7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bb7-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4bb7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bb7-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4bb7-139">INPUTS</span></span>

### <span data-ttu-id="b4bb7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b4bb7-140">System.String</span></span>

## <span data-ttu-id="b4bb7-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4bb7-141">OUTPUTS</span></span>

### <span data-ttu-id="b4bb7-142">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="b4bb7-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="b4bb7-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4bb7-143">NOTES</span></span>

## <span data-ttu-id="b4bb7-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4bb7-144">RELATED LINKS</span></span>
