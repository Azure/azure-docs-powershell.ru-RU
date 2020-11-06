---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 61fe76eba8d1f8faf0ab45d0a24f56a8dabf3641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568836"
---
# <span data-ttu-id="f7470-101">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f7470-101">Restore-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="f7470-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7470-102">SYNOPSIS</span></span>
<span data-ttu-id="f7470-103">Восстанавливает базу данных экземпляра, управляемой службой Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f7470-103">Restores an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7470-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7470-104">SYNTAX</span></span>

### <span data-ttu-id="f7470-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7470-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7470-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="f7470-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7470-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="f7470-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7470-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="f7470-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7470-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="f7470-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7470-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="f7470-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7470-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7470-111">DESCRIPTION</span></span>
<span data-ttu-id="f7470-112">Командлет **RESTORE-AzureRmSqlInstanceDatabase** восстанавливает базу данных экземпляра на момент времени в действующей базе данных.</span><span class="sxs-lookup"><span data-stu-id="f7470-112">The **Restore-AzureRmSqlInstanceDatabase** cmdlet restores an instance database from a point in time in a live database.</span></span>
<span data-ttu-id="f7470-113">Восстановленная база данных создается как новая база данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7470-113">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="f7470-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7470-114">EXAMPLES</span></span>

### <span data-ttu-id="f7470-115">Пример 1: восстановление базы данных экземпляра на момент времени</span><span class="sxs-lookup"><span data-stu-id="f7470-115">Example 1: Restore a instance database from a point in time</span></span>
```
PS C:\> Restore-AzureRmSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="f7470-116">Команда восстанавливает базу данных экземпляра Database01 из указанного резервного копирования на момент времени в базу данных экземпляра с именем Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="f7470-116">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="f7470-117">Пример 2: восстановление базы данных экземпляра с момента времени до другого экземпляра в другой группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="f7470-117">Example 2: Restore a instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="f7470-118">Команда восстанавливает базу данных экземпляра Database01 на экземпляре managedInstance1 в группе ресурсов ResourceGroup01 с указанной на момент времени резервной копии в базу данных экземпляра с именем Database01_restored на экземпляре managedInstance2 в группе ресурсов ResourceGroup02.</span><span class="sxs-lookup"><span data-stu-id="f7470-118">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

## <span data-ttu-id="f7470-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7470-119">PARAMETERS</span></span>

### <span data-ttu-id="f7470-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7470-120">-AsJob</span></span>
<span data-ttu-id="f7470-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f7470-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7470-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7470-122">-DefaultProfile</span></span>
<span data-ttu-id="f7470-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7470-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7470-124">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="f7470-124">-FromPointInTimeBackup</span></span>
<span data-ttu-id="f7470-125">Восстановление из резервной копии на момент времени.</span><span class="sxs-lookup"><span data-stu-id="f7470-125">Restore from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7470-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7470-126">-InputObject</span></span>
<span data-ttu-id="f7470-127">Объект базы данных экземпляра для восстановления</span><span class="sxs-lookup"><span data-stu-id="f7470-127">The Instance Database object to restore</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7470-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f7470-128">-InstanceName</span></span>
<span data-ttu-id="f7470-129">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7470-129">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7470-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7470-130">-Name</span></span>
<span data-ttu-id="f7470-131">Имя базы данных экземпляра для восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7470-131">The instance database name to restore.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7470-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="f7470-132">-PointInTime</span></span>
<span data-ttu-id="f7470-133">Момент времени, в который нужно восстановить базу данных.</span><span class="sxs-lookup"><span data-stu-id="f7470-133">The point in time to restore the database to.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7470-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7470-134">-ResourceGroupName</span></span>
<span data-ttu-id="f7470-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7470-135">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7470-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7470-136">-ResourceId</span></span>
<span data-ttu-id="f7470-137">Идентификатор ресурса экземпляра базы данных, который нужно восстановить</span><span class="sxs-lookup"><span data-stu-id="f7470-137">The resource id of Instance Database object to restore</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7470-138">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f7470-138">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="f7470-139">Имя целевой базы данных экземпляра для восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7470-139">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="f7470-140">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="f7470-140">-TargetInstanceName</span></span>
<span data-ttu-id="f7470-141">Имя целевого экземпляра, в который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="f7470-141">The name of the target instance to restore to.</span></span>
<span data-ttu-id="f7470-142">Если он не указан, целевой экземпляр совпадает с исходным экземпляром.</span><span class="sxs-lookup"><span data-stu-id="f7470-142">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7470-143">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7470-143">-TargetResourceGroupName</span></span>
<span data-ttu-id="f7470-144">Имя целевой группы ресурсов, в которую будет восстановлено значение.</span><span class="sxs-lookup"><span data-stu-id="f7470-144">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="f7470-145">Если этот элемент не указан, Целевая группа ресурсов совпадает с исходной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7470-145">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7470-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7470-146">-Confirm</span></span>
<span data-ttu-id="f7470-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7470-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7470-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7470-148">-WhatIf</span></span>
<span data-ttu-id="f7470-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7470-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7470-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7470-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7470-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7470-151">CommonParameters</span></span>
<span data-ttu-id="f7470-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7470-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7470-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7470-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7470-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7470-154">INPUTS</span></span>

### <span data-ttu-id="f7470-155">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f7470-155">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>
<span data-ttu-id="f7470-156">System. String</span><span class="sxs-lookup"><span data-stu-id="f7470-156">System.String</span></span>

## <span data-ttu-id="f7470-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7470-157">OUTPUTS</span></span>

### <span data-ttu-id="f7470-158">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f7470-158">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="f7470-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7470-159">NOTES</span></span>

## <span data-ttu-id="f7470-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7470-160">RELATED LINKS</span></span>
