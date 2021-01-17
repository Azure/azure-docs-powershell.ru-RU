---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413495"
---
# <span data-ttu-id="1648c-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="1648c-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="1648c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1648c-102">SYNOPSIS</span></span>
<span data-ttu-id="1648c-103">кластер обновления</span><span class="sxs-lookup"><span data-stu-id="1648c-103">update cluster</span></span>

## <span data-ttu-id="1648c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1648c-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1648c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1648c-105">DESCRIPTION</span></span>
<span data-ttu-id="1648c-106">кластер обновления</span><span class="sxs-lookup"><span data-stu-id="1648c-106">update cluster</span></span>

## <span data-ttu-id="1648c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1648c-107">EXAMPLES</span></span>

### <span data-ttu-id="1648c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1648c-108">Example 1</span></span>
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

<span data-ttu-id="1648c-109">Обновление кластера с свойствами ключа и SKU</span><span class="sxs-lookup"><span data-stu-id="1648c-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="1648c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1648c-110">PARAMETERS</span></span>

### <span data-ttu-id="1648c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1648c-111">-AsJob</span></span>
<span data-ttu-id="1648c-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1648c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1648c-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1648c-113">-ClusterName</span></span>
<span data-ttu-id="1648c-114">Имя кластера.</span><span class="sxs-lookup"><span data-stu-id="1648c-114">The cluster name.</span></span>

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

### <span data-ttu-id="1648c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1648c-115">-DefaultProfile</span></span>
<span data-ttu-id="1648c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1648c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1648c-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1648c-117">-KeyName</span></span>
<span data-ttu-id="1648c-118">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="1648c-118">Key Name</span></span>

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

### <span data-ttu-id="1648c-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="1648c-119">-KeyVaultUri</span></span>
<span data-ttu-id="1648c-120">Для этого keyvault необходимо включить URI key Vault, "Purge Protection" и "Soft Delete"</span><span class="sxs-lookup"><span data-stu-id="1648c-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

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

### <span data-ttu-id="1648c-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="1648c-121">-KeyVersion</span></span>
<span data-ttu-id="1648c-122">Основная версия</span><span class="sxs-lookup"><span data-stu-id="1648c-122">Key Version</span></span>

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

### <span data-ttu-id="1648c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1648c-123">-ResourceGroupName</span></span>
<span data-ttu-id="1648c-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1648c-124">The resource group name.</span></span>

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

### <span data-ttu-id="1648c-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="1648c-125">-SkuCapacity</span></span>
<span data-ttu-id="1648c-126">Мощность SKU</span><span class="sxs-lookup"><span data-stu-id="1648c-126">Sku Capacity</span></span>

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

### <span data-ttu-id="1648c-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1648c-127">-SkuName</span></span>
<span data-ttu-id="1648c-128">Имя SKU, теперь может быть только "CapacityReservation"</span><span class="sxs-lookup"><span data-stu-id="1648c-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="1648c-129">-Теги</span><span class="sxs-lookup"><span data-stu-id="1648c-129">-Tags</span></span>
<span data-ttu-id="1648c-130">Теги кластера</span><span class="sxs-lookup"><span data-stu-id="1648c-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="1648c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1648c-131">-Confirm</span></span>
<span data-ttu-id="1648c-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1648c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1648c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1648c-133">-WhatIf</span></span>
<span data-ttu-id="1648c-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1648c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1648c-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1648c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1648c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1648c-136">CommonParameters</span></span>
<span data-ttu-id="1648c-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1648c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1648c-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1648c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1648c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1648c-139">INPUTS</span></span>

### <span data-ttu-id="1648c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1648c-140">System.String</span></span>

## <span data-ttu-id="1648c-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1648c-141">OUTPUTS</span></span>

### <span data-ttu-id="1648c-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="1648c-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="1648c-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1648c-143">NOTES</span></span>

## <span data-ttu-id="1648c-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1648c-144">RELATED LINKS</span></span>
