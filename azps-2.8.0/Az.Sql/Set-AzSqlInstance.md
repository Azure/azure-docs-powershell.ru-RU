---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: c08d2b1a08e76603af7125d0d4671643133699da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906425"
---
# <span data-ttu-id="6b15f-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6b15f-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="6b15f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b15f-102">SYNOPSIS</span></span>
<span data-ttu-id="6b15f-103">Задает свойства для управляемого экземпляра базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6b15f-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="6b15f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b15f-104">SYNTAX</span></span>

### <span data-ttu-id="6b15f-105">SetInstanceFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b15f-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b15f-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="6b15f-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b15f-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="6b15f-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b15f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b15f-108">DESCRIPTION</span></span>
<span data-ttu-id="6b15f-109">Командлет **Set-AzSqlInstance** изменяет свойства экземпляра Azure SQL, управляемого базой данных.</span><span class="sxs-lookup"><span data-stu-id="6b15f-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="6b15f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b15f-110">EXAMPLES</span></span>

### <span data-ttu-id="6b15f-111">Пример 1: Установка существующего экземпляра с использованием новых значений для параметров-AdministratorPassword,-LicenseType,-StorageSizeInGB и-VCore</span><span class="sxs-lookup"><span data-stu-id="6b15f-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="6b15f-112">Эта команда задает существующий экземпляр с использованием новых значений для параметров-AdministratorPassword,-LicenseType,-StorageSizeInGB и-VCore</span><span class="sxs-lookup"><span data-stu-id="6b15f-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="6b15f-113">Пример 2: Установка существующего экземпляра с использованием новых значений для параметров-AdministratorPassword,-LicenseType,-StorageSizeInGB и-VCore для экземпляра в пуле экземпляров</span><span class="sxs-lookup"><span data-stu-id="6b15f-113">Example 2: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="6b15f-114">Эта команда задает существующий экземпляр с использованием новых значений для параметров-AdministratorPassword,-LicenseType,-StorageSizeInGB и-VCore для экземпляра в пуле экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6b15f-114">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="6b15f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b15f-115">PARAMETERS</span></span>

### <span data-ttu-id="6b15f-116">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="6b15f-116">-AdministratorPassword</span></span>
<span data-ttu-id="6b15f-117">Новый пароль администратора SQL для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6b15f-117">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="6b15f-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6b15f-118">-AssignIdentity</span></span>
<span data-ttu-id="6b15f-119">Создавайте и назначайте удостоверение Azure Active Directory для этого экземпляра для использования в службах управления ключами, таких как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="6b15f-119">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="6b15f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b15f-120">-DefaultProfile</span></span>
<span data-ttu-id="6b15f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b15f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b15f-122">-Edition</span><span class="sxs-lookup"><span data-stu-id="6b15f-122">-Edition</span></span>
<span data-ttu-id="6b15f-123">Выпуск, назначаемый экземпляру.</span><span class="sxs-lookup"><span data-stu-id="6b15f-123">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="6b15f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6b15f-124">-Force</span></span>
<span data-ttu-id="6b15f-125">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="6b15f-125">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6b15f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b15f-126">-InputObject</span></span>
<span data-ttu-id="6b15f-127">Объект AzureSqlManagedInstanceModel, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6b15f-127">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="6b15f-128">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="6b15f-128">-InstancePoolName</span></span>
<span data-ttu-id="6b15f-129">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6b15f-129">The instance pool name.</span></span>

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

### <span data-ttu-id="6b15f-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6b15f-130">-LicenseType</span></span>
<span data-ttu-id="6b15f-131">Определяет, какой тип лицензии следует использовать.</span><span class="sxs-lookup"><span data-stu-id="6b15f-131">Determines which License Type to use.</span></span> <span data-ttu-id="6b15f-132">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6b15f-132">Possible values are:</span></span>
- <span data-ttu-id="6b15f-133">BasePrice — гибридное выгодное преимущество (AHB) для существующих владельцев лицензий SQL Server применяется скидка.</span><span class="sxs-lookup"><span data-stu-id="6b15f-133">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="6b15f-134">Служба управляемого экземпляра будет скидкам для существующих владельцев лицензий SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6b15f-134">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="6b15f-135">LicenseIncluded-(AHB) для существующих владельцев лицензий SQL Server не применяется скидка на гибридные льготы для использования в Azure.</span><span class="sxs-lookup"><span data-stu-id="6b15f-135">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="6b15f-136">Служба управляемого экземпляра будет включать в себя новые цены на лицензии SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6b15f-136">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="6b15f-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b15f-137">-Name</span></span>
<span data-ttu-id="6b15f-138">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6b15f-138">Instance name.</span></span>

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

### <span data-ttu-id="6b15f-139">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="6b15f-139">-ProxyOverride</span></span>
<span data-ttu-id="6b15f-140">Тип соединения, который используется для подключения к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="6b15f-140">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="6b15f-141">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="6b15f-141">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="6b15f-142">Включена ли конечная точка открытых данных для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6b15f-142">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="6b15f-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b15f-143">-ResourceGroupName</span></span>
<span data-ttu-id="6b15f-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b15f-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="6b15f-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b15f-145">-ResourceId</span></span>
<span data-ttu-id="6b15f-146">Идентификатор ресурса удаляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6b15f-146">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="6b15f-147">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="6b15f-147">-StorageSizeInGB</span></span>
<span data-ttu-id="6b15f-148">Определяет объем хранилища, связанного с экземпляром</span><span class="sxs-lookup"><span data-stu-id="6b15f-148">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="6b15f-149">-Тег</span><span class="sxs-lookup"><span data-stu-id="6b15f-149">-Tag</span></span>
<span data-ttu-id="6b15f-150">Теги, связываемые с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="6b15f-150">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="6b15f-151">-VCore</span><span class="sxs-lookup"><span data-stu-id="6b15f-151">-VCore</span></span>
<span data-ttu-id="6b15f-152">Определяет, сколько VCore связать с экземпляром</span><span class="sxs-lookup"><span data-stu-id="6b15f-152">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="6b15f-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b15f-153">-Confirm</span></span>
<span data-ttu-id="6b15f-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b15f-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b15f-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b15f-155">-WhatIf</span></span>
<span data-ttu-id="6b15f-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b15f-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b15f-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b15f-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b15f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b15f-158">CommonParameters</span></span>
<span data-ttu-id="6b15f-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b15f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b15f-160">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b15f-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b15f-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b15f-161">INPUTS</span></span>

### <span data-ttu-id="6b15f-162">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="6b15f-162">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="6b15f-163">System. String</span><span class="sxs-lookup"><span data-stu-id="6b15f-163">System.String</span></span>

## <span data-ttu-id="6b15f-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b15f-164">OUTPUTS</span></span>

### <span data-ttu-id="6b15f-165">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="6b15f-165">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="6b15f-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b15f-166">NOTES</span></span>

## <span data-ttu-id="6b15f-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b15f-167">RELATED LINKS</span></span>
