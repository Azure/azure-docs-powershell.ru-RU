---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420855"
---
# <span data-ttu-id="ab496-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="ab496-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="ab496-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab496-102">SYNOPSIS</span></span>
<span data-ttu-id="ab496-103">Создание информационного объекта базы данных, специального для сценария синхронизации, который будет использоваться для задачи миграции.</span><span class="sxs-lookup"><span data-stu-id="ab496-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="ab496-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ab496-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab496-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab496-105">DESCRIPTION</span></span>

<span data-ttu-id="ab496-106">С New-AzDataMigrationSyncSelectedDB создается объект сведений базы данных, специфичный для сценария синхронизации, содержащий сведения об исходных и целевых базах данных.</span><span class="sxs-lookup"><span data-stu-id="ab496-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="ab496-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ab496-107">EXAMPLES</span></span>

### <span data-ttu-id="ab496-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ab496-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="ab496-109">В этом примере создается объект метаданных базы данных, описывающий параметры переноса $DatabaseName в $DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="ab496-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="ab496-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab496-110">PARAMETERS</span></span>

### <span data-ttu-id="ab496-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab496-111">-DefaultProfile</span></span>
<span data-ttu-id="ab496-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab496-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab496-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="ab496-113">-MigrationSetting</span></span>
<span data-ttu-id="ab496-114">Параметры миграции, которые настраивают поведение миграции</span><span class="sxs-lookup"><span data-stu-id="ab496-114">Migration settings which tune the migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab496-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ab496-115">-SchemaName</span></span>
<span data-ttu-id="ab496-116">Имя схемы, которое нужно перенести</span><span class="sxs-lookup"><span data-stu-id="ab496-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="ab496-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ab496-117">-SourceDatabaseName</span></span>
<span data-ttu-id="ab496-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ab496-118">The name of the source database.</span></span>

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

### <span data-ttu-id="ab496-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="ab496-119">-SourceSetting</span></span>
<span data-ttu-id="ab496-120">Параметры источника для настройки поведения при миграции исходных конечных точек</span><span class="sxs-lookup"><span data-stu-id="ab496-120">Source settings to tune source endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab496-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="ab496-121">-TableMap</span></span>
<span data-ttu-id="ab496-122">Сопоставление источника с целевыми таблицами</span><span class="sxs-lookup"><span data-stu-id="ab496-122">Mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab496-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ab496-123">-TargetDatabaseName</span></span>
<span data-ttu-id="ab496-124">Имя целевой базы данных</span><span class="sxs-lookup"><span data-stu-id="ab496-124">The name of the target database</span></span>

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

### <span data-ttu-id="ab496-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="ab496-125">-TargetSetting</span></span>
<span data-ttu-id="ab496-126">Настройка целевых параметров для настройки поведения конечной конечной точки</span><span class="sxs-lookup"><span data-stu-id="ab496-126">Target settings to tune target endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab496-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab496-127">CommonParameters</span></span>
<span data-ttu-id="ab496-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab496-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab496-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab496-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab496-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab496-130">INPUTS</span></span>

### <span data-ttu-id="ab496-131">Нет</span><span class="sxs-lookup"><span data-stu-id="ab496-131">None</span></span>

## <span data-ttu-id="ab496-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ab496-132">OUTPUTS</span></span>

### <span data-ttu-id="ab496-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="ab496-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="ab496-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ab496-134">NOTES</span></span>

## <span data-ttu-id="ab496-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab496-135">RELATED LINKS</span></span>
