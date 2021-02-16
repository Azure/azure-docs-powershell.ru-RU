---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: c5c7cdffc8b329fdff426f48f60869ca6821f32d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399232"
---
# <span data-ttu-id="2b23d-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="2b23d-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="2b23d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b23d-102">SYNOPSIS</span></span>
<span data-ttu-id="2b23d-103">Со списком всех кластеров "Кусто" в группе ресурсов или с конкретным кластером "Кусто".</span><span class="sxs-lookup"><span data-stu-id="2b23d-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="2b23d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2b23d-104">SYNTAX</span></span>

### <span data-ttu-id="2b23d-105">ByClusterOrResourceGroupOrSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b23d-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b23d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2b23d-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b23d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b23d-107">DESCRIPTION</span></span>
<span data-ttu-id="2b23d-108">Со списком всех кластеров "Кусто" в группе ресурсов или с конкретным кластером "Кусто".</span><span class="sxs-lookup"><span data-stu-id="2b23d-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="2b23d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2b23d-109">EXAMPLES</span></span>

### <span data-ttu-id="2b23d-110">Пример 1. Список всех кластеров кусто в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="2b23d-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="2b23d-111">Type : Microsoft.Kusto/Clusters Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup : testrg Name : mykustocluster1 Location : Central US Capacity : 3 SKU : D13_v2 ProvisioningState : Succeeded State : Running Tag : {} Uri : `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri : `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="2b23d-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span></span>

<span data-ttu-id="2b23d-112">Type : Microsoft.Kusto/Clusters Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup : testrg Name : mykustocluster2 Location : Central US Capacity : 5 SKU : D13_v2 ProvisioningState : Succeeded State : Running Tag : {} Uri : `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri : `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="2b23d-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="2b23d-113">В этой команде перечислены все кластеры Кусто в группе ресурсов Testrg.</span><span class="sxs-lookup"><span data-stu-id="2b23d-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="2b23d-114">Пример 2. Получить конкретный кластер кусто по имени</span><span class="sxs-lookup"><span data-stu-id="2b23d-114">Example 2 - Get a specific Kusto cluster by name</span></span>

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

<span data-ttu-id="2b23d-115">Она возвращает кластер Кусто с именем "mykustocluster" в группе ресурсов testrg.</span><span class="sxs-lookup"><span data-stu-id="2b23d-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="2b23d-116">Пример 3. Получите конкретный кластер кусто по ид ресурса</span><span class="sxs-lookup"><span data-stu-id="2b23d-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

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

<span data-ttu-id="2b23d-117">Она возвращает кластер Кусто с именем "mykustocluster" в группе ресурсов testrg.</span><span class="sxs-lookup"><span data-stu-id="2b23d-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="2b23d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b23d-118">PARAMETERS</span></span>

### <span data-ttu-id="2b23d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b23d-119">-DefaultProfile</span></span>
<span data-ttu-id="2b23d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b23d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b23d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2b23d-121">-Name</span></span>
<span data-ttu-id="2b23d-122">Название определенного кластера.</span><span class="sxs-lookup"><span data-stu-id="2b23d-122">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="2b23d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b23d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b23d-124">Имя группы ресурсов, для которой пользователь хочет получить кластер.</span><span class="sxs-lookup"><span data-stu-id="2b23d-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="2b23d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b23d-125">-ResourceId</span></span>
<span data-ttu-id="2b23d-126">Кусто, кластер и ИД ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2b23d-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="2b23d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b23d-127">CommonParameters</span></span>
<span data-ttu-id="2b23d-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b23d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b23d-129">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b23d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b23d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b23d-130">INPUTS</span></span>

### <span data-ttu-id="2b23d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2b23d-131">System.String</span></span>

## <span data-ttu-id="2b23d-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2b23d-132">OUTPUTS</span></span>

### <span data-ttu-id="2b23d-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="2b23d-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="2b23d-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2b23d-134">NOTES</span></span>

## <span data-ttu-id="2b23d-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b23d-135">RELATED LINKS</span></span>
