---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 93c4c5c1fa269414b80001f9fd24f1a79c5ed4de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078615"
---
# <span data-ttu-id="91628-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="91628-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="91628-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91628-102">SYNOPSIS</span></span>
<span data-ttu-id="91628-103">Настройка политики хранения для архивации по короткому критерию.</span><span class="sxs-lookup"><span data-stu-id="91628-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="91628-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91628-104">SYNTAX</span></span>

### <span data-ttu-id="91628-105">PolicyByResourceInstanceDatabaseSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="91628-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91628-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="91628-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91628-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="91628-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91628-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91628-108">DESCRIPTION</span></span>
<span data-ttu-id="91628-109">Командлет **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** получает краткосрочную политику хранения, зарегистрированную в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="91628-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="91628-110">Политика — срок хранения (в днях) для резервного копирования на определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="91628-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="91628-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91628-111">EXAMPLES</span></span>

### <span data-ttu-id="91628-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="91628-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="91628-113">Эта команда устанавливает краткосрочную политику хранения для Database01 в 35 дней.</span><span class="sxs-lookup"><span data-stu-id="91628-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="91628-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="91628-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="91628-115">Эта команда задает краткосрочную политику хранения для Database01 в 35 дней с помощью трубопроводов в объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="91628-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="91628-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="91628-116">Example 3</span></span>
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

<span data-ttu-id="91628-117">Эта команда задает политику краткосрочного хранения для всех удаленных баз данных с именем DB1 по конвейеру в удаленном объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="91628-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="91628-118">Примечание. Вы можете уменьшить срок хранения в удаленных базах данных.</span><span class="sxs-lookup"><span data-stu-id="91628-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="91628-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91628-119">PARAMETERS</span></span>

### <span data-ttu-id="91628-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="91628-120">-DatabaseName</span></span>
<span data-ttu-id="91628-121">Имя базы данных экземпляра Azure SQL, для которой требуется получить резервные копии.</span><span class="sxs-lookup"><span data-stu-id="91628-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="91628-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91628-122">-DefaultProfile</span></span>
<span data-ttu-id="91628-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91628-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91628-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="91628-124">-DeletionDate</span></span>
<span data-ttu-id="91628-125">Дата удаления базы данных экземпляра Azure SQL, для которой требуется получить резервные копии с точностью до миллисекунд (например, 2016-02-23T00:21:22.847 Z)</span><span class="sxs-lookup"><span data-stu-id="91628-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="91628-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91628-126">-InputObject</span></span>
<span data-ttu-id="91628-127">Объект базы данных Live или DELETE, для которого нужно получить или настроить политику.</span><span class="sxs-lookup"><span data-stu-id="91628-127">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="91628-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="91628-128">-InstanceName</span></span>
<span data-ttu-id="91628-129">Имя управляемого экземпляра Azure SQL, на котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="91628-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="91628-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91628-130">-ResourceGroupName</span></span>
<span data-ttu-id="91628-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91628-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="91628-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91628-132">-ResourceId</span></span>
<span data-ttu-id="91628-133">Краткосрочный идентификатор ресурса политики хранения.</span><span class="sxs-lookup"><span data-stu-id="91628-133">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="91628-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="91628-134">-RetentionDays</span></span>
<span data-ttu-id="91628-135">Дни хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="91628-135">Days of backup retention.</span></span>

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

### <span data-ttu-id="91628-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91628-136">-Confirm</span></span>
<span data-ttu-id="91628-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="91628-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91628-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91628-138">-WhatIf</span></span>
<span data-ttu-id="91628-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="91628-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91628-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="91628-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91628-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91628-141">CommonParameters</span></span>
<span data-ttu-id="91628-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91628-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91628-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91628-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91628-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91628-144">INPUTS</span></span>

### <span data-ttu-id="91628-145">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="91628-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="91628-146">System. String</span><span class="sxs-lookup"><span data-stu-id="91628-146">System.String</span></span>

## <span data-ttu-id="91628-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91628-147">OUTPUTS</span></span>

### <span data-ttu-id="91628-148">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="91628-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="91628-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="91628-149">NOTES</span></span>

## <span data-ttu-id="91628-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91628-150">RELATED LINKS</span></span>
