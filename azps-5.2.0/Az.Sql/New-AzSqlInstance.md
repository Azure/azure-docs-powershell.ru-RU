---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: ef809acdf8b78eb0d1203a901b3b44028c79733e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395719"
---
# <span data-ttu-id="40ba7-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="40ba7-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="40ba7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="40ba7-103">Создает экземпляр, управляемый базой SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="40ba7-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="40ba7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="40ba7-104">SYNTAX</span></span>

### <span data-ttu-id="40ba7-105">NewByEditionAndComputeGenerationParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40ba7-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ba7-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40ba7-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ba7-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40ba7-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ba7-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="40ba7-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40ba7-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40ba7-109">DESCRIPTION</span></span>
<span data-ttu-id="40ba7-110">С **его использованием** создается экземпляр Azure SQL Database Managed.</span><span class="sxs-lookup"><span data-stu-id="40ba7-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="40ba7-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="40ba7-111">EXAMPLES</span></span>

### <span data-ttu-id="40ba7-112">Пример 1. Создание экземпляра</span><span class="sxs-lookup"><span data-stu-id="40ba7-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="40ba7-113">Эта команда создает новый экземпляр с использованием параметра SkuName.</span><span class="sxs-lookup"><span data-stu-id="40ba7-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="40ba7-114">Пример 2. Создание экземпляра</span><span class="sxs-lookup"><span data-stu-id="40ba7-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="40ba7-115">Эта команда создает новый экземпляр с использованием параметров Edition и ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="40ba7-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="40ba7-116">Пример 3. Создание экземпляра в пуле экземпляров с помощью объекта пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="40ba7-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="40ba7-117">Эта команда создает новый экземпляр в пуле экземпляров с использованием объекта пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="40ba7-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="40ba7-118">Пример 4. Создание экземпляра в пуле экземпляров с помощью идентификатора ресурса пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="40ba7-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="40ba7-119">Эта команда создает новый экземпляр в пуле экземпляров с использованием идентификатора ресурса пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="40ba7-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="40ba7-120">Пример 5. Создание экземпляра в пуле экземпляров</span><span class="sxs-lookup"><span data-stu-id="40ba7-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="40ba7-121">Эта команда создает новый экземпляр в пуле экземпляров с экземпляром InstancePool0</span><span class="sxs-lookup"><span data-stu-id="40ba7-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="40ba7-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40ba7-122">PARAMETERS</span></span>

### <span data-ttu-id="40ba7-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="40ba7-123">-AdministratorCredential</span></span>
<span data-ttu-id="40ba7-124">Учетные SQL проверки подлинности экземпляра.</span><span class="sxs-lookup"><span data-stu-id="40ba7-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="40ba7-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40ba7-125">-AsJob</span></span>
<span data-ttu-id="40ba7-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="40ba7-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40ba7-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="40ba7-127">-AssignIdentity</span></span>
<span data-ttu-id="40ba7-128">Создание и назначение удостоверения Azure Active Directory для этого экземпляра Managed для использования с ключевыми службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="40ba7-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="40ba7-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="40ba7-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="40ba7-130">Избыточность резервного копирования хранилища, используемого для хранения резервных копий управляемого экземпляра Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="40ba7-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="40ba7-131">Возможные варианты: Local (Локальный), Zone (Зона) и Geo (География)</span><span class="sxs-lookup"><span data-stu-id="40ba7-131">Options are: Local, Zone and Geo</span></span>

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

### <span data-ttu-id="40ba7-132">-Collation</span><span class="sxs-lookup"><span data-stu-id="40ba7-132">-Collation</span></span>
<span data-ttu-id="40ba7-133">Разлиновка управляемого экземпляра Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="40ba7-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="40ba7-134">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="40ba7-134">-ComputeGeneration</span></span>
<span data-ttu-id="40ba7-135">The compute generation for the instance.</span><span class="sxs-lookup"><span data-stu-id="40ba7-135">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="40ba7-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ba7-136">-DefaultProfile</span></span>
<span data-ttu-id="40ba7-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40ba7-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40ba7-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="40ba7-138">-DnsZonePartner</span></span>
<span data-ttu-id="40ba7-139">ИД ресурса управляемого сервера партнера, который наследует свойство DnsZone от экземпляра Managed</span><span class="sxs-lookup"><span data-stu-id="40ba7-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="40ba7-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="40ba7-140">-Edition</span></span>
<span data-ttu-id="40ba7-141">Выпуск для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="40ba7-141">The edition for the instance.</span></span>

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

### <span data-ttu-id="40ba7-142">-Force</span><span class="sxs-lookup"><span data-stu-id="40ba7-142">-Force</span></span>
<span data-ttu-id="40ba7-143">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="40ba7-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="40ba7-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="40ba7-144">-InstancePool</span></span>
<span data-ttu-id="40ba7-145">Родительский объект пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="40ba7-145">The instance pool parent object.</span></span>

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

### <span data-ttu-id="40ba7-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="40ba7-146">-InstancePoolName</span></span>
<span data-ttu-id="40ba7-147">Пул экземпляров для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="40ba7-147">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="40ba7-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="40ba7-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="40ba7-149">ИД пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="40ba7-149">The instance pool resource id.</span></span>

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

