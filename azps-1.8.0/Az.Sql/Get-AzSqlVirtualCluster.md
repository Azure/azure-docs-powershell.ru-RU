---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: f5e52938a6d0f618d53621a895aeb7037dc543ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728911"
---
# <span data-ttu-id="eeda4-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="eeda4-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="eeda4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eeda4-102">SYNOPSIS</span></span>
<span data-ttu-id="eeda4-103">Возвращает сведения о виртуальном кластере Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="eeda4-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="eeda4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eeda4-104">SYNTAX</span></span>

### <span data-ttu-id="eeda4-105">GetVirtualClusterByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eeda4-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eeda4-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eeda4-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eeda4-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="eeda4-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eeda4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eeda4-108">DESCRIPTION</span></span>
<span data-ttu-id="eeda4-109">Командлет **Get-AzSqlVirtualCluster** возвращает сведения об одном или нескольких виртуальных кластерах Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="eeda4-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="eeda4-110">Укажите имя виртуального кластера, чтобы просмотреть сведения только для этого кластера.</span><span class="sxs-lookup"><span data-stu-id="eeda4-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="eeda4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eeda4-111">EXAMPLES</span></span>

### <span data-ttu-id="eeda4-112">Пример 1: получение всех виртуальных кластеров, назначенных группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="eeda4-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
```powershell
PS C:> Get-AzSqlVirtualCluster -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster2
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster2
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name2

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster3
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster3
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name3
```

<span data-ttu-id="eeda4-113">Эта команда получает сведения обо всех виртуальных кластерах, назначенных группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="eeda4-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="eeda4-114">Пример 2: получение сведений о конкретном виртуальном кластере</span><span class="sxs-lookup"><span data-stu-id="eeda4-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="eeda4-115">Эта команда получает сведения о виртуальном кластере VirtualCluster1 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="eeda4-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="eeda4-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eeda4-116">PARAMETERS</span></span>

### <span data-ttu-id="eeda4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeda4-117">-DefaultProfile</span></span>
<span data-ttu-id="eeda4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eeda4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeda4-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eeda4-119">-Name</span></span>
<span data-ttu-id="eeda4-120">Имя виртуального кластера.</span><span class="sxs-lookup"><span data-stu-id="eeda4-120">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeda4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeda4-121">-ResourceGroupName</span></span>
<span data-ttu-id="eeda4-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eeda4-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeda4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eeda4-123">-ResourceId</span></span>
<span data-ttu-id="eeda4-124">Идентификатор ресурса объекта экземпляра, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="eeda4-124">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeda4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeda4-125">CommonParameters</span></span>
<span data-ttu-id="eeda4-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eeda4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeda4-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eeda4-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeda4-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eeda4-128">INPUTS</span></span>

### <span data-ttu-id="eeda4-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="eeda4-129">None</span></span>

## <span data-ttu-id="eeda4-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eeda4-130">OUTPUTS</span></span>

### <span data-ttu-id="eeda4-131">Microsoft. Azure. Commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="eeda4-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="eeda4-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="eeda4-132">NOTES</span></span>

## <span data-ttu-id="eeda4-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eeda4-133">RELATED LINKS</span></span>
