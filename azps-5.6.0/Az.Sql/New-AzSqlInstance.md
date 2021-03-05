---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: 9f648f0e2ab15919f3caa849041846570d627df5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970200"
---
# <span data-ttu-id="c682a-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c682a-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="c682a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c682a-102">SYNOPSIS</span></span>
<span data-ttu-id="c682a-103">Создает экземпляр управляемой базы SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c682a-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="c682a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c682a-104">SYNTAX</span></span>

### <span data-ttu-id="c682a-105">NewByEditionAndComputeGenerationParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c682a-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c682a-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c682a-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c682a-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c682a-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c682a-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="c682a-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c682a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c682a-109">DESCRIPTION</span></span>
<span data-ttu-id="c682a-110">С **его использованием** создается экземпляр Azure SQL Database Managed.</span><span class="sxs-lookup"><span data-stu-id="c682a-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="c682a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c682a-111">EXAMPLES</span></span>

### <span data-ttu-id="c682a-112">Пример 1. Создание нового экземпляра</span><span class="sxs-lookup"><span data-stu-id="c682a-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="c682a-113">Эта команда создает новый экземпляр с использованием параметра SkuName.</span><span class="sxs-lookup"><span data-stu-id="c682a-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="c682a-114">Пример 2. Создание экземпляра</span><span class="sxs-lookup"><span data-stu-id="c682a-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="c682a-115">Эта команда создает новый экземпляр с использованием параметров Edition и ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="c682a-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="c682a-116">Пример 3. Создание экземпляра в пуле экземпляров с помощью объекта пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="c682a-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="c682a-117">Эта команда создает новый экземпляр в пуле экземпляров с использованием объекта пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c682a-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="c682a-118">Пример 4. Создание экземпляра в пуле экземпляров с помощью идентификатора ресурса пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="c682a-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="c682a-119">Эта команда создает новый экземпляр в пуле экземпляров с использованием идентификатора ресурса пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c682a-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="c682a-120">Пример 5. Создание экземпляра в пуле экземпляров</span><span class="sxs-lookup"><span data-stu-id="c682a-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="c682a-121">Эта команда создает новый экземпляр в пуле экземпляров с экземпляром InstancePool0</span><span class="sxs-lookup"><span data-stu-id="c682a-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

