---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
ms.openlocfilehash: 8758cc8045856f66799144200c173ac766d8cbdb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312146"
---
# <span data-ttu-id="7b0cb-101">Get-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7b0cb-101">Get-AzSqlInstance</span></span>

## <span data-ttu-id="7b0cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b0cb-102">SYNOPSIS</span></span>
<span data-ttu-id="7b0cb-103">Возвращает сведения о экземпляре управляемой базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-103">Returns information about Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="7b0cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b0cb-104">SYNTAX</span></span>

### <span data-ttu-id="7b0cb-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b0cb-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstance [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b0cb-106">ListByInstancePoolObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b0cb-106">ListByInstancePoolObjectParameterSet</span></span>
```
Get-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b0cb-107">ListByInstancePoolResourceIdentiferParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b0cb-107">ListByInstancePoolResourceIdentiferParameterSet</span></span>
```
Get-AzSqlInstance [-InstancePoolResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b0cb-108">GetByManagedInstanceResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b0cb-108">GetByManagedInstanceResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstance [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b0cb-109">ListByInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b0cb-109">ListByInstancePoolParameterSet</span></span>
```
Get-AzSqlInstance [-InstancePoolName] <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b0cb-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b0cb-110">DESCRIPTION</span></span>
<span data-ttu-id="7b0cb-111">Командлет **Get-AzSqlInstance** возвращает сведения об одном или нескольких экземплярах, УПРАВЛЯЕМЫХ Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-111">The **Get-AzSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="7b0cb-112">Укажите имя экземпляра, чтобы просмотреть сведения только для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-112">Specify the name of an instance to see information for only that instance.</span></span>

## <span data-ttu-id="7b0cb-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b0cb-113">EXAMPLES</span></span>

### <span data-ttu-id="7b0cb-114">Пример 1: получение всех экземпляров, назначенных группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="7b0cb-114">Example 1: Get all instances assigned to a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
```

<span data-ttu-id="7b0cb-115">Эта команда получает сведения обо всех экземплярах, назначенных группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-115">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="7b0cb-116">Пример 2: получение сведений о экземпляре</span><span class="sxs-lookup"><span data-stu-id="7b0cb-116">Example 2: Get information about an  instance</span></span>
```powershell
PS C:\> Get-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
```

<span data-ttu-id="7b0cb-117">Эта команда получает сведения о экземпляре с именем managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-117">This command gets information about the instance named managedInstance1.</span></span>

### <span data-ttu-id="7b0cb-118">Пример 3: получение всех экземпляров, назначенных группе ресурсов с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="7b0cb-118">Example 3: Get all instances assigned to a resource group using filtering</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "managedInstance*"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
```

<span data-ttu-id="7b0cb-119">Эта команда получает сведения обо всех экземплярах, назначенных группе ресурсов ResourceGroup01, которая начинается с "managedInstance".</span><span class="sxs-lookup"><span data-stu-id="7b0cb-119">This command gets information about all instances assigned to the resource group ResourceGroup01 that start with "managedInstance".</span></span>

### <span data-ttu-id="7b0cb-120">Пример 4: получение всех экземпляров в пуле экземпляров</span><span class="sxs-lookup"><span data-stu-id="7b0cb-120">Example 4: Get all instances within an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstancePoolName "instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="7b0cb-121">Эта команда получает сведения обо всех экземплярах в пуле экземпляров "instancePool0".</span><span class="sxs-lookup"><span data-stu-id="7b0cb-121">This command gets information about all instances within the instance pool "instancePool0".</span></span>

### <span data-ttu-id="7b0cb-122">Пример 5: получение всех экземпляров в пуле экземпляров с помощью объекта пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="7b0cb-122">Example 5: Get all instances within an instance pool using instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName "ResourceGroup01" -Name "instancePool0"
PS C:\> Get-AzSqlInstance -InstancePool $instancePool
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="7b0cb-123">Эта команда получает сведения обо всех экземплярах в пуле экземпляров "instancePool0".</span><span class="sxs-lookup"><span data-stu-id="7b0cb-123">This command gets information about all instances within the instance pool "instancePool0".</span></span>

### <span data-ttu-id="7b0cb-124">Пример 6: получение всех экземпляров в пуле экземпляров с помощью идентификатора ресурса пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="7b0cb-124">Example 6: Get all instances within an instance pool using instance pool resource identifier</span></span>
```powershell
PS C:\> Get-AzSqlInstance -InstancePoolResourceIdentifier "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="7b0cb-125">Эта команда получает сведения обо всех экземплярах в пуле экземпляров "instancePool0".</span><span class="sxs-lookup"><span data-stu-id="7b0cb-125">This command gets information about all instances within the instance pool "instancePool0".</span></span>

### <span data-ttu-id="7b0cb-126">Пример 7: получение управляемого экземпляра с помощью его идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="7b0cb-126">Example 7: Get a managed instance using its resource identifier</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceIdentifier "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="7b0cb-127">Эта команда получает сведения о экземпляре с именем managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-127">This command gets information about the instance named managedInstance1.</span></span>

## <span data-ttu-id="7b0cb-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b0cb-128">PARAMETERS</span></span>

### <span data-ttu-id="7b0cb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b0cb-129">-DefaultProfile</span></span>
<span data-ttu-id="7b0cb-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b0cb-131">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="7b0cb-131">-InstancePool</span></span>
<span data-ttu-id="7b0cb-132">Родительский объект пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-132">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: ListByInstancePoolObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b0cb-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="7b0cb-133">-InstancePoolName</span></span>
<span data-ttu-id="7b0cb-134">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-134">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b0cb-135">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="7b0cb-135">-InstancePoolResourceId</span></span>
<span data-ttu-id="7b0cb-136">Идентификатор ресурса пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-136">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolResourceIdentiferParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b0cb-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7b0cb-137">-Name</span></span>
<span data-ttu-id="7b0cb-138">Имя экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-138">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: InstanceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b0cb-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b0cb-139">-ResourceGroupName</span></span>
<span data-ttu-id="7b0cb-140">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b0cb-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b0cb-141">-ResourceId</span></span>
<span data-ttu-id="7b0cb-142">Идентификатор ресурса управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-142">The managed instance resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b0cb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b0cb-143">CommonParameters</span></span>
<span data-ttu-id="7b0cb-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b0cb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b0cb-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b0cb-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b0cb-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b0cb-146">INPUTS</span></span>

### <span data-ttu-id="7b0cb-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="7b0cb-147">None</span></span>

## <span data-ttu-id="7b0cb-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b0cb-148">OUTPUTS</span></span>

### <span data-ttu-id="7b0cb-149">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7b0cb-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="7b0cb-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b0cb-150">NOTES</span></span>

## <span data-ttu-id="7b0cb-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b0cb-151">RELATED LINKS</span></span>