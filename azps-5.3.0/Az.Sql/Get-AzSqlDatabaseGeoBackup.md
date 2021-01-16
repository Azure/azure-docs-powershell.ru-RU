---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419351"
---
# <span data-ttu-id="e867f-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="e867f-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="e867f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e867f-102">SYNOPSIS</span></span>
<span data-ttu-id="e867f-103">Получает гео избыточное резервное копирование базы данных.</span><span class="sxs-lookup"><span data-stu-id="e867f-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="e867f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e867f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e867f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e867f-105">DESCRIPTION</span></span>
<span data-ttu-id="e867f-106">Cmdlet **Get-AzSqlDatabaseGeoBackup** получает указанную геоизбыточную резервную копию базы данных SQL или все доступные геоизбытные резервные копии на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="e867f-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="e867f-107">Гео избыточное резервное копирование — это восстановленный ресурс, использующий файлы данных из отдельного географического расположения.</span><span class="sxs-lookup"><span data-stu-id="e867f-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="e867f-108">Вы можете Geo-Restore резервную копию в случае регионального простоя, чтобы восстановить базу данных в новом регионе.</span><span class="sxs-lookup"><span data-stu-id="e867f-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="e867f-109">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="e867f-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e867f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e867f-110">EXAMPLES</span></span>

### <span data-ttu-id="e867f-111">Пример 1. Получите все гео избыточные резервные копии на сервере</span><span class="sxs-lookup"><span data-stu-id="e867f-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="e867f-112">Эта команда получает все доступные гео избыточные резервные копии на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="e867f-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="e867f-113">Пример 2. Получить указанную геопроибытную резервную копию</span><span class="sxs-lookup"><span data-stu-id="e867f-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="e867f-114">Эта команда получает геозабытную резервную копию базы данных ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="e867f-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="e867f-115">Пример 3. Получите все гео избыточные резервные копии на сервере с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="e867f-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="e867f-116">Эта команда получает все доступные гео избыточные резервные копии на указанном сервере, который начинается с Contoso.</span><span class="sxs-lookup"><span data-stu-id="e867f-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="e867f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e867f-117">PARAMETERS</span></span>

### <span data-ttu-id="e867f-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e867f-118">-DatabaseName</span></span>
<span data-ttu-id="e867f-119">Имя базы данных, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="e867f-119">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e867f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e867f-120">-DefaultProfile</span></span>
<span data-ttu-id="e867f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e867f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e867f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e867f-122">-ResourceGroupName</span></span>
<span data-ttu-id="e867f-123">Имя группы ресурсов, которой назначен SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="e867f-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e867f-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e867f-124">-ServerName</span></span>
<span data-ttu-id="e867f-125">Указывает имя сервера, на котором размещена резервная копия для восстановления.</span><span class="sxs-lookup"><span data-stu-id="e867f-125">Specifies the name of the server that hosts the backup to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e867f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e867f-126">-Confirm</span></span>
<span data-ttu-id="e867f-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e867f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e867f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e867f-128">-WhatIf</span></span>
<span data-ttu-id="e867f-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e867f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e867f-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e867f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e867f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e867f-131">CommonParameters</span></span>
<span data-ttu-id="e867f-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e867f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e867f-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e867f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e867f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e867f-134">INPUTS</span></span>

### <span data-ttu-id="e867f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e867f-135">System.String</span></span>

## <span data-ttu-id="e867f-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e867f-136">OUTPUTS</span></span>

### <span data-ttu-id="e867f-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="e867f-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="e867f-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e867f-138">NOTES</span></span>

## <span data-ttu-id="e867f-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e867f-139">RELATED LINKS</span></span>

[<span data-ttu-id="e867f-140">Обзор: непрерывность облачного бизнеса и аварийное восстановление базы данных с SQL Database</span><span class="sxs-lookup"><span data-stu-id="e867f-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="e867f-141">Восстановление базы данных Azure SQL из-за простоя</span><span class="sxs-lookup"><span data-stu-id="e867f-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="e867f-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e867f-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="e867f-143">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="e867f-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