### <span data-ttu-id="c682a-122">Пример 6. Создание экземпляра с конфигурацией обслуживания</span><span class="sxs-lookup"><span data-stu-id="c682a-122">Example 6: Create a new instance with maintenance configuration</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourcegroup01 -Location "westus" -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -ComputeGeneration Gen5 -Edition GeneralPurpose -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
Location                   : westus
Id                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName          : resourcegroup01
ManagedInstanceName        : managedInstance1
Tags                       :
Identity                   :
Sku                        : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName   : managedInstance1.wusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin         : adminLogin1
AdministratorPassword      :
SubnetId                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType                : LicenseIncluded
VCores                     : 8
StorageSizeInGB            : 256
Collation                  : SQL_Latin1_General_CP1_CI_AS
PublicDataEndpointEnabled  : False
ProxyOverride              :
TimezoneId                 : UTC
DnsZonePartner             :
DnsZone                    : ad35cna0mw
InstancePoolName           :
MinimalTlsVersion          :
BackupStorageRedundancy    : Geo
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2
```

<span data-ttu-id="c682a-123">Эта команда создает новый экземпляр с конфигурацией обслуживания MI_2</span><span class="sxs-lookup"><span data-stu-id="c682a-123">This command creates a new instance with maintenance configuration MI_2</span></span>

## <span data-ttu-id="c682a-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c682a-124">PARAMETERS</span></span>

### <span data-ttu-id="c682a-125">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="c682a-125">-AdministratorCredential</span></span>
<span data-ttu-id="c682a-126">Учетные SQL проверки подлинности экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c682a-126">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="c682a-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c682a-127">-AsJob</span></span>
<span data-ttu-id="c682a-128">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c682a-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c682a-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c682a-129">-AssignIdentity</span></span>
<span data-ttu-id="c682a-130">Создание и назначение удостоверения Azure Active Directory для этого управляемого экземпляра для использования с ключевыми службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c682a-130">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c682a-131">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="c682a-131">-BackupStorageRedundancy</span></span>
<span data-ttu-id="c682a-132">Избыточность резервного копирования хранилища, используемого для хранения резервных копий управляемого экземпляра Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="c682a-132">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="c682a-133">Возможные варианты: Local (Локальный), Zone (Зона) и Geo (География)</span><span class="sxs-lookup"><span data-stu-id="c682a-133">Options are: Local, Zone and Geo</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c682a-134">-Collation</span><span class="sxs-lookup"><span data-stu-id="c682a-134">-Collation</span></span>
<span data-ttu-id="c682a-135">Разлиновка управляемого экземпляра Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c682a-135">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="c682a-136">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="c682a-136">-ComputeGeneration</span></span>
<span data-ttu-id="c682a-137">The compute generation for the instance.</span><span class="sxs-lookup"><span data-stu-id="c682a-137">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="c682a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c682a-138">-DefaultProfile</span></span>
<span data-ttu-id="c682a-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c682a-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c682a-140">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="c682a-140">-DnsZonePartner</span></span>
<span data-ttu-id="c682a-141">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span><span class="sxs-lookup"><span data-stu-id="c682a-141">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="c682a-142">-Edition</span><span class="sxs-lookup"><span data-stu-id="c682a-142">-Edition</span></span>
<span data-ttu-id="c682a-143">Выпуск для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c682a-143">The edition for the instance.</span></span>

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

### <span data-ttu-id="c682a-144">-Force</span><span class="sxs-lookup"><span data-stu-id="c682a-144">-Force</span></span>
<span data-ttu-id="c682a-145">Пропустить сообщение подтверждения для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="c682a-145">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c682a-146">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="c682a-146">-InstancePool</span></span>
<span data-ttu-id="c682a-147">Родительский объект пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c682a-147">The instance pool parent object.</span></span>

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

### <span data-ttu-id="c682a-148">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="c682a-148">-InstancePoolName</span></span>
<span data-ttu-id="c682a-149">Пул экземпляров для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c682a-149">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="c682a-150">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="c682a-150">-InstancePoolResourceId</span></span>
<span data-ttu-id="c682a-151">ИД пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="c682a-151">The instance pool resource id.</span></span>

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

### <span data-ttu-id="c682a-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c682a-152">-LicenseType</span></span>
<span data-ttu-id="c682a-153">Определяет тип лицензии.</span><span class="sxs-lookup"><span data-stu-id="c682a-153">Determines which License Type to use.</span></span> <span data-ttu-id="c682a-154">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="c682a-154">Possible values are:</span></span>
- <span data-ttu-id="c682a-155">BasePrice — скидка на гибридное преимущество Azure (AHB) для существующих SQL Server лицензий применяется.</span><span class="sxs-lookup"><span data-stu-id="c682a-155">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="c682a-156">Для существующих владельцев лицензий на управляемый экземпляр скидка SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c682a-156">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="c682a-157">LicenseIncluded — скидка на azure Hybrid Benefit (AHB) для существующих SQL Server лицензий не применяется.</span><span class="sxs-lookup"><span data-stu-id="c682a-157">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="c682a-158">Стоимость услуги Managed Instance будет включать новую стоимость SQL Server стоимостью лицензий.</span><span class="sxs-lookup"><span data-stu-id="c682a-158">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="c682a-159">-Location</span><span class="sxs-lookup"><span data-stu-id="c682a-159">-Location</span></span>
<span data-ttu-id="c682a-160">Расположение для создания экземпляра</span><span class="sxs-lookup"><span data-stu-id="c682a-160">The location in which to create the instance</span></span>

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

### <span data-ttu-id="c682a-161">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c682a-161">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="c682a-162">Конфигурация обслуживания для управляемого экземпляра Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="c682a-162">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="c682a-163">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c682a-163">-MinimalTlsVersion</span></span>
<span data-ttu-id="c682a-164">Минимальная версия TLS, которая будет применяться для управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="c682a-164">The minimal TLS version to enforce for Managed instance</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c682a-165">-Name</span><span class="sxs-lookup"><span data-stu-id="c682a-165">-Name</span></span>
<span data-ttu-id="c682a-166">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c682a-166">Instance name.</span></span>

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

### <span data-ttu-id="c682a-167">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="c682a-167">-ProxyOverride</span></span>
<span data-ttu-id="c682a-168">Тип подключения, используемый для подключения к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="c682a-168">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="c682a-169">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="c682a-169">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="c682a-170">Включена ли конечная точка общедоступных данных для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c682a-170">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="c682a-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c682a-171">-ResourceGroupName</span></span>
<span data-ttu-id="c682a-172">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c682a-172">The name of the resource group.</span></span>

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

### <span data-ttu-id="c682a-173">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c682a-173">-SkuName</span></span>
<span data-ttu-id="c682a-174">Имя SKU экземпляра, например "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="c682a-174">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="c682a-175">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="c682a-175">-StorageSizeInGB</span></span>
<span data-ttu-id="c682a-176">Определяет размер хранилища, который нужно связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="c682a-176">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="c682a-177">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c682a-177">-SubnetId</span></span>
<span data-ttu-id="c682a-178">ИД подсети, который используется для создания экземпляра</span><span class="sxs-lookup"><span data-stu-id="c682a-178">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="c682a-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="c682a-179">-Tag</span></span>
<span data-ttu-id="c682a-180">Теги, которые нужно связать с экземпляром</span><span class="sxs-lookup"><span data-stu-id="c682a-180">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="c682a-181">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="c682a-181">-TimezoneId</span></span>
<span data-ttu-id="c682a-182">Часовой пояс, который нужно установить в экземпляре.</span><span class="sxs-lookup"><span data-stu-id="c682a-182">The time zone id for the instance to set.</span></span> <span data-ttu-id="c682a-183">Список временных поясов можно просмотреть в представлении sys.time_zone_info Transact-SQL.</span><span class="sxs-lookup"><span data-stu-id="c682a-183">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="c682a-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="c682a-184">-VCore</span></span>
<span data-ttu-id="c682a-185">Определяет, сколько VCore нужно связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="c682a-185">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="c682a-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c682a-186">-Confirm</span></span>
<span data-ttu-id="c682a-187">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c682a-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c682a-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c682a-188">-WhatIf</span></span>
<span data-ttu-id="c682a-189">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c682a-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c682a-190">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c682a-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c682a-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c682a-191">CommonParameters</span></span>
<span data-ttu-id="c682a-192">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c682a-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c682a-193">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c682a-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c682a-194">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c682a-194">INPUTS</span></span>

### <span data-ttu-id="c682a-195">Нет</span><span class="sxs-lookup"><span data-stu-id="c682a-195">None</span></span>

## <span data-ttu-id="c682a-196">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c682a-196">OUTPUTS</span></span>

### <span data-ttu-id="c682a-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c682a-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="c682a-198">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c682a-198">NOTES</span></span>

## <span data-ttu-id="c682a-199">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c682a-199">RELATED LINKS</span></span>
