---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
ms.openlocfilehash: 1e992e33591f5c993bfdda1bf9934245b2f5f2c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567679"
---
# <span data-ttu-id="4b40b-101">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4b40b-101">Set-AzureRmSqlInstance</span></span>

## <span data-ttu-id="4b40b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b40b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b40b-103">Задает свойства для управляемого экземпляра базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4b40b-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b40b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b40b-104">SYNTAX</span></span>

### <span data-ttu-id="4b40b-105">SetInstanceFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4b40b-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b40b-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="4b40b-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b40b-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="4b40b-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzureRmSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>] [-AssignIdentity]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b40b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b40b-108">DESCRIPTION</span></span>
<span data-ttu-id="4b40b-109">Командлет **Set-AzureRmSqlInstance** изменяет свойства экземпляра Azure SQL, управляемого базой данных.</span><span class="sxs-lookup"><span data-stu-id="4b40b-109">The **Set-AzureRmSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="4b40b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b40b-110">EXAMPLES</span></span>

### <span data-ttu-id="4b40b-111">Пример 1: Установка существующего экземпляра с использованием новых значений для параметров-AdministratorPassword,-LicenseType,-StorageSizeInGB и-VCore</span><span class="sxs-lookup"><span data-stu-id="4b40b-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="4b40b-112">Эта команда задает существующий экземпляр с использованием новых значений для параметров-AdministratorPassword,-LicenseType,-StorageSizeInGB и-VCore</span><span class="sxs-lookup"><span data-stu-id="4b40b-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

## <span data-ttu-id="4b40b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b40b-113">PARAMETERS</span></span>

### <span data-ttu-id="4b40b-114">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="4b40b-114">-AdministratorPassword</span></span>
<span data-ttu-id="4b40b-115">Новый пароль администратора SQL для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4b40b-115">The new SQL administrator password for the instance.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b40b-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4b40b-116">-AssignIdentity</span></span>
<span data-ttu-id="4b40b-117">Создавайте и назначайте удостоверение Azure Active Directory для этого экземпляра для использования в службах управления ключами, таких как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="4b40b-117">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="4b40b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b40b-118">-DefaultProfile</span></span>
<span data-ttu-id="4b40b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b40b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b40b-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="4b40b-120">-Edition</span></span>
<span data-ttu-id="4b40b-121">Выпуск, назначаемый экземпляру.</span><span class="sxs-lookup"><span data-stu-id="4b40b-121">The edition to assign to the instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b40b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4b40b-122">-Force</span></span>
<span data-ttu-id="4b40b-123">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="4b40b-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="4b40b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b40b-124">-InputObject</span></span>
<span data-ttu-id="4b40b-125">Объект AzureSqlManagedInstanceModel, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4b40b-125">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b40b-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4b40b-126">-LicenseType</span></span>
<span data-ttu-id="4b40b-127">Определяет тип используемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4b40b-127">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b40b-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4b40b-128">-Name</span></span>
<span data-ttu-id="4b40b-129">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4b40b-129">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b40b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b40b-130">-ResourceGroupName</span></span>
<span data-ttu-id="4b40b-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b40b-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b40b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b40b-132">-ResourceId</span></span>
<span data-ttu-id="4b40b-133">Идентификатор ресурса удаляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4b40b-133">The resource id of instance to remove</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b40b-134">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="4b40b-134">-StorageSizeInGB</span></span>
<span data-ttu-id="4b40b-135">Определяет объем хранилища, связанного с экземпляром</span><span class="sxs-lookup"><span data-stu-id="4b40b-135">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b40b-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="4b40b-136">-Tag</span></span>
<span data-ttu-id="4b40b-137">Теги, связываемые с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="4b40b-137">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="4b40b-138">-VCore</span><span class="sxs-lookup"><span data-stu-id="4b40b-138">-VCore</span></span>
<span data-ttu-id="4b40b-139">Определяет, сколько VCore связать с экземпляром</span><span class="sxs-lookup"><span data-stu-id="4b40b-139">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b40b-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b40b-140">-Confirm</span></span>
<span data-ttu-id="4b40b-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4b40b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b40b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b40b-142">-WhatIf</span></span>
<span data-ttu-id="4b40b-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4b40b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b40b-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4b40b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b40b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b40b-145">CommonParameters</span></span>
<span data-ttu-id="4b40b-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b40b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b40b-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b40b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b40b-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b40b-148">INPUTS</span></span>

### <span data-ttu-id="4b40b-149">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4b40b-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="4b40b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4b40b-150">System.String</span></span>

## <span data-ttu-id="4b40b-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b40b-151">OUTPUTS</span></span>

### <span data-ttu-id="4b40b-152">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4b40b-152">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="4b40b-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b40b-153">NOTES</span></span>

## <span data-ttu-id="4b40b-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b40b-154">RELATED LINKS</span></span>
