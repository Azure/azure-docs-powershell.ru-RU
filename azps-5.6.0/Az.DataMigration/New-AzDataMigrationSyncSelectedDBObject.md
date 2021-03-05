---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: 6fa95473091afe991eac90ad87d7321b8401a8be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996803"
---
# <span data-ttu-id="3eb2e-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="3eb2e-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="3eb2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eb2e-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb2e-103">Создание информационного объекта базы данных, специального для сценария синхронизации, который будет использоваться для задачи миграции.</span><span class="sxs-lookup"><span data-stu-id="3eb2e-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="3eb2e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3eb2e-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eb2e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3eb2e-105">DESCRIPTION</span></span>

<span data-ttu-id="3eb2e-106">С New-AzDataMigrationSyncSelectedDB создается объект сведений базы данных, специфичный для сценария синхронизации, содержащий сведения об исходных и целевых базах данных.</span><span class="sxs-lookup"><span data-stu-id="3eb2e-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="3eb2e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3eb2e-107">EXAMPLES</span></span>

### <span data-ttu-id="3eb2e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3eb2e-108">Example 1</span></span>
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

<span data-ttu-id="3eb2e-109">В этом примере создается объект метаданных базы данных, описывающий параметры переноса $DatabaseName в $DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="3eb2e-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="3eb2e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3eb2e-110">PARAMETERS</span></span>

### <span data-ttu-id="3eb2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb2e-111">-DefaultProfile</span></span>
<span data-ttu-id="3eb2e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3eb2e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eb2e-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="3eb2e-113">-MigrationSetting</span></span>
<span data-ttu-id="3eb2e-114">Параметры миграции, которые настраивают поведение миграции</span><span class="sxs-lookup"><span data-stu-id="3eb2e-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="3eb2e-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3eb2e-115">-SchemaName</span></span>
<span data-ttu-id="3eb2e-116">Имя схемы, которое нужно перенести</span><span class="sxs-lookup"><span data-stu-id="3eb2e-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="3eb2e-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3eb2e-117">-SourceDatabaseName</span></span>
<span data-ttu-id="3eb2e-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="3eb2e-118">The name of the source database.</span></span>

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

### <span data-ttu-id="3eb2e-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="3eb2e-119">-SourceSetting</span></span>
<span data-ttu-id="3eb2e-120">Параметры источника для настройки поведения при миграции исходных конечных точек</span><span class="sxs-lookup"><span data-stu-id="3eb2e-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="3eb2e-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="3eb2e-121">-TableMap</span></span>
<span data-ttu-id="3eb2e-122">Сопоставление источника с целевыми таблицами</span><span class="sxs-lookup"><span data-stu-id="3eb2e-122">Mapping of source to target tables</span></span>

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

### <span data-ttu-id="3eb2e-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3eb2e-123">-TargetDatabaseName</span></span>
<span data-ttu-id="3eb2e-124">Имя целевой базы данных</span><span class="sxs-lookup"><span data-stu-id="3eb2e-124">The name of the target database</span></span>

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

### <span data-ttu-id="3eb2e-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="3eb2e-125">-TargetSetting</span></span>
<span data-ttu-id="3eb2e-126">Настройка целевых параметров для настройки поведения конечной конечной точки</span><span class="sxs-lookup"><span data-stu-id="3eb2e-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="3eb2e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb2e-127">CommonParameters</span></span>
<span data-ttu-id="3eb2e-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eb2e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb2e-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb2e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb2e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3eb2e-130">INPUTS</span></span>

### <span data-ttu-id="3eb2e-131">Нет</span><span class="sxs-lookup"><span data-stu-id="3eb2e-131">None</span></span>

## <span data-ttu-id="3eb2e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3eb2e-132">OUTPUTS</span></span>

### <span data-ttu-id="3eb2e-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="3eb2e-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="3eb2e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3eb2e-134">NOTES</span></span>

## <span data-ttu-id="3eb2e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3eb2e-135">RELATED LINKS</span></span>
