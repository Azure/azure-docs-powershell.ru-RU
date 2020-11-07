---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: ad98b764eac08c9fb1f6d3dd367d78ca1b5d45d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728772"
---
# <span data-ttu-id="44ae9-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="44ae9-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="44ae9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="44ae9-103">Задает свойства для управляемого экземпляра базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="44ae9-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="44ae9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44ae9-104">SYNTAX</span></span>

### <span data-ttu-id="44ae9-105">SetInstanceFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44ae9-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44ae9-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="44ae9-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44ae9-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="44ae9-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44ae9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44ae9-108">DESCRIPTION</span></span>
<span data-ttu-id="44ae9-109">Командлет **Set-AzSqlInstance** изменяет свойства экземпляра Azure SQL, управляемого базой данных.</span><span class="sxs-lookup"><span data-stu-id="44ae9-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="44ae9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44ae9-110">EXAMPLES</span></span>

### <span data-ttu-id="44ae9-111">Пример 1: Установка существующего экземпляра с использованием новых значений для параметров-AdministratorPassword,-LicenseType,-StorageSizeInGB и-VCore</span><span class="sxs-lookup"><span data-stu-id="44ae9-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```
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
```

<span data-ttu-id="44ae9-112">Эта команда задает существующий экземпляр с использованием новых значений для параметров-AdministratorPassword,-LicenseType,-StorageSizeInGB и-VCore</span><span class="sxs-lookup"><span data-stu-id="44ae9-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

## <span data-ttu-id="44ae9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44ae9-113">PARAMETERS</span></span>

### <span data-ttu-id="44ae9-114">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="44ae9-114">-AdministratorPassword</span></span>
<span data-ttu-id="44ae9-115">Новый пароль администратора SQL для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="44ae9-115">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="44ae9-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="44ae9-116">-AssignIdentity</span></span>
<span data-ttu-id="44ae9-117">Создавайте и назначайте удостоверение Azure Active Directory для этого экземпляра для использования в службах управления ключами, таких как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="44ae9-117">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="44ae9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ae9-118">-DefaultProfile</span></span>
<span data-ttu-id="44ae9-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44ae9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44ae9-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="44ae9-120">-Edition</span></span>
<span data-ttu-id="44ae9-121">Выпуск, назначаемый экземпляру.</span><span class="sxs-lookup"><span data-stu-id="44ae9-121">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="44ae9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="44ae9-122">-Force</span></span>
<span data-ttu-id="44ae9-123">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="44ae9-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="44ae9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44ae9-124">-InputObject</span></span>
<span data-ttu-id="44ae9-125">Объект AzureSqlManagedInstanceModel, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="44ae9-125">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="44ae9-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="44ae9-126">-LicenseType</span></span>
<span data-ttu-id="44ae9-127">Определяет, какой тип лицензии следует использовать.</span><span class="sxs-lookup"><span data-stu-id="44ae9-127">Determines which License Type to use.</span></span> <span data-ttu-id="44ae9-128">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="44ae9-128">Possible values are:</span></span>
- <span data-ttu-id="44ae9-129">BasePrice — гибридное выгодное преимущество (AHB) для существующих владельцев лицензий SQL Server применяется скидка.</span><span class="sxs-lookup"><span data-stu-id="44ae9-129">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="44ae9-130">Служба управляемого экземпляра будет скидкам для существующих владельцев лицензий SQL Server.</span><span class="sxs-lookup"><span data-stu-id="44ae9-130">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="44ae9-131">LicenseIncluded-(AHB) для существующих владельцев лицензий SQL Server не применяется скидка на гибридные льготы для использования в Azure.</span><span class="sxs-lookup"><span data-stu-id="44ae9-131">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="44ae9-132">Служба управляемого экземпляра будет включать в себя новые цены на лицензии SQL Server.</span><span class="sxs-lookup"><span data-stu-id="44ae9-132">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="44ae9-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44ae9-133">-Name</span></span>
<span data-ttu-id="44ae9-134">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="44ae9-134">Instance name.</span></span>

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

### <span data-ttu-id="44ae9-135">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="44ae9-135">-ProxyOverride</span></span>
<span data-ttu-id="44ae9-136">Тип соединения, который используется для подключения к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="44ae9-136">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="44ae9-137">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="44ae9-137">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="44ae9-138">Включена ли конечная точка открытых данных для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="44ae9-138">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="44ae9-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44ae9-139">-ResourceGroupName</span></span>
<span data-ttu-id="44ae9-140">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44ae9-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="44ae9-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44ae9-141">-ResourceId</span></span>
<span data-ttu-id="44ae9-142">Идентификатор ресурса удаляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="44ae9-142">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="44ae9-143">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="44ae9-143">-StorageSizeInGB</span></span>
<span data-ttu-id="44ae9-144">Определяет объем хранилища, связанного с экземпляром</span><span class="sxs-lookup"><span data-stu-id="44ae9-144">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="44ae9-145">-Тег</span><span class="sxs-lookup"><span data-stu-id="44ae9-145">-Tag</span></span>
<span data-ttu-id="44ae9-146">Теги, связываемые с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="44ae9-146">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="44ae9-147">-VCore</span><span class="sxs-lookup"><span data-stu-id="44ae9-147">-VCore</span></span>
<span data-ttu-id="44ae9-148">Определяет, сколько VCore связать с экземпляром</span><span class="sxs-lookup"><span data-stu-id="44ae9-148">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="44ae9-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44ae9-149">-Confirm</span></span>
<span data-ttu-id="44ae9-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="44ae9-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44ae9-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44ae9-151">-WhatIf</span></span>
<span data-ttu-id="44ae9-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="44ae9-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44ae9-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="44ae9-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44ae9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ae9-154">CommonParameters</span></span>
<span data-ttu-id="44ae9-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44ae9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ae9-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44ae9-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ae9-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44ae9-157">INPUTS</span></span>

### <span data-ttu-id="44ae9-158">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="44ae9-158">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="44ae9-159">System. String</span><span class="sxs-lookup"><span data-stu-id="44ae9-159">System.String</span></span>

## <span data-ttu-id="44ae9-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44ae9-160">OUTPUTS</span></span>

### <span data-ttu-id="44ae9-161">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="44ae9-161">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="44ae9-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="44ae9-162">NOTES</span></span>

## <span data-ttu-id="44ae9-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44ae9-163">RELATED LINKS</span></span>
