---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: be2e9342407cea6ba3da0bf239ee73e7b726dd82
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245824"
---
# <span data-ttu-id="88f21-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="88f21-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="88f21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88f21-102">SYNOPSIS</span></span>
<span data-ttu-id="88f21-103">Удаление долгосрочной резервной копии хранения.</span><span class="sxs-lookup"><span data-stu-id="88f21-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="88f21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88f21-104">SYNTAX</span></span>

### <span data-ttu-id="88f21-105">RemoveBackupDefault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88f21-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88f21-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="88f21-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88f21-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="88f21-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88f21-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88f21-108">DESCRIPTION</span></span>
<span data-ttu-id="88f21-109">Командлет **Remove-AzSqlDatabaseLongTermRetentionBackup** удаляет указанную резервную копию.</span><span class="sxs-lookup"><span data-stu-id="88f21-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="88f21-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88f21-110">EXAMPLES</span></span>

### <span data-ttu-id="88f21-111">Пример 1: удаление одной резервной копии с помощью группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="88f21-111">Example 1: Delete a single backup with resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000" -ResourceGrouName resourcegroup01


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="88f21-112">Удаление резервной копии с именем 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="88f21-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="88f21-113">Пример 2: удаление одной резервной копии без группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="88f21-113">Example 2: Delete a single backup without resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server02 -DatabaseName database02 -BackupName "55970792-164c-4a4a-88e5-7158d092d503;131656309980000000"


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM
```

<span data-ttu-id="88f21-114">Удаление резервной копии с именем 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="88f21-114">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="88f21-115">Пример 3: удаление всех резервных копий для местоположения</span><span class="sxs-lookup"><span data-stu-id="88f21-115">Example 3: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM
```

<span data-ttu-id="88f21-116">Эта команда удаляет все долгосрочные резервные копии хранения для местоположения northeurope.</span><span class="sxs-lookup"><span data-stu-id="88f21-116">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="88f21-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88f21-117">PARAMETERS</span></span>

### <span data-ttu-id="88f21-118">-BackupName</span><span class="sxs-lookup"><span data-stu-id="88f21-118">-BackupName</span></span>
<span data-ttu-id="88f21-119">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="88f21-119">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88f21-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="88f21-120">-DatabaseName</span></span>
<span data-ttu-id="88f21-121">Имя базы данных SQL Azure, из которой находится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="88f21-121">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88f21-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f21-122">-DefaultProfile</span></span>
<span data-ttu-id="88f21-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88f21-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88f21-124">-Force</span><span class="sxs-lookup"><span data-stu-id="88f21-124">-Force</span></span>
<span data-ttu-id="88f21-125">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="88f21-125">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88f21-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88f21-126">-InputObject</span></span>
<span data-ttu-id="88f21-127">Удаляемый объект резервного копирования базы данных для хранения.</span><span class="sxs-lookup"><span data-stu-id="88f21-127">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88f21-128">-Location</span><span class="sxs-lookup"><span data-stu-id="88f21-128">-Location</span></span>
<span data-ttu-id="88f21-129">Расположение исходного сервера резервных копий.</span><span class="sxs-lookup"><span data-stu-id="88f21-129">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88f21-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88f21-130">-ResourceGroupName</span></span>
<span data-ttu-id="88f21-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88f21-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88f21-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88f21-132">-ResourceId</span></span>
<span data-ttu-id="88f21-133">Идентификатор ресурса резервной копии базы данных, для которого необходимо удалить архив.</span><span class="sxs-lookup"><span data-stu-id="88f21-133">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88f21-134">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="88f21-134">-ServerName</span></span>
<span data-ttu-id="88f21-135">Имя сервера Azure SQL Server, в котором находится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="88f21-135">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88f21-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88f21-136">-Confirm</span></span>
<span data-ttu-id="88f21-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88f21-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88f21-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88f21-138">-WhatIf</span></span>
<span data-ttu-id="88f21-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88f21-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88f21-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88f21-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88f21-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f21-141">CommonParameters</span></span>
<span data-ttu-id="88f21-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88f21-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f21-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88f21-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f21-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88f21-144">INPUTS</span></span>

### <span data-ttu-id="88f21-145">System. String</span><span class="sxs-lookup"><span data-stu-id="88f21-145">System.String</span></span>

## <span data-ttu-id="88f21-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88f21-146">OUTPUTS</span></span>

### <span data-ttu-id="88f21-147">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="88f21-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="88f21-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="88f21-148">NOTES</span></span>

## <span data-ttu-id="88f21-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88f21-149">RELATED LINKS</span></span>

[<span data-ttu-id="88f21-150">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="88f21-150">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="88f21-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="88f21-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="88f21-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="88f21-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="88f21-153">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="88f21-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)