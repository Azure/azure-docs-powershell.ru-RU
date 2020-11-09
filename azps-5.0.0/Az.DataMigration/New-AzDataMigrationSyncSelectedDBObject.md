---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313109"
---
# <span data-ttu-id="7388f-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="7388f-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="7388f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7388f-102">SYNOPSIS</span></span>
<span data-ttu-id="7388f-103">Создает объект сведений о базе данных, специфичный для сценария синхронизации, который будет использоваться для задачи миграции.</span><span class="sxs-lookup"><span data-stu-id="7388f-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="7388f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7388f-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7388f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7388f-105">DESCRIPTION</span></span>

<span data-ttu-id="7388f-106">Командлет New-AzDataMigrationSyncSelectedDB создает объект сведений о базе данных, специфичный для сценария синхронизации, который включает сведения о исходной и целевой базах данных.</span><span class="sxs-lookup"><span data-stu-id="7388f-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="7388f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7388f-107">EXAMPLES</span></span>

### <span data-ttu-id="7388f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7388f-108">Example 1</span></span>
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

<span data-ttu-id="7388f-109">В этом примере создается объект метаданных базы данных, описывающий параметры миграции для $DatabaseName в базу данных $DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="7388f-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="7388f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7388f-110">PARAMETERS</span></span>

### <span data-ttu-id="7388f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7388f-111">-DefaultProfile</span></span>
<span data-ttu-id="7388f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7388f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7388f-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="7388f-113">-MigrationSetting</span></span>
<span data-ttu-id="7388f-114">Параметры миграции для настройки поведения миграции</span><span class="sxs-lookup"><span data-stu-id="7388f-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="7388f-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7388f-115">-SchemaName</span></span>
<span data-ttu-id="7388f-116">Имя схемы для миграции</span><span class="sxs-lookup"><span data-stu-id="7388f-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="7388f-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7388f-117">-SourceDatabaseName</span></span>
<span data-ttu-id="7388f-118">Имя исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="7388f-118">The name of the source database.</span></span>

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

### <span data-ttu-id="7388f-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="7388f-119">-SourceSetting</span></span>
<span data-ttu-id="7388f-120">Параметры источника для настройки поведения миграции исходной конечной точки</span><span class="sxs-lookup"><span data-stu-id="7388f-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="7388f-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="7388f-121">-TableMap</span></span>
<span data-ttu-id="7388f-122">Сопоставление исходного кода с целевыми таблицами</span><span class="sxs-lookup"><span data-stu-id="7388f-122">Mapping of source to target tables</span></span>

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

### <span data-ttu-id="7388f-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7388f-123">-TargetDatabaseName</span></span>
<span data-ttu-id="7388f-124">Имя целевой базы данных.</span><span class="sxs-lookup"><span data-stu-id="7388f-124">The name of the target database</span></span>

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

### <span data-ttu-id="7388f-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="7388f-125">-TargetSetting</span></span>
<span data-ttu-id="7388f-126">Целевые параметры для настройки поведения миграции целевой конечной точки</span><span class="sxs-lookup"><span data-stu-id="7388f-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="7388f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7388f-127">CommonParameters</span></span>
<span data-ttu-id="7388f-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7388f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7388f-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7388f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7388f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7388f-130">INPUTS</span></span>

### <span data-ttu-id="7388f-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="7388f-131">None</span></span>

## <span data-ttu-id="7388f-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7388f-132">OUTPUTS</span></span>

### <span data-ttu-id="7388f-133">Microsoft. Azure. Management. Migration. Models. MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="7388f-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="7388f-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="7388f-134">NOTES</span></span>

## <span data-ttu-id="7388f-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7388f-135">RELATED LINKS</span></span>