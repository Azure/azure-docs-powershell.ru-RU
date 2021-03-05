---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: a6dd059b7fdab3c2670e3b8902def148d88124d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015864"
---
# <span data-ttu-id="92eda-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="92eda-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="92eda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92eda-102">SYNOPSIS</span></span>
<span data-ttu-id="92eda-103">Задает свойства экземпляра, управляемого базой SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="92eda-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="92eda-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92eda-104">SYNTAX</span></span>

### <span data-ttu-id="92eda-105">SetInstanceFromInputParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92eda-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92eda-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="92eda-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92eda-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="92eda-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92eda-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92eda-108">DESCRIPTION</span></span>
<span data-ttu-id="92eda-109">Cmdlet **Set-AzSqlInstance** изменяет свойства экземпляра Azure SQL Database Managed.</span><span class="sxs-lookup"><span data-stu-id="92eda-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="92eda-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92eda-110">EXAMPLES</span></span>

### <span data-ttu-id="92eda-111">Пример 1. Настройка существующего экземпляра с использованием новых значений для -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore и -Edition</span><span class="sxs-lookup"><span data-stu-id="92eda-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition BusinessCritical
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
InstancePoolName         :
```

### <span data-ttu-id="92eda-112">Пример 2. Изменение существующего оборудования экземпляра с использованием нового значения для -ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="92eda-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -ComputeGeneration Gen5
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
InstancePoolName         :
```

<span data-ttu-id="92eda-113">Эта команда задает существующий экземпляр, используя новые значения для -AdministratorPassword, -LicenseType, -StorageSizeInGB и -VCore.</span><span class="sxs-lookup"><span data-stu-id="92eda-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="92eda-114">Пример 3. Настройка существующего экземпляра с использованием новых значений для -AdministratorPassword, -LicenseType, -StorageSizeInGB и -VCore для экземпляра в пуле экземпляров</span><span class="sxs-lookup"><span data-stu-id="92eda-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolName instancePool0
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
StorageSizeInGB          : 1024
InstancePoolName         : instancePool0
```

<span data-ttu-id="92eda-115">Эта команда задает существующий экземпляр, используя новые значения для -AdministratorPassword, -LicenseType, -StorageSizeInGB и -VCore для экземпляра в пуле экземпляров.</span><span class="sxs-lookup"><span data-stu-id="92eda-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

### <span data-ttu-id="92eda-116">Пример 4. Обновление конфигурации обслуживания для существующего экземпляра</span><span class="sxs-lookup"><span data-stu-id="92eda-116">Example 4: Update maintenance configuration for existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
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

<span data-ttu-id="92eda-117">Эта команда обновляет существующий экземпляр с конфигурацией обслуживания MI_2</span><span class="sxs-lookup"><span data-stu-id="92eda-117">This command updates existing instance with maintenance configuration MI_2</span></span>

### <span data-ttu-id="92eda-118">Пример 5. Удаление конфигурации обслуживания из существующего экземпляра</span><span class="sxs-lookup"><span data-stu-id="92eda-118">Example 5: Remove maintenance configuration from existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managediInstance1" -ResourceGroupName "Resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default"
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
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default
```

<span data-ttu-id="92eda-119">Эта команда сбрасывает конфигурацию обслуживания до значения по умолчанию для существующего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="92eda-119">This command resets maintenance configuration to default for existing instance</span></span>

## <span data-ttu-id="92eda-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92eda-120">PARAMETERS</span></span>

### <span data-ttu-id="92eda-121">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="92eda-121">-AdministratorPassword</span></span>
<span data-ttu-id="92eda-122">Новый пароль SQL администратора для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="92eda-122">The new SQL administrator password for the instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92eda-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92eda-123">-AsJob</span></span>
<span data-ttu-id="92eda-124">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="92eda-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92eda-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="92eda-125">-AssignIdentity</span></span>
<span data-ttu-id="92eda-126">Создание и назначение удостоверения Azure Active Directory для этого экземпляра для использования с ключевыми службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="92eda-126">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="92eda-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="92eda-127">-ComputeGeneration</span></span>
<span data-ttu-id="92eda-128">The compute generation for the instance.</span><span class="sxs-lookup"><span data-stu-id="92eda-128">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="92eda-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92eda-129">-DefaultProfile</span></span>
<span data-ttu-id="92eda-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92eda-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92eda-131">-Edition</span><span class="sxs-lookup"><span data-stu-id="92eda-131">-Edition</span></span>
<span data-ttu-id="92eda-132">Выпуск, который нужно назначить экземпляру.</span><span class="sxs-lookup"><span data-stu-id="92eda-132">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="92eda-133">-Force</span><span class="sxs-lookup"><span data-stu-id="92eda-133">-Force</span></span>
<span data-ttu-id="92eda-134">Пропустить сообщение подтверждения для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="92eda-134">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="92eda-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92eda-135">-InputObject</span></span>
<span data-ttu-id="92eda-136">Объект AzureSqlManagedInstanceModel, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="92eda-136">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92eda-137">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="92eda-137">-InstancePoolName</span></span>
<span data-ttu-id="92eda-138">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="92eda-138">The instance pool name.</span></span>

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

