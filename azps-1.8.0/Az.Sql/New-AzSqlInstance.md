---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bfa1785004e13400395bd6a6fc93bdec29a69809
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728891"
---
# <span data-ttu-id="f7b3a-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f7b3a-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="f7b3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b3a-103">Создает экземпляр управляемой базы данных SQL для Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="f7b3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7b3a-104">SYNTAX</span></span>

### <span data-ttu-id="f7b3a-105">NewByEditionAndComputeGenerationParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7b3a-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7b3a-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="f7b3a-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7b3a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7b3a-107">DESCRIPTION</span></span>
<span data-ttu-id="f7b3a-108">Командлет **New-AzSqlInstance** создает экземпляр управляемой базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-108">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="f7b3a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7b3a-109">EXAMPLES</span></span>

### <span data-ttu-id="f7b3a-110">Пример 1: создание нового экземпляра</span><span class="sxs-lookup"><span data-stu-id="f7b3a-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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

<span data-ttu-id="f7b3a-111">Эта команда создает новый экземпляр с помощью параметров выпусков и ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="f7b3a-112">Пример 2: создание нового экземпляра</span><span class="sxs-lookup"><span data-stu-id="f7b3a-112">Example 2: Create a new instance</span></span>
```
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
```

<span data-ttu-id="f7b3a-113">Эта команда создает новый экземпляр с помощью параметров выпусков и ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="f7b3a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7b3a-114">PARAMETERS</span></span>

### <span data-ttu-id="f7b3a-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="f7b3a-115">-AdministratorCredential</span></span>
<span data-ttu-id="f7b3a-116">Учетные данные проверки подлинности SQL для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-116">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="f7b3a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7b3a-117">-AsJob</span></span>
<span data-ttu-id="f7b3a-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f7b3a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7b3a-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f7b3a-119">-AssignIdentity</span></span>
<span data-ttu-id="f7b3a-120">Создайте и назначьте удостоверение Azure Active Directory для этого управляемого экземпляра для использования в службах управления ключами, таких как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="f7b3a-121">-Параметры сортировки</span><span class="sxs-lookup"><span data-stu-id="f7b3a-121">-Collation</span></span>
<span data-ttu-id="f7b3a-122">Параметры сортировки управляемого экземпляра Azure SQL, который нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-122">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="f7b3a-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="f7b3a-123">-ComputeGeneration</span></span>
<span data-ttu-id="f7b3a-124">Вычисленое поколение для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="f7b3a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b3a-125">-DefaultProfile</span></span>
<span data-ttu-id="f7b3a-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7b3a-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="f7b3a-127">-Edition</span></span>
<span data-ttu-id="f7b3a-128">Выпуск для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-128">The edition for the instance.</span></span>

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

### <span data-ttu-id="f7b3a-129">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f7b3a-129">-LicenseType</span></span>
<span data-ttu-id="f7b3a-130">Определяет, какой тип лицензии следует использовать.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-130">Determines which License Type to use.</span></span> <span data-ttu-id="f7b3a-131">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f7b3a-131">Possible values are:</span></span>
- <span data-ttu-id="f7b3a-132">BasePrice — гибридное выгодное преимущество (AHB) для существующих владельцев лицензий SQL Server применяется скидка.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-132">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="f7b3a-133">Служба управляемого экземпляра будет скидкам для существующих владельцев лицензий SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-133">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="f7b3a-134">LicenseIncluded-(AHB) для существующих владельцев лицензий SQL Server не применяется скидка на гибридные льготы для использования в Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-134">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="f7b3a-135">Служба управляемого экземпляра будет включать в себя новые цены на лицензии SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-135">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b3a-136">-Location</span><span class="sxs-lookup"><span data-stu-id="f7b3a-136">-Location</span></span>
<span data-ttu-id="f7b3a-137">Расположение, в котором нужно создать экземпляр.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-137">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b3a-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7b3a-138">-Name</span></span>
<span data-ttu-id="f7b3a-139">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-139">Instance name.</span></span>

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

### <span data-ttu-id="f7b3a-140">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="f7b3a-140">-ProxyOverride</span></span>
<span data-ttu-id="f7b3a-141">Тип соединения, который используется для подключения к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-141">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="f7b3a-142">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="f7b3a-142">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="f7b3a-143">Включена ли конечная точка открытых данных для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-143">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="f7b3a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b3a-144">-ResourceGroupName</span></span>
<span data-ttu-id="f7b3a-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b3a-146">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f7b3a-146">-SkuName</span></span>
<span data-ttu-id="f7b3a-147">Имя SKU для экземпляра, например "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="f7b3a-147">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="f7b3a-148">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="f7b3a-148">-StorageSizeInGB</span></span>
<span data-ttu-id="f7b3a-149">Определяет объем хранилища, связанного с экземпляром</span><span class="sxs-lookup"><span data-stu-id="f7b3a-149">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="f7b3a-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f7b3a-150">-SubnetId</span></span>
<span data-ttu-id="f7b3a-151">Идентификатор подсети, который будет использоваться для создания экземпляра</span><span class="sxs-lookup"><span data-stu-id="f7b3a-151">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b3a-152">-Тег</span><span class="sxs-lookup"><span data-stu-id="f7b3a-152">-Tag</span></span>
<span data-ttu-id="f7b3a-153">Теги, связываемые с экземпляром</span><span class="sxs-lookup"><span data-stu-id="f7b3a-153">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="f7b3a-154">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="f7b3a-154">-TimezoneId</span></span>
<span data-ttu-id="f7b3a-155">Идентификатор часового пояса для устанавливаемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-155">The time zone id for the instance to set.</span></span> <span data-ttu-id="f7b3a-156">Список идентификаторов часовых поясов предоставляется с помощью представления sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="f7b3a-156">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="f7b3a-157">-VCore</span><span class="sxs-lookup"><span data-stu-id="f7b3a-157">-VCore</span></span>
<span data-ttu-id="f7b3a-158">Определяет, сколько VCore связать с экземпляром</span><span class="sxs-lookup"><span data-stu-id="f7b3a-158">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="f7b3a-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7b3a-159">-Confirm</span></span>
<span data-ttu-id="f7b3a-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b3a-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b3a-161">-WhatIf</span></span>
<span data-ttu-id="f7b3a-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7b3a-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7b3a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b3a-164">CommonParameters</span></span>
<span data-ttu-id="f7b3a-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7b3a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b3a-166">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7b3a-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b3a-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7b3a-167">INPUTS</span></span>

### <span data-ttu-id="f7b3a-168">Ничего</span><span class="sxs-lookup"><span data-stu-id="f7b3a-168">None</span></span>

## <span data-ttu-id="f7b3a-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7b3a-169">OUTPUTS</span></span>

### <span data-ttu-id="f7b3a-170">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="f7b3a-170">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="f7b3a-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7b3a-171">NOTES</span></span>

## <span data-ttu-id="f7b3a-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7b3a-172">RELATED LINKS</span></span>
