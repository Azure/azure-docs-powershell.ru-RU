---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a68604e9701a6ae2c251edf3f2a0935df5ffa94f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900046"
---
# <span data-ttu-id="40429-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="40429-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="40429-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40429-102">SYNOPSIS</span></span>
<span data-ttu-id="40429-103">Список всех кластеров Kusto в группе ресурсов или получение определенного кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="40429-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="40429-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40429-104">SYNTAX</span></span>

### <span data-ttu-id="40429-105">ByClusterOrResourceGroupOrSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40429-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40429-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="40429-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40429-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40429-107">DESCRIPTION</span></span>
<span data-ttu-id="40429-108">Список всех кластеров Kusto в группе ресурсов или получение определенного кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="40429-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="40429-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40429-109">EXAMPLES</span></span>

### <span data-ttu-id="40429-110">Пример 1: список всех кластеров Kusto в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="40429-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="40429-111">Тип: Microsoft. Kusto/Clusters ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup: testrg имя: mykustocluster1 расположение: Центральная американская емкость: 3 SKU: D13_v2 ProvisioningState: успешное состояние: запущенный тег: {} URI: https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster1.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="40429-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net</span></span>

<span data-ttu-id="40429-112">Тип: Microsoft. Kusto/Clusters ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup: testrg имя: mykustocluster2 расположение: Центральная американская емкость: 5 SKU: D13_v2 ProvisioningState: успешное состояние: запущенный тег: {} URI: https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster2.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="40429-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster2.centralus.kusto.windows.net</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="40429-113">В приведенной выше команде перечислены все кластеры Kusto в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="40429-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="40429-114">Пример 2: получение определенного имени Kusto кластера</span><span class="sxs-lookup"><span data-stu-id="40429-114">Example 2 - Get a specific Kusto cluster by name</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="40429-115">Приведенная выше команда возвращает кластер Kusto с именем "mykustocluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="40429-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="40429-116">Пример 3: получение определенного кластера Kusto по ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="40429-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/clusters/mykustocluster
Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="40429-117">Приведенная выше команда возвращает кластер Kusto с именем "mykustocluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="40429-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="40429-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40429-118">PARAMETERS</span></span>

### <span data-ttu-id="40429-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40429-119">-DefaultProfile</span></span>
<span data-ttu-id="40429-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40429-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40429-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40429-121">-Name</span></span>
<span data-ttu-id="40429-122">Имя определенного кластера.</span><span class="sxs-lookup"><span data-stu-id="40429-122">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40429-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40429-123">-ResourceGroupName</span></span>
<span data-ttu-id="40429-124">Имя группы ресурсов, в которой пользователь хочет получить кластер.</span><span class="sxs-lookup"><span data-stu-id="40429-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="40429-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40429-125">-ResourceId</span></span>
<span data-ttu-id="40429-126">Kusto Cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="40429-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="40429-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40429-127">CommonParameters</span></span>
<span data-ttu-id="40429-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40429-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40429-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40429-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40429-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40429-130">INPUTS</span></span>

### <span data-ttu-id="40429-131">System. String</span><span class="sxs-lookup"><span data-stu-id="40429-131">System.String</span></span>

## <span data-ttu-id="40429-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40429-132">OUTPUTS</span></span>

### <span data-ttu-id="40429-133">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="40429-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="40429-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="40429-134">NOTES</span></span>

## <span data-ttu-id="40429-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40429-135">RELATED LINKS</span></span>
