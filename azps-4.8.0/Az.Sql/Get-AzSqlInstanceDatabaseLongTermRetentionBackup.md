---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: ccd716b493640afef7b5adea0b2e834c10893c3c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235304"
---
# <span data-ttu-id="be7d0-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="be7d0-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="be7d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be7d0-102">SYNOPSIS</span></span>
<span data-ttu-id="be7d0-103">Возвращает долгосрочные резервные копии хранения.</span><span class="sxs-lookup"><span data-stu-id="be7d0-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="be7d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be7d0-104">SYNTAX</span></span>

### <span data-ttu-id="be7d0-105">Расположение (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be7d0-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be7d0-106">InstanceName (имя_экземпляра)</span><span class="sxs-lookup"><span data-stu-id="be7d0-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be7d0-107">Имя</span><span class="sxs-lookup"><span data-stu-id="be7d0-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be7d0-108">BackupName</span><span class="sxs-lookup"><span data-stu-id="be7d0-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be7d0-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="be7d0-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be7d0-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="be7d0-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be7d0-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="be7d0-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be7d0-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be7d0-112">DESCRIPTION</span></span>
<span data-ttu-id="be7d0-113">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="be7d0-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="be7d0-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be7d0-114">EXAMPLES</span></span>

### <span data-ttu-id="be7d0-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="be7d0-115">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


BackupExpirationTime : 3/10/2020 1:10:45 PM
BackupName           : 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
BackupTime           : 2/22/2020 6:04:15 AM
DatabaseName         : test
DatabaseDeletionTime : 2/24/2020 2:56:44 PM
Location             : southeastasia
ResourceId           : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManaged
                       Instances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
ManagedInstanceName  : testInstance
InstanceCreateTime   : 10/17/2019 4:52:10 PM
ResourceGroupName    : testResourceGroup
```

<span data-ttu-id="be7d0-116">Получает все долгосрочные резервные копии хранения для определенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="be7d0-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="be7d0-117">Группа ресурсов является необязательной.</span><span class="sxs-lookup"><span data-stu-id="be7d0-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="be7d0-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be7d0-118">PARAMETERS</span></span>

### <span data-ttu-id="be7d0-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="be7d0-119">-BackupName</span></span>
<span data-ttu-id="be7d0-120">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="be7d0-120">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be7d0-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="be7d0-121">-DatabaseName</span></span>
<span data-ttu-id="be7d0-122">Имя управляемой базы данных, в которой находятся резервные копии.</span><span class="sxs-lookup"><span data-stu-id="be7d0-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7d0-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="be7d0-123">-DatabaseState</span></span>
<span data-ttu-id="be7d0-124">Состояние базы данных, резервные копии которой вы хотите найти, проверить, удалить или все.</span><span class="sxs-lookup"><span data-stu-id="be7d0-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="be7d0-125">По умолчанию все</span><span class="sxs-lookup"><span data-stu-id="be7d0-125">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be7d0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be7d0-126">-DefaultProfile</span></span>
<span data-ttu-id="be7d0-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be7d0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be7d0-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be7d0-128">-InputObject</span></span>
<span data-ttu-id="be7d0-129">Объект базы данных, для которого требуется получить резервные копии.</span><span class="sxs-lookup"><span data-stu-id="be7d0-129">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be7d0-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="be7d0-130">-InstanceName</span></span>
<span data-ttu-id="be7d0-131">Имя управляемого экземпляра, под которым находятся резервные копии.</span><span class="sxs-lookup"><span data-stu-id="be7d0-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7d0-132">-Location</span><span class="sxs-lookup"><span data-stu-id="be7d0-132">-Location</span></span>
<span data-ttu-id="be7d0-133">Расположение исходного экземпляра, управляемого с помощью резервных копий.</span><span class="sxs-lookup"><span data-stu-id="be7d0-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7d0-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="be7d0-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="be7d0-135">Следует ли получить последнюю резервную копию на базу данных.</span><span class="sxs-lookup"><span data-stu-id="be7d0-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="be7d0-136">По умолчанию используется значение false.</span><span class="sxs-lookup"><span data-stu-id="be7d0-136">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7d0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be7d0-137">-ResourceGroupName</span></span>
<span data-ttu-id="be7d0-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be7d0-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7d0-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be7d0-139">-ResourceId</span></span>
<span data-ttu-id="be7d0-140">Идентификатор ресурса базы данных, для которого требуется получить резервные копии.</span><span class="sxs-lookup"><span data-stu-id="be7d0-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be7d0-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be7d0-141">-Confirm</span></span>
<span data-ttu-id="be7d0-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be7d0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be7d0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be7d0-143">-WhatIf</span></span>
<span data-ttu-id="be7d0-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be7d0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be7d0-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be7d0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be7d0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be7d0-146">CommonParameters</span></span>
<span data-ttu-id="be7d0-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be7d0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be7d0-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be7d0-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be7d0-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be7d0-149">INPUTS</span></span>

### <span data-ttu-id="be7d0-150">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="be7d0-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="be7d0-151">System. String</span><span class="sxs-lookup"><span data-stu-id="be7d0-151">System.String</span></span>

## <span data-ttu-id="be7d0-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be7d0-152">OUTPUTS</span></span>

### <span data-ttu-id="be7d0-153">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="be7d0-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="be7d0-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="be7d0-154">NOTES</span></span>

## <span data-ttu-id="be7d0-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be7d0-155">RELATED LINKS</span></span>

[<span data-ttu-id="be7d0-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="be7d0-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="be7d0-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="be7d0-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="be7d0-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="be7d0-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="be7d0-159">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="be7d0-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)