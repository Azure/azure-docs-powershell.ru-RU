---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: e97143f282bc01bbdd9c5d6186f0ccb5532b1df1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419319"
---
# <span data-ttu-id="cc32a-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="cc32a-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="cc32a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc32a-102">SYNOPSIS</span></span>
<span data-ttu-id="cc32a-103">Получает одну или несколько резервных копий хранения в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="cc32a-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="cc32a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc32a-104">SYNTAX</span></span>

### <span data-ttu-id="cc32a-105">Расположение (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc32a-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc32a-106">Имя Сервера</span><span class="sxs-lookup"><span data-stu-id="cc32a-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc32a-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="cc32a-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc32a-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc32a-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc32a-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc32a-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc32a-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="cc32a-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc32a-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="cc32a-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc32a-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc32a-112">DESCRIPTION</span></span>
<span data-ttu-id="cc32a-113">Для хранения местоположения, сервера или базы данных с функцией **Get-AzSqlDataBaseLongTermRetentionBackup** в течение долгого времени можно получить резервную копию.</span><span class="sxs-lookup"><span data-stu-id="cc32a-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="cc32a-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc32a-114">EXAMPLES</span></span>

### <span data-ttu-id="cc32a-115">Пример 1. Получить все резервные копии для расположения</span><span class="sxs-lookup"><span data-stu-id="cc32a-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope


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

<span data-ttu-id="cc32a-116">Эта команда получает все долгосрочные резервные копии хранения для всех баз данных (которые могут быть живы или удалены) в northeurope, группа ресурсов будет настроена только при условии, что сервер находится в прямом эфире.</span><span class="sxs-lookup"><span data-stu-id="cc32a-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="cc32a-117">Пример 2. Получить все резервные копии для расположения в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="cc32a-117">Example 2: Get all backups for a location under a resource group</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ResourceGroup resourceGroup01


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

<span data-ttu-id="cc32a-118">Эта команда получает все долгосрочные резервные копии хранения для всех баз данных (которые могут быть живы или удалены) в группе ресурсов в northeurope.</span><span class="sxs-lookup"><span data-stu-id="cc32a-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="cc32a-119">Пример 3. Получите резервную копию хранения в течение определенного времени</span><span class="sxs-lookup"><span data-stu-id="cc32a-119">Example 3: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


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

<span data-ttu-id="cc32a-120">Эта команда получает резервную копию с именем 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span><span class="sxs-lookup"><span data-stu-id="cc32a-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="cc32a-121">Пример 4. Получите все резервные копии хранения в течение долгого времени для базы данных</span><span class="sxs-lookup"><span data-stu-id="cc32a-121">Example 4: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="cc32a-122">Эта команда получает все долгосрочные резервные копии хранения для базы данных01</span><span class="sxs-lookup"><span data-stu-id="cc32a-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="cc32a-123">Пример 5. Получите долгосрочное резервное копирование хранения с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="cc32a-123">Example 5: Get long term retention backups using filtering</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7*"

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database02/longTermRetentionBackups/601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server01
ServerCreateTime     : 2/28/2018 12:12:19 AM

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

<span data-ttu-id="cc32a-124">Эта команда получает все резервные копии с именем, которое начинается с "601061b7"</span><span class="sxs-lookup"><span data-stu-id="cc32a-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="cc32a-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc32a-125">PARAMETERS</span></span>

### <span data-ttu-id="cc32a-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="cc32a-126">-BackupName</span></span>
<span data-ttu-id="cc32a-127">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="cc32a-127">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc32a-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cc32a-128">-DatabaseName</span></span>
<span data-ttu-id="cc32a-129">Имя базы данных Azure SQL, из которой создана резервная копия.</span><span class="sxs-lookup"><span data-stu-id="cc32a-129">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BackupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32a-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="cc32a-130">-DatabaseState</span></span>
<span data-ttu-id="cc32a-131">Состояние базы данных, резервные копии которой нужно найти: "Живые", "Удаленные" или "Все".</span><span class="sxs-lookup"><span data-stu-id="cc32a-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="cc32a-132">По умолчанию для всех</span><span class="sxs-lookup"><span data-stu-id="cc32a-132">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc32a-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc32a-133">-DefaultProfile</span></span>
<span data-ttu-id="cc32a-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc32a-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc32a-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc32a-135">-InputObject</span></span>
<span data-ttu-id="cc32a-136">Объект базы данных, для которой нужно получить резервные копии.</span><span class="sxs-lookup"><span data-stu-id="cc32a-136">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc32a-137">-Location</span><span class="sxs-lookup"><span data-stu-id="cc32a-137">-Location</span></span>
<span data-ttu-id="cc32a-138">Расположение исходных серверов резервных копий.</span><span class="sxs-lookup"><span data-stu-id="cc32a-138">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32a-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="cc32a-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="cc32a-140">Нужно ли получать только последние резервные копии для базы данных.</span><span class="sxs-lookup"><span data-stu-id="cc32a-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="cc32a-141">Значение по умолчанию false.</span><span class="sxs-lookup"><span data-stu-id="cc32a-141">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc32a-142">-ResourceGroupName</span></span>
<span data-ttu-id="cc32a-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc32a-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32a-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc32a-144">-ResourceId</span></span>
<span data-ttu-id="cc32a-145">ИД ресурса базы данных, для которой нужно получить резервные копии.</span><span class="sxs-lookup"><span data-stu-id="cc32a-145">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc32a-146">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cc32a-146">-ServerName</span></span>
<span data-ttu-id="cc32a-147">Имя службы Azure SQL Server под резервными копиями.</span><span class="sxs-lookup"><span data-stu-id="cc32a-147">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32a-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc32a-148">-Confirm</span></span>
<span data-ttu-id="cc32a-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc32a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc32a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc32a-150">-WhatIf</span></span>
<span data-ttu-id="cc32a-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc32a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc32a-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cc32a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc32a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc32a-153">CommonParameters</span></span>
<span data-ttu-id="cc32a-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc32a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc32a-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc32a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc32a-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc32a-156">INPUTS</span></span>

### <span data-ttu-id="cc32a-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cc32a-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="cc32a-158">System.String</span><span class="sxs-lookup"><span data-stu-id="cc32a-158">System.String</span></span>

## <span data-ttu-id="cc32a-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc32a-159">OUTPUTS</span></span>

### <span data-ttu-id="cc32a-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="cc32a-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="cc32a-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc32a-161">NOTES</span></span>

## <span data-ttu-id="cc32a-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc32a-162">RELATED LINKS</span></span>

[<span data-ttu-id="cc32a-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="cc32a-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="cc32a-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cc32a-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="cc32a-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cc32a-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="cc32a-166">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="cc32a-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)