---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 8fd76e227951afefcbb8f7b04cf4ae3616ef5ef7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728858"
---
# <span data-ttu-id="1c932-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="1c932-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="1c932-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c932-102">SYNOPSIS</span></span>
<span data-ttu-id="1c932-103">Удаление долгосрочной резервной копии хранения.</span><span class="sxs-lookup"><span data-stu-id="1c932-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="1c932-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c932-104">SYNTAX</span></span>

### <span data-ttu-id="1c932-105">RemoveBackupDefault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1c932-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c932-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="1c932-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c932-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c932-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c932-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c932-108">DESCRIPTION</span></span>
<span data-ttu-id="1c932-109">Командлет **Remove-AzSqlDatabaseLongTermRetentionBackup** удаляет указанную резервную копию.</span><span class="sxs-lookup"><span data-stu-id="1c932-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="1c932-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c932-110">EXAMPLES</span></span>

### <span data-ttu-id="1c932-111">Пример 1: удаление одной резервной копии</span><span class="sxs-lookup"><span data-stu-id="1c932-111">Example 1: Delete a single backup</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="1c932-112">Удаление резервной копии с именем 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="1c932-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="1c932-113">Пример 2: удаление всех резервных копий для местоположения</span><span class="sxs-lookup"><span data-stu-id="1c932-113">Example 2: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="1c932-114">Эта команда удаляет все долгосрочные резервные копии хранения для местоположения northeurope.</span><span class="sxs-lookup"><span data-stu-id="1c932-114">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="1c932-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c932-115">PARAMETERS</span></span>

### <span data-ttu-id="1c932-116">-BackupName</span><span class="sxs-lookup"><span data-stu-id="1c932-116">-BackupName</span></span>
<span data-ttu-id="1c932-117">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="1c932-117">The name of the backup.</span></span>

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

### <span data-ttu-id="1c932-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1c932-118">-DatabaseName</span></span>
<span data-ttu-id="1c932-119">Имя базы данных SQL Azure, из которой находится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="1c932-119">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="1c932-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c932-120">-DefaultProfile</span></span>
<span data-ttu-id="1c932-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c932-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c932-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1c932-122">-Force</span></span>
<span data-ttu-id="1c932-123">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="1c932-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1c932-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c932-124">-InputObject</span></span>
<span data-ttu-id="1c932-125">Удаляемый объект резервного копирования базы данных для хранения.</span><span class="sxs-lookup"><span data-stu-id="1c932-125">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c932-126">-Location</span><span class="sxs-lookup"><span data-stu-id="1c932-126">-Location</span></span>
<span data-ttu-id="1c932-127">Расположение исходного сервера резервных копий.</span><span class="sxs-lookup"><span data-stu-id="1c932-127">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="1c932-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c932-128">-ResourceId</span></span>
<span data-ttu-id="1c932-129">Идентификатор ресурса резервной копии базы данных, для которого необходимо удалить архив.</span><span class="sxs-lookup"><span data-stu-id="1c932-129">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="1c932-130">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="1c932-130">-ServerName</span></span>
<span data-ttu-id="1c932-131">Имя сервера Azure SQL Server, в котором находится резервная копия.</span><span class="sxs-lookup"><span data-stu-id="1c932-131">The name of the Azure SQL Server the backup is under.</span></span>

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

### <span data-ttu-id="1c932-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c932-132">-Confirm</span></span>
<span data-ttu-id="1c932-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1c932-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c932-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c932-134">-WhatIf</span></span>
<span data-ttu-id="1c932-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1c932-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c932-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1c932-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c932-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c932-137">CommonParameters</span></span>
<span data-ttu-id="1c932-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c932-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c932-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c932-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c932-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c932-140">INPUTS</span></span>

### <span data-ttu-id="1c932-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1c932-141">System.String</span></span>

## <span data-ttu-id="1c932-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c932-142">OUTPUTS</span></span>

### <span data-ttu-id="1c932-143">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="1c932-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="1c932-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c932-144">NOTES</span></span>

## <span data-ttu-id="1c932-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c932-145">RELATED LINKS</span></span>

[<span data-ttu-id="1c932-146">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="1c932-146">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="1c932-147">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c932-147">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="1c932-148">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c932-148">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="1c932-149">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="1c932-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)