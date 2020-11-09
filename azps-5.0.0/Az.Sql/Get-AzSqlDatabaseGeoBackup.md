---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249602"
---
# <span data-ttu-id="e4c68-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="e4c68-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="e4c68-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4c68-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c68-103">Получает геоизбыточную резервную копию базы данных.</span><span class="sxs-lookup"><span data-stu-id="e4c68-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="e4c68-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4c68-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4c68-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4c68-105">DESCRIPTION</span></span>
<span data-ttu-id="e4c68-106">Командлет **Get-AzSqlDatabaseGeoBackup** получает указанную геоизбыточную резервную копию базы данных SQL или все доступные геоизбыточные резервные копии на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="e4c68-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="e4c68-107">Резервная копия с геоизбыточным резервированием — это ресурс restorable с использованием файлов данных из отдельного географического расположения.</span><span class="sxs-lookup"><span data-stu-id="e4c68-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="e4c68-108">Вы можете использовать Geo-Restore для восстановления геоизбыточной резервной копии в случае сбоя в регионе, чтобы восстановить базу данных в новом регионе.</span><span class="sxs-lookup"><span data-stu-id="e4c68-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="e4c68-109">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="e4c68-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e4c68-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4c68-110">EXAMPLES</span></span>

### <span data-ttu-id="e4c68-111">Пример 1: получение всех геоизбыточных резервных копий на сервере</span><span class="sxs-lookup"><span data-stu-id="e4c68-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="e4c68-112">Эта команда получает все доступные резервные копии с геоизбыточным хранилищем на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="e4c68-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="e4c68-113">Пример 2: получение указанной геоизбыточной резервной копии</span><span class="sxs-lookup"><span data-stu-id="e4c68-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="e4c68-114">Эта команда возвращает геоизбыточное резервное копирование базы данных с именем ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="e4c68-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="e4c68-115">Пример 3: получение всех геоизбыточных резервных копий на сервере с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="e4c68-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="e4c68-116">Эта команда получает все доступные резервные копии с геоизбыточной учетной записью на указанном сервере, который начинается со слова contoso.</span><span class="sxs-lookup"><span data-stu-id="e4c68-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="e4c68-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4c68-117">PARAMETERS</span></span>

### <span data-ttu-id="e4c68-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e4c68-118">-DatabaseName</span></span>
<span data-ttu-id="e4c68-119">Указывает имя базы данных, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="e4c68-119">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="e4c68-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c68-120">-DefaultProfile</span></span>
<span data-ttu-id="e4c68-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e4c68-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4c68-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c68-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4c68-123">Указывает имя группы ресурсов, которой назначен сервер базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e4c68-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="e4c68-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e4c68-124">-ServerName</span></span>
<span data-ttu-id="e4c68-125">Указывает имя сервера, на котором размещается резервная копия для восстановления.</span><span class="sxs-lookup"><span data-stu-id="e4c68-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="e4c68-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4c68-126">-Confirm</span></span>
<span data-ttu-id="e4c68-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e4c68-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4c68-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4c68-128">-WhatIf</span></span>
<span data-ttu-id="e4c68-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e4c68-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4c68-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e4c68-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4c68-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c68-131">CommonParameters</span></span>
<span data-ttu-id="e4c68-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4c68-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c68-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4c68-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c68-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4c68-134">INPUTS</span></span>

### <span data-ttu-id="e4c68-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e4c68-135">System.String</span></span>

## <span data-ttu-id="e4c68-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4c68-136">OUTPUTS</span></span>

### <span data-ttu-id="e4c68-137">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="e4c68-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="e4c68-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4c68-138">NOTES</span></span>

## <span data-ttu-id="e4c68-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4c68-139">RELATED LINKS</span></span>

[<span data-ttu-id="e4c68-140">Обзор: бесперебойная работа в облаке и аварийное восстановление базы данных с помощью базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="e4c68-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="e4c68-141">Восстановление базы данных SQL Azure из сбоя</span><span class="sxs-lookup"><span data-stu-id="e4c68-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="e4c68-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e4c68-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="e4c68-143">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="e4c68-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)