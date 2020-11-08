---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: ed039eefe46a1527948e7fffc3030f209a91b0c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065601"
---
# <span data-ttu-id="40034-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="40034-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="40034-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40034-102">SYNOPSIS</span></span>
<span data-ttu-id="40034-103">Создает новую базу данных Kusto в существующем кластере.</span><span class="sxs-lookup"><span data-stu-id="40034-103">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="40034-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40034-104">SYNTAX</span></span>

### <span data-ttu-id="40034-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40034-105">ByNameAndResourceGroup (Default)</span></span>
```
New-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40034-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="40034-106">ByResourceId</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40034-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="40034-107">ByInputObject</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-InputObject] <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40034-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40034-108">DESCRIPTION</span></span>
<span data-ttu-id="40034-109">Создает новую базу данных Kusto в существующем кластере.</span><span class="sxs-lookup"><span data-stu-id="40034-109">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="40034-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40034-110">EXAMPLES</span></span>

### <span data-ttu-id="40034-111">Пример 1: создание новой базы данных Kusto по имени</span><span class="sxs-lookup"><span data-stu-id="40034-111">Example 1 - Create a new Kusto database by name</span></span>

```
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 4 -HotCachePeriodInDays 2

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 4
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="40034-112">Вышеприведенная команда создает новую базу данных Kusto с именем "mykustodatabase" в существующем кластере "mykustocluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="40034-112">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="40034-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40034-113">PARAMETERS</span></span>

### <span data-ttu-id="40034-114">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="40034-114">-ClusterName</span></span>
<span data-ttu-id="40034-115">Имя кластера, в котором вы хотите создать базу данных.</span><span class="sxs-lookup"><span data-stu-id="40034-115">Name of cluster under which you want to create the database.</span></span>

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

### <span data-ttu-id="40034-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40034-116">-DefaultProfile</span></span>
<span data-ttu-id="40034-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40034-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40034-118">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="40034-118">-HotCachePeriodInDays</span></span>
<span data-ttu-id="40034-119">Количество дней, в течение которых данные будут храниться в кэше для быстрого запроса.</span><span class="sxs-lookup"><span data-stu-id="40034-119">The number of days of data that should be kept in cache for fast queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40034-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40034-120">-InputObject</span></span>
<span data-ttu-id="40034-121">Объект Cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="40034-121">Kusto cluster object.</span></span>

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

### <span data-ttu-id="40034-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40034-122">-Name</span></span>
<span data-ttu-id="40034-123">Имя базы данных, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="40034-123">Name of the database to be created.</span></span>

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

### <span data-ttu-id="40034-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40034-124">-ResourceGroupName</span></span>
<span data-ttu-id="40034-125">Имя группы ресурсов, в которой находится кластер.</span><span class="sxs-lookup"><span data-stu-id="40034-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="40034-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40034-126">-ResourceId</span></span>
<span data-ttu-id="40034-127">Kusto Cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="40034-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="40034-128">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="40034-128">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="40034-129">Количество дней, в течение которых данные будут храниться, прежде чем она станет доступна для запросов.</span><span class="sxs-lookup"><span data-stu-id="40034-129">The number of days data should be kept before it stops being accessible to queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40034-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40034-130">-Confirm</span></span>
<span data-ttu-id="40034-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40034-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40034-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40034-132">-WhatIf</span></span>
<span data-ttu-id="40034-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40034-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40034-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40034-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40034-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40034-135">CommonParameters</span></span>
<span data-ttu-id="40034-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40034-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40034-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40034-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40034-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40034-138">INPUTS</span></span>

### <span data-ttu-id="40034-139">System. String</span><span class="sxs-lookup"><span data-stu-id="40034-139">System.String</span></span>

### <span data-ttu-id="40034-140">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="40034-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="40034-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40034-141">OUTPUTS</span></span>

### <span data-ttu-id="40034-142">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="40034-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="40034-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="40034-143">NOTES</span></span>

## <span data-ttu-id="40034-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40034-144">RELATED LINKS</span></span>