### <span data-ttu-id="40ba7-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="40ba7-150">-LicenseType</span></span>
<span data-ttu-id="40ba7-151">Определяет тип лицензии.</span><span class="sxs-lookup"><span data-stu-id="40ba7-151">Determines which License Type to use.</span></span> <span data-ttu-id="40ba7-152">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="40ba7-152">Possible values are:</span></span>
- <span data-ttu-id="40ba7-153">BasePrice — скидка на Azure Hybrid Benefit (AHB) для существующих SQL Server лицензий применяется.</span><span class="sxs-lookup"><span data-stu-id="40ba7-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="40ba7-154">Для существующих владельцев лицензий на управляемый экземпляр скидка SQL Server.</span><span class="sxs-lookup"><span data-stu-id="40ba7-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="40ba7-155">LicenseIncluded — скидка на azure Hybrid Benefit (AHB) для существующих SQL Server лицензий не применяется.</span><span class="sxs-lookup"><span data-stu-id="40ba7-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="40ba7-156">Стоимость услуги Managed Instance будет включать новую стоимость SQL Server стоимостью лицензий.</span><span class="sxs-lookup"><span data-stu-id="40ba7-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="40ba7-157">-Location</span><span class="sxs-lookup"><span data-stu-id="40ba7-157">-Location</span></span>
<span data-ttu-id="40ba7-158">Расположение для создания экземпляра</span><span class="sxs-lookup"><span data-stu-id="40ba7-158">The location in which to create the instance</span></span>

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

### <span data-ttu-id="40ba7-159">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="40ba7-159">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="40ba7-160">Конфигурация обслуживания для управляемого экземпляра Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="40ba7-160">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="40ba7-161">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="40ba7-161">-MinimalTlsVersion</span></span>
<span data-ttu-id="40ba7-162">Минимальная версия TLS, которая будет применяться для управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="40ba7-162">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="40ba7-163">-Name</span><span class="sxs-lookup"><span data-stu-id="40ba7-163">-Name</span></span>
<span data-ttu-id="40ba7-164">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="40ba7-164">Instance name.</span></span>

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

### <span data-ttu-id="40ba7-165">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="40ba7-165">-ProxyOverride</span></span>
<span data-ttu-id="40ba7-166">Тип подключения, используемый для подключения к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="40ba7-166">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="40ba7-167">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="40ba7-167">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="40ba7-168">Включена ли конечная точка общедоступных данных для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="40ba7-168">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="40ba7-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40ba7-169">-ResourceGroupName</span></span>
<span data-ttu-id="40ba7-170">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40ba7-170">The name of the resource group.</span></span>

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

### <span data-ttu-id="40ba7-171">-SkuName</span><span class="sxs-lookup"><span data-stu-id="40ba7-171">-SkuName</span></span>
<span data-ttu-id="40ba7-172">Имя SKU экземпляра, например "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="40ba7-172">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="40ba7-173">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="40ba7-173">-StorageSizeInGB</span></span>
<span data-ttu-id="40ba7-174">Определяет размер хранилища, который нужно связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="40ba7-174">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="40ba7-175">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="40ba7-175">-SubnetId</span></span>
<span data-ttu-id="40ba7-176">ИД подсети, который нужно использовать для создания экземпляра</span><span class="sxs-lookup"><span data-stu-id="40ba7-176">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="40ba7-177">-Tag</span><span class="sxs-lookup"><span data-stu-id="40ba7-177">-Tag</span></span>
<span data-ttu-id="40ba7-178">Теги, которые нужно связать с экземпляром</span><span class="sxs-lookup"><span data-stu-id="40ba7-178">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="40ba7-179">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="40ba7-179">-TimezoneId</span></span>
<span data-ttu-id="40ba7-180">Часовой пояс, который нужно установить в экземпляре.</span><span class="sxs-lookup"><span data-stu-id="40ba7-180">The time zone id for the instance to set.</span></span> <span data-ttu-id="40ba7-181">Список временных поясов можно просмотреть в представлении sys.time_zone_info Transact-SQL.</span><span class="sxs-lookup"><span data-stu-id="40ba7-181">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="40ba7-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="40ba7-182">-VCore</span></span>
<span data-ttu-id="40ba7-183">Определяет, сколько VCore нужно связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="40ba7-183">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="40ba7-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40ba7-184">-Confirm</span></span>
<span data-ttu-id="40ba7-185">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="40ba7-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40ba7-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40ba7-186">-WhatIf</span></span>
<span data-ttu-id="40ba7-187">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40ba7-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40ba7-188">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="40ba7-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40ba7-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ba7-189">CommonParameters</span></span>
<span data-ttu-id="40ba7-190">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40ba7-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ba7-191">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40ba7-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ba7-192">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40ba7-192">INPUTS</span></span>

### <span data-ttu-id="40ba7-193">Нет</span><span class="sxs-lookup"><span data-stu-id="40ba7-193">None</span></span>

## <span data-ttu-id="40ba7-194">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="40ba7-194">OUTPUTS</span></span>

### <span data-ttu-id="40ba7-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="40ba7-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="40ba7-196">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="40ba7-196">NOTES</span></span>

## <span data-ttu-id="40ba7-197">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40ba7-197">RELATED LINKS</span></span>
