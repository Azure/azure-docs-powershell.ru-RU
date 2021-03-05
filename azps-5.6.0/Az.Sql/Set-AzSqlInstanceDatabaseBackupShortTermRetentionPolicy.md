---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 0a08176dab2d4bb40d25f11574850d584981063c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981544"
---
# <span data-ttu-id="fa419-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fa419-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="fa419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa419-102">SYNOPSIS</span></span>
<span data-ttu-id="fa419-103">Задает политику хранения для резервного копирования в течение короткого срока.</span><span class="sxs-lookup"><span data-stu-id="fa419-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="fa419-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fa419-104">SYNTAX</span></span>

### <span data-ttu-id="fa419-105">PolicyByResourceInstanceDatabaseSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa419-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa419-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fa419-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa419-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fa419-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa419-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa419-108">DESCRIPTION</span></span>
<span data-ttu-id="fa419-109">Для этой базы данных зарегистрируется **краткое** политика хранения, зарегистрированная для этой базы данных, с ее учетом.</span><span class="sxs-lookup"><span data-stu-id="fa419-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="fa419-110">Политика — это период хранения в днях для восстановления резервных копий за данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="fa419-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="fa419-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fa419-111">EXAMPLES</span></span>

### <span data-ttu-id="fa419-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fa419-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="fa419-113">Эта команда задает кратковременную политику хранения для базы данных01, которая составляет 35 дней.</span><span class="sxs-lookup"><span data-stu-id="fa419-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="fa419-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fa419-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="fa419-115">Эта команда задает краткосрочную политику хранения для базы данных01 до 35 дней посредством прокайки в объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="fa419-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="fa419-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="fa419-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 8
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 8

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 8
```

<span data-ttu-id="fa419-117">Эта команда задает краткосрочную политику хранения для всех удаленных баз данных с именем DB1 путем прокавки в удаленном объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="fa419-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="fa419-118">Имейте в виду, что срок хранения удаленных баз данных можно сократить.</span><span class="sxs-lookup"><span data-stu-id="fa419-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="fa419-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa419-119">PARAMETERS</span></span>

### <span data-ttu-id="fa419-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fa419-120">-DatabaseName</span></span>
<span data-ttu-id="fa419-121">Имя базы данных экземпляра Azure SQL Azure, для которой нужно получить резервные копии.</span><span class="sxs-lookup"><span data-stu-id="fa419-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa419-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa419-122">-DefaultProfile</span></span>
<span data-ttu-id="fa419-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa419-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa419-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="fa419-124">-DeletionDate</span></span>
<span data-ttu-id="fa419-125">Дата удаления базы данных экземпляра Azure SQL для получения резервных копий с точностью в миллисекунд (например, 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="fa419-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa419-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa419-126">-InputObject</span></span>
<span data-ttu-id="fa419-127">Live или deleted database object to get/set the policy for.</span><span class="sxs-lookup"><span data-stu-id="fa419-127">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa419-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fa419-128">-InstanceName</span></span>
<span data-ttu-id="fa419-129">Имя управляемого экземпляра SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fa419-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa419-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa419-130">-ResourceGroupName</span></span>
<span data-ttu-id="fa419-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fa419-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa419-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa419-132">-ResourceId</span></span>
<span data-ttu-id="fa419-133">Краткий ИД ресурса политики хранения.</span><span class="sxs-lookup"><span data-stu-id="fa419-133">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa419-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="fa419-134">-RetentionDays</span></span>
<span data-ttu-id="fa419-135">Количество дней хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="fa419-135">Days of backup retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa419-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa419-136">-Confirm</span></span>
<span data-ttu-id="fa419-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fa419-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa419-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa419-138">-WhatIf</span></span>
<span data-ttu-id="fa419-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa419-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa419-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fa419-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa419-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa419-141">CommonParameters</span></span>
<span data-ttu-id="fa419-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa419-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa419-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa419-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa419-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa419-144">INPUTS</span></span>

### <span data-ttu-id="fa419-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fa419-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="fa419-146">System.String</span><span class="sxs-lookup"><span data-stu-id="fa419-146">System.String</span></span>

## <span data-ttu-id="fa419-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa419-147">OUTPUTS</span></span>

### <span data-ttu-id="fa419-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fa419-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="fa419-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fa419-149">NOTES</span></span>

## <span data-ttu-id="fa419-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa419-150">RELATED LINKS</span></span>
