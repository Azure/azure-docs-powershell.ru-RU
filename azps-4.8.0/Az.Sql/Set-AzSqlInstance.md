---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: e17c6b226f7ed4fe17842c93d03828d53c0bb22c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235773"
---
# <span data-ttu-id="6e6cd-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6e6cd-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="6e6cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="6e6cd-103">Задает свойства для управляемого экземпляра базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="6e6cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e6cd-104">SYNTAX</span></span>

### <span data-ttu-id="6e6cd-105">SetInstanceFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e6cd-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e6cd-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="6e6cd-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e6cd-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="6e6cd-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e6cd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e6cd-108">DESCRIPTION</span></span>
<span data-ttu-id="6e6cd-109">Командлет **Set-AzSqlInstance** изменяет свойства экземпляра Azure SQL, управляемого базой данных.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="6e6cd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e6cd-110">EXAMPLES</span></span>

### <span data-ttu-id="6e6cd-111">Пример 1: Установка существующего экземпляра с использованием новых значений для параметров-AdministratorPassword,-LicenseType и-StorageSizeInGB,-VCore и-Edition</span><span class="sxs-lookup"><span data-stu-id="6e6cd-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="6e6cd-112">Пример 2: изменение существующего экземпляра аппаратного поколения с новым значением параметра-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="6e6cd-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="6e6cd-113">Эта команда задает существующий экземпляр с использованием новых значений для параметров-AdministratorPassword,-LicenseType,-StorageSizeInGB и-VCore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="6e6cd-114">Пример 3: Установка существующего экземпляра с использованием новых значений для параметров-AdministratorPassword,-LicenseType,-StorageSizeInGB и-VCore для экземпляра в пуле экземпляров</span><span class="sxs-lookup"><span data-stu-id="6e6cd-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="6e6cd-115">Эта команда задает существующий экземпляр с использованием новых значений для параметров-AdministratorPassword,-LicenseType,-StorageSizeInGB и-VCore для экземпляра в пуле экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="6e6cd-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e6cd-116">PARAMETERS</span></span>

### <span data-ttu-id="6e6cd-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="6e6cd-117">-AdministratorPassword</span></span>
<span data-ttu-id="6e6cd-118">Новый пароль администратора SQL для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="6e6cd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e6cd-119">-AsJob</span></span>
<span data-ttu-id="6e6cd-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6e6cd-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e6cd-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6e6cd-121">-AssignIdentity</span></span>
<span data-ttu-id="6e6cd-122">Создавайте и назначайте удостоверение Azure Active Directory для этого экземпляра для использования в службах управления ключами, таких как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="6e6cd-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="6e6cd-123">-ComputeGeneration</span></span>
<span data-ttu-id="6e6cd-124">Вычисленое поколение для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="6e6cd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e6cd-125">-DefaultProfile</span></span>
<span data-ttu-id="6e6cd-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e6cd-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="6e6cd-127">-Edition</span></span>
<span data-ttu-id="6e6cd-128">Выпуск, назначаемый экземпляру.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="6e6cd-129">-Force</span><span class="sxs-lookup"><span data-stu-id="6e6cd-129">-Force</span></span>
<span data-ttu-id="6e6cd-130">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="6e6cd-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6e6cd-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e6cd-131">-InputObject</span></span>
<span data-ttu-id="6e6cd-132">Объект AzureSqlManagedInstanceModel, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="6e6cd-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="6e6cd-133">-InstancePoolName</span></span>
<span data-ttu-id="6e6cd-134">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-134">The instance pool name.</span></span>

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

### <span data-ttu-id="6e6cd-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6e6cd-135">-LicenseType</span></span>
<span data-ttu-id="6e6cd-136">Определяет, какой тип лицензии следует использовать.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-136">Determines which License Type to use.</span></span> <span data-ttu-id="6e6cd-137">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6e6cd-137">Possible values are:</span></span>
- <span data-ttu-id="6e6cd-138">BasePrice — гибридное выгодное преимущество (AHB) для существующих владельцев лицензий SQL Server применяется скидка.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="6e6cd-139">Служба управляемого экземпляра будет скидкам для существующих владельцев лицензий SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="6e6cd-140">LicenseIncluded-(AHB) для существующих владельцев лицензий SQL Server не применяется скидка на гибридные льготы для использования в Azure.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="6e6cd-141">Служба управляемого экземпляра будет включать в себя новые цены на лицензии SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="6e6cd-142">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="6e6cd-142">-MinimalTlsVersion</span></span>
<span data-ttu-id="6e6cd-143">Минимальная версия TLS для обеспечения управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="6e6cd-143">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="6e6cd-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6e6cd-144">-Name</span></span>
<span data-ttu-id="6e6cd-145">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-145">Instance name.</span></span>

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

### <span data-ttu-id="6e6cd-146">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="6e6cd-146">-ProxyOverride</span></span>
<span data-ttu-id="6e6cd-147">Тип соединения, который используется для подключения к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-147">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="6e6cd-148">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="6e6cd-148">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="6e6cd-149">Включена ли конечная точка открытых данных для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-149">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="6e6cd-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e6cd-150">-ResourceGroupName</span></span>
<span data-ttu-id="6e6cd-151">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="6e6cd-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e6cd-152">-ResourceId</span></span>
<span data-ttu-id="6e6cd-153">Идентификатор ресурса удаляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-153">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="6e6cd-154">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="6e6cd-154">-StorageSizeInGB</span></span>
<span data-ttu-id="6e6cd-155">Определяет объем хранилища, связанного с экземпляром</span><span class="sxs-lookup"><span data-stu-id="6e6cd-155">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="6e6cd-156">-Тег</span><span class="sxs-lookup"><span data-stu-id="6e6cd-156">-Tag</span></span>
<span data-ttu-id="6e6cd-157">Теги, связываемые с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-157">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="6e6cd-158">-VCore</span><span class="sxs-lookup"><span data-stu-id="6e6cd-158">-VCore</span></span>
<span data-ttu-id="6e6cd-159">Определяет, сколько VCore связать с экземпляром</span><span class="sxs-lookup"><span data-stu-id="6e6cd-159">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="6e6cd-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e6cd-160">-Confirm</span></span>
<span data-ttu-id="6e6cd-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e6cd-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e6cd-162">-WhatIf</span></span>
<span data-ttu-id="6e6cd-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e6cd-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e6cd-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e6cd-165">CommonParameters</span></span>
<span data-ttu-id="6e6cd-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e6cd-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e6cd-167">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e6cd-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e6cd-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e6cd-168">INPUTS</span></span>

### <span data-ttu-id="6e6cd-169">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="6e6cd-169">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="6e6cd-170">System. String</span><span class="sxs-lookup"><span data-stu-id="6e6cd-170">System.String</span></span>

## <span data-ttu-id="6e6cd-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e6cd-171">OUTPUTS</span></span>

### <span data-ttu-id="6e6cd-172">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="6e6cd-172">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="6e6cd-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e6cd-173">NOTES</span></span>

## <span data-ttu-id="6e6cd-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e6cd-174">RELATED LINKS</span></span>
