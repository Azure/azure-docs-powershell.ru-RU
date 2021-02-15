---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 0e4557f44d3219b55edc0bd31464033e9000c772
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211137"
---
# <span data-ttu-id="6bb2d-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="6bb2d-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="6bb2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bb2d-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb2d-103">Создает объект ввода базы данных, содержащий сведения об исходных и целевых базах данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="6bb2d-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="6bb2d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6bb2d-104">SYNTAX</span></span>

### <span data-ttu-id="6bb2d-105">MigrateSqlServerSqlDb (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6bb2d-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bb2d-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="6bb2d-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bb2d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bb2d-107">DESCRIPTION</span></span>
<span data-ttu-id="6bb2d-108">С New-AzDataMigrationSelectedDB создается объект сведений базы данных, содержащий сведения об исходных и целевых базах данных, а также сопоставления таблиц для миграции.</span><span class="sxs-lookup"><span data-stu-id="6bb2d-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="6bb2d-109">Этот cmdlet можно использовать в качестве параметра с New-AzDataMigrationTask.</span><span class="sxs-lookup"><span data-stu-id="6bb2d-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="6bb2d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6bb2d-110">EXAMPLES</span></span>

### <span data-ttu-id="6bb2d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6bb2d-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="6bb2d-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6bb2d-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="6bb2d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bb2d-113">PARAMETERS</span></span>

### <span data-ttu-id="6bb2d-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="6bb2d-114">-BackupFileShare</span></span>
<span data-ttu-id="6bb2d-115">Файловая папка, в которой должны быть архивы исходных серверных файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="6bb2d-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="6bb2d-116">Используйте этот параметр, чтобы переопределить сведения о доступе к файлам для каждой базы данных.</span><span class="sxs-lookup"><span data-stu-id="6bb2d-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="6bb2d-117">Используйте для сервера полное доменное имя.</span><span class="sxs-lookup"><span data-stu-id="6bb2d-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="6bb2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb2d-118">-DefaultProfile</span></span>
<span data-ttu-id="6bb2d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6bb2d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bb2d-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="6bb2d-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="6bb2d-121">Настройка системы для чтения базы данных перед миграцией</span><span class="sxs-lookup"><span data-stu-id="6bb2d-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="6bb2d-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="6bb2d-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="6bb2d-123">Заведите тип миграции SQL Server SQL DB.</span><span class="sxs-lookup"><span data-stu-id="6bb2d-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="6bb2d-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="6bb2d-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="6bb2d-125">Заведите тип миграции SQL Server миграции SQL DB MI.</span><span class="sxs-lookup"><span data-stu-id="6bb2d-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="6bb2d-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6bb2d-126">-SourceDatabaseName</span></span>
<span data-ttu-id="6bb2d-127">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="6bb2d-127">The name of the source database.</span></span>

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

### <span data-ttu-id="6bb2d-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="6bb2d-128">-TableMap</span></span>
<span data-ttu-id="6bb2d-129">Сопоставление источника с целевыми таблицами</span><span class="sxs-lookup"><span data-stu-id="6bb2d-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="6bb2d-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6bb2d-130">-TargetDatabaseName</span></span>
<span data-ttu-id="6bb2d-131">Имя целевой базы данных.</span><span class="sxs-lookup"><span data-stu-id="6bb2d-131">The name of the target database.</span></span>

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

### <span data-ttu-id="6bb2d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb2d-132">CommonParameters</span></span>
<span data-ttu-id="6bb2d-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bb2d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb2d-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bb2d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb2d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bb2d-135">INPUTS</span></span>

### <span data-ttu-id="6bb2d-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span><span class="sxs-lookup"><span data-stu-id="6bb2d-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="6bb2d-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6bb2d-137">OUTPUTS</span></span>

### <span data-ttu-id="6bb2d-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="6bb2d-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="6bb2d-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6bb2d-139">NOTES</span></span>

## <span data-ttu-id="6bb2d-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6bb2d-140">RELATED LINKS</span></span>
