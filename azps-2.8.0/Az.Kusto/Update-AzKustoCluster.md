---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 890ec07cecd46badaccc1c2140290fd8042d319b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720566"
---
# <span data-ttu-id="d20c2-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d20c2-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="d20c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d20c2-102">SYNOPSIS</span></span>
<span data-ttu-id="d20c2-103">Обновите существующий кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="d20c2-103">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="d20c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d20c2-104">SYNTAX</span></span>

### <span data-ttu-id="d20c2-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d20c2-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>] [-Capacity <Int32>]
 [-Tier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d20c2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d20c2-106">ByResourceId</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d20c2-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d20c2-107">ByInputObject</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-InputObject] <PSKustoCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d20c2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d20c2-108">DESCRIPTION</span></span>
<span data-ttu-id="d20c2-109">Обновите существующий кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="d20c2-109">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="d20c2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d20c2-110">EXAMPLES</span></span>

### <span data-ttu-id="d20c2-111">Пример 1. Обновите существующий кластер по имени</span><span class="sxs-lookup"><span data-stu-id="d20c2-111">Example 1 - Update an existing cluster by name</span></span>

```
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Sku D14_v2

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Sku               : D14_v2
Capacity          : 5
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="d20c2-112">Приведенная выше команда обновляет уровень кластера Kusto "mykustocluster", который находится в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="d20c2-112">The above command updates the tier of the Kusto cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="d20c2-113">Пример 2: обновление существующего кластера с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="d20c2-113">Example 2 - Update an existing cluster by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Update-AzKustoCluster -Sku D14_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D14_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="d20c2-114">В приведенной выше команде получается кластер Kusto "mykustocluster", обнаруженный в группе ресурсов "testrg", с помощью `Get-AzKustoCluster` командлета, а затем передается результат, чтобы `Update-AzKustoCluster` обновить уровень кластера на "Standard".</span><span class="sxs-lookup"><span data-stu-id="d20c2-114">The above command gets the Kusto cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Update-AzKustoCluster` to update the cluster's tier to "standard".</span></span>

## <span data-ttu-id="d20c2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d20c2-115">PARAMETERS</span></span>

### <span data-ttu-id="d20c2-116">-Capacity</span><span class="sxs-lookup"><span data-stu-id="d20c2-116">-Capacity</span></span>
<span data-ttu-id="d20c2-117">Номер экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d20c2-117">The instance number of the VM.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d20c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d20c2-118">-DefaultProfile</span></span>
<span data-ttu-id="d20c2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d20c2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d20c2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d20c2-120">-InputObject</span></span>
<span data-ttu-id="d20c2-121">Объект Cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d20c2-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d20c2-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d20c2-122">-Name</span></span>
<span data-ttu-id="d20c2-123">Имя кластера, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="d20c2-123">Name of cluster to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d20c2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d20c2-124">-ResourceGroupName</span></span>
<span data-ttu-id="d20c2-125">Имя группы ресурсов, в которой находится кластер.</span><span class="sxs-lookup"><span data-stu-id="d20c2-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d20c2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d20c2-126">-ResourceId</span></span>
<span data-ttu-id="d20c2-127">Kusto Cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="d20c2-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d20c2-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d20c2-128">-SkuName</span></span>
<span data-ttu-id="d20c2-129">Имя SKU, используемого для создания кластера</span><span class="sxs-lookup"><span data-stu-id="d20c2-129">Name of the Sku used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d20c2-130">Уровень</span><span class="sxs-lookup"><span data-stu-id="d20c2-130">-Tier</span></span>
<span data-ttu-id="d20c2-131">Имя уровня, используемого для создания кластера</span><span class="sxs-lookup"><span data-stu-id="d20c2-131">Name of the Tier used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d20c2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d20c2-132">-Confirm</span></span>
<span data-ttu-id="d20c2-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d20c2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d20c2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d20c2-134">-WhatIf</span></span>
<span data-ttu-id="d20c2-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d20c2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d20c2-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d20c2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d20c2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d20c2-137">CommonParameters</span></span>
<span data-ttu-id="d20c2-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d20c2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d20c2-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d20c2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d20c2-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d20c2-140">INPUTS</span></span>

### <span data-ttu-id="d20c2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d20c2-141">System.String</span></span>

### <span data-ttu-id="d20c2-142">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d20c2-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="d20c2-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d20c2-143">OUTPUTS</span></span>

### <span data-ttu-id="d20c2-144">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d20c2-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="d20c2-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="d20c2-145">NOTES</span></span>

## <span data-ttu-id="d20c2-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d20c2-146">RELATED LINKS</span></span>
