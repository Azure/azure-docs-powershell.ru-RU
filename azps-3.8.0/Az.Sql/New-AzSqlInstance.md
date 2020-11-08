---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: 34b12387ef7c967349b6c5f8599d5be361ae43e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073690"
---
# <span data-ttu-id="1ab5c-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1ab5c-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="1ab5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ab5c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ab5c-103">Создает экземпляр управляемой базы данных SQL для Azure.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="1ab5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ab5c-104">SYNTAX</span></span>

### <span data-ttu-id="1ab5c-105">NewByEditionAndComputeGenerationParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1ab5c-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-AsJob] [-MinimalTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ab5c-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ab5c-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ab5c-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ab5c-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ab5c-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="1ab5c-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ab5c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ab5c-109">DESCRIPTION</span></span>
<span data-ttu-id="1ab5c-110">Командлет **New-AzSqlInstance** создает экземпляр управляемой базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="1ab5c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ab5c-111">EXAMPLES</span></span>

### <span data-ttu-id="1ab5c-112">Пример 1: создание нового экземпляра</span><span class="sxs-lookup"><span data-stu-id="1ab5c-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="1ab5c-113">Эта команда создает новый экземпляр с помощью параметра SkuName.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="1ab5c-114">Пример 2: создание нового экземпляра</span><span class="sxs-lookup"><span data-stu-id="1ab5c-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="1ab5c-115">Эта команда создает новый экземпляр с помощью параметров выпусков и ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="1ab5c-116">Пример 3: создание нового экземпляра в пуле экземпляров с помощью объекта пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="1ab5c-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="1ab5c-117">Эта команда создает новый экземпляр в пуле экземпляров с помощью объекта пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="1ab5c-118">Пример 4: создание нового экземпляра в пуле экземпляров с помощью идентификатора ресурса пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="1ab5c-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="1ab5c-119">Эта команда создает новый экземпляр в пуле экземпляров с помощью идентификатора ресурса пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="1ab5c-120">Пример 5: создание нового экземпляра в пуле экземпляров</span><span class="sxs-lookup"><span data-stu-id="1ab5c-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="1ab5c-121">Эта команда создает новый экземпляр в пуле экземпляров с именем instancePool0</span><span class="sxs-lookup"><span data-stu-id="1ab5c-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="1ab5c-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ab5c-122">PARAMETERS</span></span>

### <span data-ttu-id="1ab5c-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="1ab5c-123">-AdministratorCredential</span></span>
<span data-ttu-id="1ab5c-124">Учетные данные проверки подлинности SQL для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="1ab5c-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ab5c-125">-AsJob</span></span>
<span data-ttu-id="1ab5c-126">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1ab5c-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ab5c-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1ab5c-127">-AssignIdentity</span></span>
<span data-ttu-id="1ab5c-128">Создайте и назначьте удостоверение Azure Active Directory для этого управляемого экземпляра для использования в службах управления ключами, таких как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="1ab5c-129">-Параметры сортировки</span><span class="sxs-lookup"><span data-stu-id="1ab5c-129">-Collation</span></span>
<span data-ttu-id="1ab5c-130">Параметры сортировки управляемого экземпляра Azure SQL, который нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-130">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="1ab5c-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="1ab5c-131">-ComputeGeneration</span></span>
<span data-ttu-id="1ab5c-132">Вычисленое поколение для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-132">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="1ab5c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ab5c-133">-DefaultProfile</span></span>
<span data-ttu-id="1ab5c-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ab5c-135">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="1ab5c-135">-DnsZonePartner</span></span>
<span data-ttu-id="1ab5c-136">Идентификатор ресурса сервера, управляемого партнером, для наследования свойства DnsZone из для создания управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-136">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="1ab5c-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="1ab5c-137">-Edition</span></span>
<span data-ttu-id="1ab5c-138">Выпуск для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-138">The edition for the instance.</span></span>

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

### <span data-ttu-id="1ab5c-139">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="1ab5c-139">-InstancePool</span></span>
<span data-ttu-id="1ab5c-140">Родительский объект пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-140">The instance pool parent object.</span></span>

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

### <span data-ttu-id="1ab5c-141">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="1ab5c-141">-MinimalTlsVersion</span></span>
<span data-ttu-id="1ab5c-142">Минимальная версия TLS для обеспечения управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="1ab5c-142">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="1ab5c-143">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="1ab5c-143">-InstancePoolName</span></span>
<span data-ttu-id="1ab5c-144">Пул экземпляров, в котором нужно разместить этот экземпляр.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-144">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="1ab5c-145">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="1ab5c-145">-InstancePoolResourceId</span></span>
<span data-ttu-id="1ab5c-146">Идентификатор ресурса пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-146">The instance pool resource id.</span></span>

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

