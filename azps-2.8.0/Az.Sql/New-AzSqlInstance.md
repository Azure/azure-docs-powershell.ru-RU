---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: d80e6ddd7fa420b07a0df30c2718d9c4e96123fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906578"
---
# <span data-ttu-id="11562-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11562-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="11562-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11562-102">SYNOPSIS</span></span>
<span data-ttu-id="11562-103">Создает экземпляр управляемой базы данных SQL для Azure.</span><span class="sxs-lookup"><span data-stu-id="11562-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="11562-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11562-104">SYNTAX</span></span>

### <span data-ttu-id="11562-105">NewByEditionAndComputeGenerationParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11562-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11562-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11562-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11562-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11562-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11562-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="11562-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11562-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11562-109">DESCRIPTION</span></span>
<span data-ttu-id="11562-110">Командлет **New-AzSqlInstance** создает экземпляр управляемой базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="11562-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="11562-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11562-111">EXAMPLES</span></span>

### <span data-ttu-id="11562-112">Пример 1: создание нового экземпляра</span><span class="sxs-lookup"><span data-stu-id="11562-112">Example 1: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4 -DnsZonePartner "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/partnerServerForDnsZone"
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
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="11562-113">Эта команда создает новый экземпляр с помощью параметра SkuName.</span><span class="sxs-lookup"><span data-stu-id="11562-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="11562-114">Пример 2: создание нового экземпляра</span><span class="sxs-lookup"><span data-stu-id="11562-114">Example 2: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="11562-115">Эта команда создает новый экземпляр с помощью параметров выпусков и ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="11562-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="11562-116">Пример 3: создание нового экземпляра в пуле экземпляров с помощью объекта пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="11562-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="11562-117">Эта команда создает новый экземпляр в пуле экземпляров с помощью объекта пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="11562-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="11562-118">Пример 4: создание нового экземпляра в пуле экземпляров с помощью идентификатора ресурса пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="11562-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
```powershell
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="11562-119">Эта команда создает новый экземпляр в пуле экземпляров с помощью идентификатора ресурса пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="11562-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="11562-120">Пример 5: создание нового экземпляра в пуле экземпляров</span><span class="sxs-lookup"><span data-stu-id="11562-120">Example 5: Create a new instance in an instance pool</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 32 -VCore 2 -ComputeGeneration Gen5 -Edition GeneralPurpose -InstancePoolName instancePool0
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
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 32
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="11562-121">Эта команда создает новый экземпляр в пуле экземпляров с именем instancePool0</span><span class="sxs-lookup"><span data-stu-id="11562-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="11562-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11562-122">PARAMETERS</span></span>

### <span data-ttu-id="11562-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="11562-123">-AdministratorCredential</span></span>
<span data-ttu-id="11562-124">Учетные данные проверки подлинности SQL для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="11562-124">The SQL authentication credential of the instance.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11562-125">-AsJob</span></span>
<span data-ttu-id="11562-126">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="11562-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="11562-127">-AssignIdentity</span></span>
<span data-ttu-id="11562-128">Создайте и назначьте удостоверение Azure Active Directory для этого управляемого экземпляра для использования в службах управления ключами, таких как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="11562-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-129">-Параметры сортировки</span><span class="sxs-lookup"><span data-stu-id="11562-129">-Collation</span></span>
<span data-ttu-id="11562-130">Параметры сортировки управляемого экземпляра Azure SQL, который нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="11562-130">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="11562-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="11562-131">-ComputeGeneration</span></span>
<span data-ttu-id="11562-132">Вычисленое поколение для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="11562-132">The compute generation for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11562-133">-DefaultProfile</span></span>
<span data-ttu-id="11562-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11562-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11562-135">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="11562-135">-DnsZonePartner</span></span>
<span data-ttu-id="11562-136">Идентификатор ресурса сервера, управляемого партнером, для наследования свойства DnsZone из для создания управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="11562-136">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="11562-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="11562-137">-Edition</span></span>
<span data-ttu-id="11562-138">Выпуск для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="11562-138">The edition for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-139">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="11562-139">-InstancePool</span></span>
<span data-ttu-id="11562-140">Родительский объект пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="11562-140">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: NewByInstancePoolParentObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11562-141">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="11562-141">-InstancePoolName</span></span>
<span data-ttu-id="11562-142">Пул экземпляров, в котором нужно разместить этот экземпляр.</span><span class="sxs-lookup"><span data-stu-id="11562-142">The instance pool to place this instance in.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-143">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="11562-143">-InstancePoolResourceId</span></span>
<span data-ttu-id="11562-144">Идентификатор ресурса пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="11562-144">The instance pool resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByInstancePoolResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11562-145">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="11562-145">-LicenseType</span></span>
<span data-ttu-id="11562-146">Определяет, какой тип лицензии следует использовать.</span><span class="sxs-lookup"><span data-stu-id="11562-146">Determines which License Type to use.</span></span> <span data-ttu-id="11562-147">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="11562-147">Possible values are:</span></span>
- <span data-ttu-id="11562-148">BasePrice — гибридное выгодное преимущество (AHB) для существующих владельцев лицензий SQL Server применяется скидка.</span><span class="sxs-lookup"><span data-stu-id="11562-148">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="11562-149">Служба управляемого экземпляра будет скидкам для существующих владельцев лицензий SQL Server.</span><span class="sxs-lookup"><span data-stu-id="11562-149">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="11562-150">LicenseIncluded-(AHB) для существующих владельцев лицензий SQL Server не применяется скидка на гибридные льготы для использования в Azure.</span><span class="sxs-lookup"><span data-stu-id="11562-150">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="11562-151">Служба управляемого экземпляра будет включать в себя новые цены на лицензии SQL Server.</span><span class="sxs-lookup"><span data-stu-id="11562-151">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-152">-Location</span><span class="sxs-lookup"><span data-stu-id="11562-152">-Location</span></span>
<span data-ttu-id="11562-153">Расположение, в котором нужно создать экземпляр.</span><span class="sxs-lookup"><span data-stu-id="11562-153">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-154">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11562-154">-Name</span></span>
<span data-ttu-id="11562-155">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="11562-155">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-156">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="11562-156">-ProxyOverride</span></span>
<span data-ttu-id="11562-157">Тип соединения, который используется для подключения к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="11562-157">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="11562-158">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="11562-158">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="11562-159">Включена ли конечная точка открытых данных для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="11562-159">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11562-160">-ResourceGroupName</span></span>
<span data-ttu-id="11562-161">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11562-161">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-162">-SkuName</span><span class="sxs-lookup"><span data-stu-id="11562-162">-SkuName</span></span>
<span data-ttu-id="11562-163">Имя SKU для экземпляра, например "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="11562-163">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: System.String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-164">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="11562-164">-StorageSizeInGB</span></span>
<span data-ttu-id="11562-165">Определяет объем хранилища, связанного с экземпляром</span><span class="sxs-lookup"><span data-stu-id="11562-165">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-166">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="11562-166">-SubnetId</span></span>
<span data-ttu-id="11562-167">Идентификатор подсети, который будет использоваться для создания экземпляра</span><span class="sxs-lookup"><span data-stu-id="11562-167">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-168">-Тег</span><span class="sxs-lookup"><span data-stu-id="11562-168">-Tag</span></span>
<span data-ttu-id="11562-169">Теги, связываемые с экземпляром</span><span class="sxs-lookup"><span data-stu-id="11562-169">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11562-170">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="11562-170">-TimezoneId</span></span>
<span data-ttu-id="11562-171">Идентификатор часового пояса для устанавливаемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="11562-171">The time zone id for the instance to set.</span></span> <span data-ttu-id="11562-172">Список идентификаторов часовых поясов предоставляется с помощью представления sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="11562-172">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="11562-173">-VCore</span><span class="sxs-lookup"><span data-stu-id="11562-173">-VCore</span></span>
<span data-ttu-id="11562-174">Определяет, сколько VCore связать с экземпляром</span><span class="sxs-lookup"><span data-stu-id="11562-174">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="11562-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11562-175">-Confirm</span></span>
<span data-ttu-id="11562-176">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11562-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11562-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11562-177">-WhatIf</span></span>
<span data-ttu-id="11562-178">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11562-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11562-179">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11562-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11562-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11562-180">CommonParameters</span></span>
<span data-ttu-id="11562-181">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11562-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11562-182">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11562-182">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11562-183">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11562-183">INPUTS</span></span>

### <span data-ttu-id="11562-184">Ничего</span><span class="sxs-lookup"><span data-stu-id="11562-184">None</span></span>

## <span data-ttu-id="11562-185">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11562-185">OUTPUTS</span></span>

### <span data-ttu-id="11562-186">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="11562-186">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="11562-187">Пуск</span><span class="sxs-lookup"><span data-stu-id="11562-187">NOTES</span></span>

## <span data-ttu-id="11562-188">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11562-188">RELATED LINKS</span></span>
