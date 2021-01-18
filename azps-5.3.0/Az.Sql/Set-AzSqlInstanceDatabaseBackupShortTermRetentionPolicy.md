---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 93c4c5c1fa269414b80001f9fd24f1a79c5ed4de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506456"
---
# <span data-ttu-id="4a35e-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a35e-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="4a35e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a35e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a35e-103">Задает политику хранения для резервного копирования в течение краткого срока.</span><span class="sxs-lookup"><span data-stu-id="4a35e-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="4a35e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a35e-104">SYNTAX</span></span>

### <span data-ttu-id="4a35e-105">PolicyByResourceInstanceDatabaseSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a35e-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a35e-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4a35e-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a35e-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4a35e-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a35e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a35e-108">DESCRIPTION</span></span>
<span data-ttu-id="4a35e-109">Для этой базы данных зарегистрируется **краткое** сроки политики хранения, зарегистрированные для этой базы данных, с его учетом.</span><span class="sxs-lookup"><span data-stu-id="4a35e-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="4a35e-110">Политика — это срок хранения резервных копий, которые будут восстанавливаться за несколько дней.</span><span class="sxs-lookup"><span data-stu-id="4a35e-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="4a35e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a35e-111">EXAMPLES</span></span>

### <span data-ttu-id="4a35e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a35e-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="4a35e-113">Эта команда задает кратковременную политику хранения для базы данных01, которая составляет 35 дней.</span><span class="sxs-lookup"><span data-stu-id="4a35e-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="4a35e-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4a35e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="4a35e-115">Эта команда задает кратковременную политику хранения для базы данных01 в течение 35 дней путем прокажиния в объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="4a35e-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="4a35e-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4a35e-116">Example 3</span></span>
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

<span data-ttu-id="4a35e-117">Эта команда задает краткосрочную политику хранения для всех удаленных баз данных с именем DB1 путем прокавки в удаленном объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="4a35e-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="4a35e-118">Обратите внимание, что срок хранения только для удаленных баз данных можно сократить.</span><span class="sxs-lookup"><span data-stu-id="4a35e-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="4a35e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a35e-119">PARAMETERS</span></span>

### <span data-ttu-id="4a35e-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a35e-120">-DatabaseName</span></span>
<span data-ttu-id="4a35e-121">Имя базы данных экземпляра Azure SQL Azure, для которой нужно получить резервные копии.</span><span class="sxs-lookup"><span data-stu-id="4a35e-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="4a35e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a35e-122">-DefaultProfile</span></span>
<span data-ttu-id="4a35e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a35e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a35e-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="4a35e-124">-DeletionDate</span></span>
<span data-ttu-id="4a35e-125">Дата удаления базы данных экземпляра Azure SQL для получения резервных копий с точностью в миллисекунд (например, 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="4a35e-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="4a35e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a35e-126">-InputObject</span></span>
<span data-ttu-id="4a35e-127">Live или deleted database object to get/set the policy for.</span><span class="sxs-lookup"><span data-stu-id="4a35e-127">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="4a35e-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4a35e-128">-InstanceName</span></span>
<span data-ttu-id="4a35e-129">Имя управляемого экземпляра SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4a35e-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="4a35e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a35e-130">-ResourceGroupName</span></span>
<span data-ttu-id="4a35e-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a35e-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a35e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a35e-132">-ResourceId</span></span>
<span data-ttu-id="4a35e-133">Краткий ИД ресурса политики хранения.</span><span class="sxs-lookup"><span data-stu-id="4a35e-133">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="4a35e-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="4a35e-134">-RetentionDays</span></span>
<span data-ttu-id="4a35e-135">Количество дней хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="4a35e-135">Days of backup retention.</span></span>

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

### <span data-ttu-id="4a35e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a35e-136">-Confirm</span></span>
<span data-ttu-id="4a35e-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a35e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a35e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a35e-138">-WhatIf</span></span>
<span data-ttu-id="4a35e-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a35e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a35e-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4a35e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a35e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a35e-141">CommonParameters</span></span>
<span data-ttu-id="4a35e-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a35e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a35e-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a35e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a35e-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a35e-144">INPUTS</span></span>

### <span data-ttu-id="4a35e-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4a35e-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="4a35e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4a35e-146">System.String</span></span>

## <span data-ttu-id="4a35e-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a35e-147">OUTPUTS</span></span>

### <span data-ttu-id="4a35e-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4a35e-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="4a35e-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a35e-149">NOTES</span></span>

## <span data-ttu-id="4a35e-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a35e-150">RELATED LINKS</span></span>