### <span data-ttu-id="1ab5c-147">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1ab5c-147">-LicenseType</span></span>
<span data-ttu-id="1ab5c-148">Определяет, какой тип лицензии следует использовать.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-148">Determines which License Type to use.</span></span> <span data-ttu-id="1ab5c-149">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1ab5c-149">Possible values are:</span></span>
- <span data-ttu-id="1ab5c-150">BasePrice — гибридное выгодное преимущество (AHB) для существующих владельцев лицензий SQL Server применяется скидка.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-150">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="1ab5c-151">Служба управляемого экземпляра будет скидкам для существующих владельцев лицензий SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-151">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="1ab5c-152">LicenseIncluded-(AHB) для существующих владельцев лицензий SQL Server не применяется скидка на гибридные льготы для использования в Azure.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-152">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="1ab5c-153">Служба управляемого экземпляра будет включать в себя новые цены на лицензии SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-153">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="1ab5c-154">-Location</span><span class="sxs-lookup"><span data-stu-id="1ab5c-154">-Location</span></span>
<span data-ttu-id="1ab5c-155">Расположение, в котором нужно создать экземпляр.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-155">The location in which to create the instance</span></span>

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

### <span data-ttu-id="1ab5c-156">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ab5c-156">-Name</span></span>
<span data-ttu-id="1ab5c-157">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-157">Instance name.</span></span>

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

### <span data-ttu-id="1ab5c-158">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="1ab5c-158">-ProxyOverride</span></span>
<span data-ttu-id="1ab5c-159">Тип соединения, который используется для подключения к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-159">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="1ab5c-160">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="1ab5c-160">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="1ab5c-161">Включена ли конечная точка открытых данных для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-161">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="1ab5c-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ab5c-162">-ResourceGroupName</span></span>
<span data-ttu-id="1ab5c-163">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-163">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ab5c-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1ab5c-164">-SkuName</span></span>
<span data-ttu-id="1ab5c-165">Имя SKU для экземпляра, например "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="1ab5c-165">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="1ab5c-166">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="1ab5c-166">-StorageSizeInGB</span></span>
<span data-ttu-id="1ab5c-167">Определяет объем хранилища, связанного с экземпляром</span><span class="sxs-lookup"><span data-stu-id="1ab5c-167">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="1ab5c-168">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1ab5c-168">-SubnetId</span></span>
<span data-ttu-id="1ab5c-169">Идентификатор подсети, который будет использоваться для создания экземпляра</span><span class="sxs-lookup"><span data-stu-id="1ab5c-169">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="1ab5c-170">-Тег</span><span class="sxs-lookup"><span data-stu-id="1ab5c-170">-Tag</span></span>
<span data-ttu-id="1ab5c-171">Теги, связываемые с экземпляром</span><span class="sxs-lookup"><span data-stu-id="1ab5c-171">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="1ab5c-172">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="1ab5c-172">-TimezoneId</span></span>
<span data-ttu-id="1ab5c-173">Идентификатор часового пояса для устанавливаемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-173">The time zone id for the instance to set.</span></span> <span data-ttu-id="1ab5c-174">Список идентификаторов часовых поясов предоставляется с помощью представления sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="1ab5c-174">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="1ab5c-175">-VCore</span><span class="sxs-lookup"><span data-stu-id="1ab5c-175">-VCore</span></span>
<span data-ttu-id="1ab5c-176">Определяет, сколько VCore связать с экземпляром</span><span class="sxs-lookup"><span data-stu-id="1ab5c-176">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="1ab5c-177">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ab5c-177">-Confirm</span></span>
<span data-ttu-id="1ab5c-178">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ab5c-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ab5c-179">-WhatIf</span></span>
<span data-ttu-id="1ab5c-180">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ab5c-181">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ab5c-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ab5c-182">CommonParameters</span></span>
<span data-ttu-id="1ab5c-183">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ab5c-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ab5c-184">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ab5c-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ab5c-185">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ab5c-185">INPUTS</span></span>

### <span data-ttu-id="1ab5c-186">Ничего</span><span class="sxs-lookup"><span data-stu-id="1ab5c-186">None</span></span>

## <span data-ttu-id="1ab5c-187">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ab5c-187">OUTPUTS</span></span>

### <span data-ttu-id="1ab5c-188">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="1ab5c-188">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="1ab5c-189">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ab5c-189">NOTES</span></span>

## <span data-ttu-id="1ab5c-190">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ab5c-190">RELATED LINKS</span></span>
