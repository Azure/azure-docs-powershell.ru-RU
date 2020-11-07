---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: 98936051ba3faa06d611fc8509faaa2b26998d29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720579"
---
# <span data-ttu-id="9c693-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="9c693-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="9c693-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c693-102">SYNOPSIS</span></span>
<span data-ttu-id="9c693-103">Перечислите все базы данных Kusto в кластере или получите определенную базу данных Kusto.</span><span class="sxs-lookup"><span data-stu-id="9c693-103">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="9c693-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c693-104">SYNTAX</span></span>

### <span data-ttu-id="9c693-105">ByClusterOrResourceGroupOrSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c693-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoDatabase -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c693-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9c693-106">ByResourceId</span></span>
```
Get-AzKustoDatabase [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c693-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9c693-107">ByInputObject</span></span>
```
Get-AzKustoDatabase [-Name <String>] -InputObject <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c693-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c693-108">DESCRIPTION</span></span>
<span data-ttu-id="9c693-109">Перечислите все базы данных Kusto в кластере или получите определенную базу данных Kusto.</span><span class="sxs-lookup"><span data-stu-id="9c693-109">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="9c693-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c693-110">EXAMPLES</span></span>

### <span data-ttu-id="9c693-111">Пример 1. Перечислите все базы данных Kusto в кластере по имени.</span><span class="sxs-lookup"><span data-stu-id="9c693-111">Example 1 - List all Kusto databases in a cluster by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster

Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="9c693-112">Приведенная выше команда возвращает все базы данных Kusto в кластере "mykustocluster", обнаруженные в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="9c693-112">The above command returns all Kusto databases in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="9c693-113">Пример 2. Перечисление всех баз данных Kusto в кластере с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="9c693-113">Example 2 - List all Kusto databases in a cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Get-AzKustoDatabase
Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="9c693-114">Вышеприведенная команда получит кластер Kusto с именем "mykustocluster", который находится в группе ресурсов "testrg", с помощью `Get-AzKustoCluster` командлета, а затем передать результат `Get-AzKustoDatabase` командлету, чтобы получить список всех баз данных в этом кластере.</span><span class="sxs-lookup"><span data-stu-id="9c693-114">The above command will get the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and pipe the result to the `Get-AzKustoDatabase` cmdlet to list all databases in that cluster.</span></span>

### <span data-ttu-id="9c693-115">Пример 3: получение определенной базы данных Kusto по имени</span><span class="sxs-lookup"><span data-stu-id="9c693-115">Example 3 - Get a specific Kusto database by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="9c693-116">Вышеприведенная команда возвращает базу данных Kusto с именем "mykustodatabase" в кластере "mykustocluster", которая находится в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="9c693-116">The above command returns the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="9c693-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c693-117">PARAMETERS</span></span>

### <span data-ttu-id="9c693-118">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="9c693-118">-ClusterName</span></span>
<span data-ttu-id="9c693-119">Имя кластера, в котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="9c693-119">Name of cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c693-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c693-120">-DefaultProfile</span></span>
<span data-ttu-id="9c693-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c693-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c693-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c693-122">-InputObject</span></span>
<span data-ttu-id="9c693-123">Объект Cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9c693-123">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c693-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c693-124">-Name</span></span>
<span data-ttu-id="9c693-125">имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="9c693-125">the name of the database.</span></span>

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

### <span data-ttu-id="9c693-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c693-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c693-127">Имя группы ресурсов, в которой пользователь хочет получить кластер.</span><span class="sxs-lookup"><span data-stu-id="9c693-127">Name of resource group under which the user wants to retrieve the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c693-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c693-128">-ResourceId</span></span>
<span data-ttu-id="9c693-129">Kusto Cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="9c693-129">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c693-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c693-130">CommonParameters</span></span>
<span data-ttu-id="9c693-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c693-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c693-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c693-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c693-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c693-133">INPUTS</span></span>

### <span data-ttu-id="9c693-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9c693-134">System.String</span></span>

### <span data-ttu-id="9c693-135">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="9c693-135">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="9c693-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c693-136">OUTPUTS</span></span>

### <span data-ttu-id="9c693-137">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="9c693-137">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="9c693-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c693-138">NOTES</span></span>

## <span data-ttu-id="9c693-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c693-139">RELATED LINKS</span></span>
