---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: 79e4919278e034c97b224c17538edfebfbf51a43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733214"
---
# <span data-ttu-id="8bc58-101">Get-AzureRmSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="8bc58-101">Get-AzureRmSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="8bc58-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8bc58-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc58-103">Получает геоизбыточную резервную копию базы данных.</span><span class="sxs-lookup"><span data-stu-id="8bc58-103">Gets a geo-redundant backup of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bc58-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8bc58-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bc58-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bc58-105">DESCRIPTION</span></span>
<span data-ttu-id="8bc58-106">Командлет **Get-AzureRMSqlDatabaseGeoBackup** получает указанную геоизбыточную резервную копию базы данных SQL или все доступные геоизбыточные резервные копии на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="8bc58-106">The **Get-AzureRMSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>

<span data-ttu-id="8bc58-107">Резервная копия с геоизбыточным резервированием — это ресурс restorable с использованием файлов данных из отдельного географического расположения.</span><span class="sxs-lookup"><span data-stu-id="8bc58-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="8bc58-108">Вы можете использовать Geo-Restore для восстановления геоизбыточной резервной копии в случае сбоя в регионе, чтобы восстановить базу данных в новом регионе.</span><span class="sxs-lookup"><span data-stu-id="8bc58-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>

<span data-ttu-id="8bc58-109">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc58-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8bc58-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8bc58-110">EXAMPLES</span></span>

### <span data-ttu-id="8bc58-111">Пример 1: получение всех геоизбыточных резервных копий на сервере</span><span class="sxs-lookup"><span data-stu-id="8bc58-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="8bc58-112">Эта команда получает все доступные резервные копии с геоизбыточным хранилищем на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="8bc58-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="8bc58-113">Пример 2: получение указанной геоизбыточной резервной копии</span><span class="sxs-lookup"><span data-stu-id="8bc58-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="8bc58-114">Эта команда возвращает геоизбыточное резервное копирование базы данных с именем ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="8bc58-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

## <span data-ttu-id="8bc58-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8bc58-115">PARAMETERS</span></span>

### <span data-ttu-id="8bc58-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8bc58-116">-DatabaseName</span></span>
<span data-ttu-id="8bc58-117">Указывает имя базы данных, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="8bc58-117">Specifies the name of the database to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc58-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc58-118">-DefaultProfile</span></span>
<span data-ttu-id="8bc58-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8bc58-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bc58-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bc58-120">-ResourceGroupName</span></span>
<span data-ttu-id="8bc58-121">Указывает имя группы ресурсов, которой назначен сервер базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="8bc58-121">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc58-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="8bc58-122">-ServerName</span></span>
<span data-ttu-id="8bc58-123">Указывает имя сервера, на котором размещается резервная копия для восстановления.</span><span class="sxs-lookup"><span data-stu-id="8bc58-123">Specifies the name of the server that hosts the backup to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc58-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bc58-124">-Confirm</span></span>
<span data-ttu-id="8bc58-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8bc58-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc58-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bc58-126">-WhatIf</span></span>
<span data-ttu-id="8bc58-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8bc58-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bc58-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8bc58-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc58-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc58-129">CommonParameters</span></span>
<span data-ttu-id="8bc58-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8bc58-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc58-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bc58-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc58-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8bc58-132">INPUTS</span></span>

### <span data-ttu-id="8bc58-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="8bc58-133">None</span></span>
<span data-ttu-id="8bc58-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8bc58-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8bc58-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bc58-135">OUTPUTS</span></span>

### <span data-ttu-id="8bc58-136">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="8bc58-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="8bc58-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="8bc58-137">NOTES</span></span>

## <span data-ttu-id="8bc58-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bc58-138">RELATED LINKS</span></span>

[<span data-ttu-id="8bc58-139">Обзор: бесперебойная работа в облаке и аварийное восстановление базы данных с помощью базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="8bc58-139">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="8bc58-140">Восстановление базы данных SQL Azure из сбоя</span><span class="sxs-lookup"><span data-stu-id="8bc58-140">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="8bc58-141">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8bc58-141">Restore-AzureRmSqlDatabase</span></span>](./Restore-AzureRmSqlDatabase.md)

[<span data-ttu-id="8bc58-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="8bc58-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