### <span data-ttu-id="92eda-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="92eda-139">-LicenseType</span></span>
<span data-ttu-id="92eda-140">Определяет тип лицензии.</span><span class="sxs-lookup"><span data-stu-id="92eda-140">Determines which License Type to use.</span></span> <span data-ttu-id="92eda-141">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="92eda-141">Possible values are:</span></span>
- <span data-ttu-id="92eda-142">BasePrice — скидка на Azure Hybrid Benefit (AHB) для существующих SQL Server лицензий применяется.</span><span class="sxs-lookup"><span data-stu-id="92eda-142">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="92eda-143">Для существующих владельцев лицензий на управляемый экземпляр скидка SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92eda-143">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="92eda-144">LicenseIncluded — скидка на azure Hybrid Benefit (AHB) для существующих SQL Server лицензий не применяется.</span><span class="sxs-lookup"><span data-stu-id="92eda-144">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="92eda-145">Стоимость услуги Managed Instance будет включать новую стоимость SQL Server лицензий.</span><span class="sxs-lookup"><span data-stu-id="92eda-145">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="92eda-146">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="92eda-146">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="92eda-147">Конфигурация обслуживания для управляемого экземпляра Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="92eda-147">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="92eda-148">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="92eda-148">-MinimalTlsVersion</span></span>
<span data-ttu-id="92eda-149">Минимальная версия TLS, которая будет применяться для управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="92eda-149">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="92eda-150">-Name</span><span class="sxs-lookup"><span data-stu-id="92eda-150">-Name</span></span>
<span data-ttu-id="92eda-151">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="92eda-151">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92eda-152">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="92eda-152">-ProxyOverride</span></span>
<span data-ttu-id="92eda-153">Тип подключения, используемый для подключения к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="92eda-153">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="92eda-154">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="92eda-154">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="92eda-155">Включена ли конечная точка общедоступных данных для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="92eda-155">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92eda-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92eda-156">-ResourceGroupName</span></span>
<span data-ttu-id="92eda-157">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92eda-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92eda-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92eda-158">-ResourceId</span></span>
<span data-ttu-id="92eda-159">ИД ресурса экземпляра, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="92eda-159">The resource id of instance to remove</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92eda-160">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="92eda-160">-StorageSizeInGB</span></span>
<span data-ttu-id="92eda-161">Определяет размер хранилища, который нужно связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="92eda-161">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92eda-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="92eda-162">-Tag</span></span>
<span data-ttu-id="92eda-163">Теги, которые нужно связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="92eda-163">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="92eda-164">-VCore</span><span class="sxs-lookup"><span data-stu-id="92eda-164">-VCore</span></span>
<span data-ttu-id="92eda-165">Определяет, сколько VCore нужно связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="92eda-165">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92eda-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92eda-166">-Confirm</span></span>
<span data-ttu-id="92eda-167">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="92eda-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92eda-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92eda-168">-WhatIf</span></span>
<span data-ttu-id="92eda-169">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92eda-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92eda-170">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="92eda-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92eda-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92eda-171">CommonParameters</span></span>
<span data-ttu-id="92eda-172">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92eda-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92eda-173">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92eda-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92eda-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92eda-174">INPUTS</span></span>

### <span data-ttu-id="92eda-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="92eda-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="92eda-176">System.String</span><span class="sxs-lookup"><span data-stu-id="92eda-176">System.String</span></span>

## <span data-ttu-id="92eda-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92eda-177">OUTPUTS</span></span>

### <span data-ttu-id="92eda-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="92eda-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="92eda-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92eda-179">NOTES</span></span>

## <span data-ttu-id="92eda-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92eda-180">RELATED LINKS</span></span>
