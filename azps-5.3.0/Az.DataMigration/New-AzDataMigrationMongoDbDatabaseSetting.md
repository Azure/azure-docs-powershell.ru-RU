---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426519"
---
# <span data-ttu-id="69c8f-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="69c8f-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="69c8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="69c8f-103">Создание параметра базы данных для миграции для миграции mongoDb</span><span class="sxs-lookup"><span data-stu-id="69c8f-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="69c8f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="69c8f-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="69c8f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69c8f-105">DESCRIPTION</span></span>
<span data-ttu-id="69c8f-106">С New-AzDataMigrationMongoDbDatabaseSetting создается объект параметров миграции, который определяет пропускную способность и поведение удаления.</span><span class="sxs-lookup"><span data-stu-id="69c8f-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="69c8f-107">Выходные данные являются парой ключевых значений с именем коллекции и значением параметра, который можно использовать при создании задачи миграции.</span><span class="sxs-lookup"><span data-stu-id="69c8f-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="69c8f-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="69c8f-108">EXAMPLES</span></span>

### <span data-ttu-id="69c8f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="69c8f-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="69c8f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69c8f-110">PARAMETERS</span></span>

### <span data-ttu-id="69c8f-111">-Name</span><span class="sxs-lookup"><span data-stu-id="69c8f-111">-Name</span></span>
<span data-ttu-id="69c8f-112">Имя базы данных</span><span class="sxs-lookup"><span data-stu-id="69c8f-112">Name of the database</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="69c8f-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="69c8f-113">-TargetRequestUnit</span></span>
<span data-ttu-id="69c8f-114">Значение единицы запроса на уровне выделенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="69c8f-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="69c8f-115">Если она не за установлена, в коллекции используется общая база данных RU.</span><span class="sxs-lookup"><span data-stu-id="69c8f-115">If not set, that collection uses shared database RU.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c8f-116">-Коллекции</span><span class="sxs-lookup"><span data-stu-id="69c8f-116">-Collections</span></span>
<span data-ttu-id="69c8f-117">Массив параметров коллекции MongoDb, возвращенный функцией New-AzureRmDmsMongoDbDatabaseSetting звонка.</span><span class="sxs-lookup"><span data-stu-id="69c8f-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

```yaml
Type: System.Collections.Generic.KeyValuePair<string, MongoDbCollectionSettings>[]
Parameter Sets: (All)
Aliases: colls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c8f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c8f-118">CommonParameters</span></span>
<span data-ttu-id="69c8f-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69c8f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c8f-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69c8f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c8f-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69c8f-121">INPUTS</span></span>

### <span data-ttu-id="69c8f-122">Нет</span><span class="sxs-lookup"><span data-stu-id="69c8f-122">None</span></span>

## <span data-ttu-id="69c8f-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69c8f-123">OUTPUTS</span></span>

### <span data-ttu-id="69c8f-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="69c8f-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="69c8f-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="69c8f-125">NOTES</span></span>

## <span data-ttu-id="69c8f-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69c8f-126">RELATED LINKS</span></span>
