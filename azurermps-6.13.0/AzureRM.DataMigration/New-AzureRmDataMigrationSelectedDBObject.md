---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSelectedDBObject.md
ms.openlocfilehash: d8303dadef33944addf63323e57727ef85acce6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732110"
---
# <span data-ttu-id="611bf-101">New-AzureRmDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="611bf-101">New-AzureRmDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="611bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="611bf-102">SYNOPSIS</span></span>
<span data-ttu-id="611bf-103">Создает объект ввода базы данных, содержащий сведения об исходной и целевой базах данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="611bf-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="611bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="611bf-104">SYNTAX</span></span>

### <span data-ttu-id="611bf-105">MigrateSqlServerSqlDb (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="611bf-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzureRmDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="611bf-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="611bf-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzureRmDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="611bf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="611bf-107">DESCRIPTION</span></span>
<span data-ttu-id="611bf-108">Командлет New-AzureRmDataMigrationSelectedDB создает объект сведений о базе данных, содержащий сведения об исходных и целевых базах данных, а также о сопоставлениях таблиц для миграции.</span><span class="sxs-lookup"><span data-stu-id="611bf-108">The New-AzureRmDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="611bf-109">Этот командлет можно использовать в качестве параметра с помощью командлета New-AzureRmDataMigrationTask.</span><span class="sxs-lookup"><span data-stu-id="611bf-109">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="611bf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="611bf-110">EXAMPLES</span></span>

### <span data-ttu-id="611bf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="611bf-111">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```


### <span data-ttu-id="611bf-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="611bf-112">Example 2</span></span>
```
PS C:\> New-AzureRmDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```


## <span data-ttu-id="611bf-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="611bf-113">PARAMETERS</span></span>

### <span data-ttu-id="611bf-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="611bf-114">-BackupFileShare</span></span>
<span data-ttu-id="611bf-115">Файловый общий доступ, для которого необходимо создать резервную копию файлов базы данных исходного сервера для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="611bf-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="611bf-116">Используйте этот параметр, чтобы переопределить общие сведения о файле для каждой базы данных.</span><span class="sxs-lookup"><span data-stu-id="611bf-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="611bf-117">Используйте полное доменное имя для сервера.</span><span class="sxs-lookup"><span data-stu-id="611bf-117">Use fully qualified domain name for the server.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.FileShare
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="611bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="611bf-118">-DefaultProfile</span></span>
<span data-ttu-id="611bf-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="611bf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611bf-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="611bf-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="611bf-121">Настройка базы данных в режим только для чтения перед миграцией</span><span class="sxs-lookup"><span data-stu-id="611bf-121">Set Database to readonly before migration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611bf-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="611bf-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="611bf-123">Задайте для миграции тип SQL Server в базу данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="611bf-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611bf-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="611bf-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="611bf-125">Задайте для миграции тип SQL Server в SQL DB MI Migration.</span><span class="sxs-lookup"><span data-stu-id="611bf-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611bf-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="611bf-126">-SourceDatabaseName</span></span>
<span data-ttu-id="611bf-127">Имя исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="611bf-127">The name of the source database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611bf-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="611bf-128">-TableMap</span></span>
<span data-ttu-id="611bf-129">Сопоставление исходного кода с целевыми таблицами</span><span class="sxs-lookup"><span data-stu-id="611bf-129">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611bf-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="611bf-130">-TargetDatabaseName</span></span>
<span data-ttu-id="611bf-131">Имя целевой базы данных.</span><span class="sxs-lookup"><span data-stu-id="611bf-131">The name of the target database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="611bf-132">CommonParameters</span></span>
<span data-ttu-id="611bf-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="611bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="611bf-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="611bf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="611bf-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="611bf-135">INPUTS</span></span>

### <span data-ttu-id="611bf-136">Microsoft. Azure. Management. remigrations. Models. \ мои</span><span class="sxs-lookup"><span data-stu-id="611bf-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="611bf-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="611bf-137">OUTPUTS</span></span>

### <span data-ttu-id="611bf-138">Microsoft. Azure. Management. Migration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="611bf-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="611bf-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="611bf-139">NOTES</span></span>

## <span data-ttu-id="611bf-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="611bf-140">RELATED LINKS</span></span>
