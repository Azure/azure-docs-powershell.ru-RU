---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: f16e6f2dcbcf3ebd16926784ca84eef02740df7b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506633"
---
# <span data-ttu-id="4d822-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4d822-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="4d822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d822-102">SYNOPSIS</span></span>
<span data-ttu-id="4d822-103">Задает свойства экземпляра, управляемого базой SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4d822-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="4d822-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4d822-104">SYNTAX</span></span>

### <span data-ttu-id="4d822-105">SetInstanceFromInputParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4d822-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d822-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="4d822-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d822-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="4d822-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d822-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d822-108">DESCRIPTION</span></span>
<span data-ttu-id="4d822-109">Cmdlet **Set-AzSqlInstance** изменяет свойства экземпляра Azure SQL Database Managed.</span><span class="sxs-lookup"><span data-stu-id="4d822-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="4d822-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4d822-110">EXAMPLES</span></span>

### <span data-ttu-id="4d822-111">Пример 1. Настройка существующего экземпляра с использованием новых значений для -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore и -Edition</span><span class="sxs-lookup"><span data-stu-id="4d822-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="4d822-112">Пример 2. Изменение существующего оборудования экземпляра с использованием нового значения для -ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="4d822-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="4d822-113">Эта команда задает существующий экземпляр, используя новые значения для -AdministratorPassword, -LicenseType, -StorageSizeInGB и -VCore.</span><span class="sxs-lookup"><span data-stu-id="4d822-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="4d822-114">Пример 3. Настройка существующего экземпляра с использованием новых значений для -AdministratorPassword, -LicenseType, -StorageSizeInGB и -VCore для экземпляра в пуле экземпляров</span><span class="sxs-lookup"><span data-stu-id="4d822-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="4d822-115">Эта команда задает существующий экземпляр, используя новые значения для -AdministratorPassword, -LicenseType, -StorageSizeInGB и -VCore для экземпляра в пуле экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4d822-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="4d822-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d822-116">PARAMETERS</span></span>

### <span data-ttu-id="4d822-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="4d822-117">-AdministratorPassword</span></span>
<span data-ttu-id="4d822-118">Новый пароль SQL администратора для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4d822-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="4d822-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d822-119">-AsJob</span></span>
<span data-ttu-id="4d822-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4d822-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d822-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4d822-121">-AssignIdentity</span></span>
<span data-ttu-id="4d822-122">Создание и назначение удостоверения Azure Active Directory для этого экземпляра для использования с ключевыми службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="4d822-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="4d822-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="4d822-123">-ComputeGeneration</span></span>
<span data-ttu-id="4d822-124">The compute generation for the instance.</span><span class="sxs-lookup"><span data-stu-id="4d822-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="4d822-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d822-125">-DefaultProfile</span></span>
<span data-ttu-id="4d822-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d822-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d822-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="4d822-127">-Edition</span></span>
<span data-ttu-id="4d822-128">Выпуск, который нужно назначить экземпляру.</span><span class="sxs-lookup"><span data-stu-id="4d822-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="4d822-129">-Force</span><span class="sxs-lookup"><span data-stu-id="4d822-129">-Force</span></span>
<span data-ttu-id="4d822-130">Пропустить сообщение подтверждения для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="4d822-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="4d822-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d822-131">-InputObject</span></span>
<span data-ttu-id="4d822-132">Объект AzureSqlManagedInstanceModel, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="4d822-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="4d822-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="4d822-133">-InstancePoolName</span></span>
<span data-ttu-id="4d822-134">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4d822-134">The instance pool name.</span></span>

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

### <span data-ttu-id="4d822-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4d822-135">-LicenseType</span></span>
<span data-ttu-id="4d822-136">Определяет тип лицензии.</span><span class="sxs-lookup"><span data-stu-id="4d822-136">Determines which License Type to use.</span></span> <span data-ttu-id="4d822-137">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="4d822-137">Possible values are:</span></span>
- <span data-ttu-id="4d822-138">BasePrice — скидка на гибридное преимущество Azure (AHB) для существующих SQL Server лицензий применяется.</span><span class="sxs-lookup"><span data-stu-id="4d822-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="4d822-139">Для существующих владельцев лицензий на управляемый экземпляр скидка SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4d822-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="4d822-140">LicenseIncluded — скидка на azure Hybrid Benefit (AHB) для существующих SQL Server лицензий не применяется.</span><span class="sxs-lookup"><span data-stu-id="4d822-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="4d822-141">Стоимость услуги Managed Instance будет включать новую стоимость SQL Server стоимостью лицензии.</span><span class="sxs-lookup"><span data-stu-id="4d822-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="4d822-142">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4d822-142">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="4d822-143">Конфигурация обслуживания для управляемого экземпляра Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="4d822-143">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="4d822-144">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4d822-144">-MinimalTlsVersion</span></span>
<span data-ttu-id="4d822-145">Минимальная версия TLS, которая будет применяться для управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="4d822-145">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="4d822-146">-Name</span><span class="sxs-lookup"><span data-stu-id="4d822-146">-Name</span></span>
<span data-ttu-id="4d822-147">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4d822-147">Instance name.</span></span>

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

### <span data-ttu-id="4d822-148">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="4d822-148">-ProxyOverride</span></span>
<span data-ttu-id="4d822-149">Тип подключения, используемый для подключения к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="4d822-149">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="4d822-150">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="4d822-150">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="4d822-151">Включена ли конечная точка общедоступных данных для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4d822-151">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="4d822-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d822-152">-ResourceGroupName</span></span>
<span data-ttu-id="4d822-153">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d822-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d822-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d822-154">-ResourceId</span></span>
<span data-ttu-id="4d822-155">ИД ресурса экземпляра, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="4d822-155">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="4d822-156">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="4d822-156">-StorageSizeInGB</span></span>
<span data-ttu-id="4d822-157">Определяет размер хранилища, который нужно связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="4d822-157">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="4d822-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="4d822-158">-Tag</span></span>
<span data-ttu-id="4d822-159">Теги, которые нужно связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="4d822-159">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="4d822-160">-VCore</span><span class="sxs-lookup"><span data-stu-id="4d822-160">-VCore</span></span>
<span data-ttu-id="4d822-161">Определяет, сколько VCore нужно связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="4d822-161">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="4d822-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d822-162">-Confirm</span></span>
<span data-ttu-id="4d822-163">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4d822-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d822-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d822-164">-WhatIf</span></span>
<span data-ttu-id="4d822-165">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d822-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d822-166">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4d822-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d822-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d822-167">CommonParameters</span></span>
<span data-ttu-id="4d822-168">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d822-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d822-169">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d822-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d822-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d822-170">INPUTS</span></span>

### <span data-ttu-id="4d822-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4d822-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="4d822-172">System.String</span><span class="sxs-lookup"><span data-stu-id="4d822-172">System.String</span></span>

## <span data-ttu-id="4d822-173">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4d822-173">OUTPUTS</span></span>

### <span data-ttu-id="4d822-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4d822-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="4d822-175">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4d822-175">NOTES</span></span>

## <span data-ttu-id="4d822-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d822-176">RELATED LINKS</span></span>
