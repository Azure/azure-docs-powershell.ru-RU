---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
ms.openlocfilehash: 025a9acc53405aeb1e211473b5f8f13066791714
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568847"
---
# <span data-ttu-id="9955d-101">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9955d-101">New-AzureRmSqlInstance</span></span>

## <span data-ttu-id="9955d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9955d-102">SYNOPSIS</span></span>
<span data-ttu-id="9955d-103">Создает экземпляр управляемой базы данных SQL для Azure.</span><span class="sxs-lookup"><span data-stu-id="9955d-103">Creates an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9955d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9955d-104">SYNTAX</span></span>

### <span data-ttu-id="9955d-105">NewByEditionAndComputeGenerationParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9955d-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9955d-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="9955d-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9955d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9955d-107">DESCRIPTION</span></span>
<span data-ttu-id="9955d-108">Командлет **New-AzureRmSqlInstance** создает экземпляр управляемой базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9955d-108">The **New-AzureRmSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="9955d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9955d-109">EXAMPLES</span></span>

### <span data-ttu-id="9955d-110">Пример 1: создание нового экземпляра</span><span class="sxs-lookup"><span data-stu-id="9955d-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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

<span data-ttu-id="9955d-111">Эта команда создает новый экземпляр с помощью параметров выпусков и ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="9955d-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="9955d-112">Пример 2: создание нового экземпляра</span><span class="sxs-lookup"><span data-stu-id="9955d-112">Example 2: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
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

<span data-ttu-id="9955d-113">Эта команда создает новый экземпляр с помощью параметров выпусков и ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="9955d-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="9955d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9955d-114">PARAMETERS</span></span>

### <span data-ttu-id="9955d-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="9955d-115">-AdministratorCredential</span></span>
<span data-ttu-id="9955d-116">Учетные данные проверки подлинности SQL для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9955d-116">The SQL authentication credential of the instance.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9955d-117">-AsJob</span></span>
<span data-ttu-id="9955d-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9955d-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9955d-119">-AssignIdentity</span></span>
<span data-ttu-id="9955d-120">Создайте и назначьте удостоверение Azure Active Directory для этого управляемого экземпляра для использования в службах управления ключами, таких как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9955d-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-121">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="9955d-121">-ComputeGeneration</span></span>
<span data-ttu-id="9955d-122">Вычисленое поколение для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9955d-122">The compute generation for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9955d-123">-DefaultProfile</span></span>
<span data-ttu-id="9955d-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9955d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="9955d-125">-Edition</span></span>
<span data-ttu-id="9955d-126">Выпуск для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9955d-126">The edition for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-127">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9955d-127">-LicenseType</span></span>
<span data-ttu-id="9955d-128">Определяет тип используемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9955d-128">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-129">-Location</span><span class="sxs-lookup"><span data-stu-id="9955d-129">-Location</span></span>
<span data-ttu-id="9955d-130">Расположение, в котором нужно создать экземпляр.</span><span class="sxs-lookup"><span data-stu-id="9955d-130">The location in which to create the instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9955d-131">-Name</span></span>
<span data-ttu-id="9955d-132">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9955d-132">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9955d-133">-ResourceGroupName</span></span>
<span data-ttu-id="9955d-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9955d-134">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-135">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9955d-135">-SkuName</span></span>
<span data-ttu-id="9955d-136">Имя SKU для экземпляра, например "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="9955d-136">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-137">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="9955d-137">-StorageSizeInGB</span></span>
<span data-ttu-id="9955d-138">Определяет объем хранилища, связанного с экземпляром</span><span class="sxs-lookup"><span data-stu-id="9955d-138">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9955d-139">-SubnetId</span></span>
<span data-ttu-id="9955d-140">Идентификатор подсети, который будет использоваться для создания экземпляра</span><span class="sxs-lookup"><span data-stu-id="9955d-140">The Subnet Id to use for instance creation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-141">-Тег</span><span class="sxs-lookup"><span data-stu-id="9955d-141">-Tag</span></span>
<span data-ttu-id="9955d-142">Теги, связываемые с экземпляром</span><span class="sxs-lookup"><span data-stu-id="9955d-142">The tags to associate with the instance</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-143">-VCore</span><span class="sxs-lookup"><span data-stu-id="9955d-143">-VCore</span></span>
<span data-ttu-id="9955d-144">Определяет, сколько VCore связать с экземпляром</span><span class="sxs-lookup"><span data-stu-id="9955d-144">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9955d-145">-Confirm</span></span>
<span data-ttu-id="9955d-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9955d-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9955d-147">-WhatIf</span></span>
<span data-ttu-id="9955d-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9955d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9955d-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9955d-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9955d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9955d-150">CommonParameters</span></span>
<span data-ttu-id="9955d-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9955d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9955d-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9955d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9955d-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9955d-153">INPUTS</span></span>

### <span data-ttu-id="9955d-154">Ничего</span><span class="sxs-lookup"><span data-stu-id="9955d-154">None</span></span>

## <span data-ttu-id="9955d-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9955d-155">OUTPUTS</span></span>

### <span data-ttu-id="9955d-156">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="9955d-156">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="9955d-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="9955d-157">NOTES</span></span>

## <span data-ttu-id="9955d-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9955d-158">RELATED LINKS</span></span>
