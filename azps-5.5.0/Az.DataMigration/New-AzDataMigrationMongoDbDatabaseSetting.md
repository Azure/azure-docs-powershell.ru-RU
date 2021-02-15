---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230612"
---
# <span data-ttu-id="172cd-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="172cd-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="172cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="172cd-102">SYNOPSIS</span></span>
<span data-ttu-id="172cd-103">Создание параметра базы данных для миграции для миграции mongoDb</span><span class="sxs-lookup"><span data-stu-id="172cd-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="172cd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="172cd-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="172cd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="172cd-105">DESCRIPTION</span></span>
<span data-ttu-id="172cd-106">С New-AzDataMigrationMongoDbDatabaseSetting создается объект параметров миграции, который определяет пропускную способность и поведение удаления.</span><span class="sxs-lookup"><span data-stu-id="172cd-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="172cd-107">Выходные данные являются парой ключевых значений с именем коллекции и значением параметра, который может использоваться при создании задачи миграции.</span><span class="sxs-lookup"><span data-stu-id="172cd-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="172cd-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="172cd-108">EXAMPLES</span></span>

### <span data-ttu-id="172cd-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="172cd-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="172cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="172cd-110">PARAMETERS</span></span>

### <span data-ttu-id="172cd-111">-Name</span><span class="sxs-lookup"><span data-stu-id="172cd-111">-Name</span></span>
<span data-ttu-id="172cd-112">Имя базы данных</span><span class="sxs-lookup"><span data-stu-id="172cd-112">Name of the database</span></span>

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
### <span data-ttu-id="172cd-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="172cd-113">-TargetRequestUnit</span></span>
<span data-ttu-id="172cd-114">Выделенное значение единицы запроса на уровне базы данных.</span><span class="sxs-lookup"><span data-stu-id="172cd-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="172cd-115">Если она не за установлена, в этой коллекции используется общая база данных RU.</span><span class="sxs-lookup"><span data-stu-id="172cd-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="172cd-116">-Коллекции</span><span class="sxs-lookup"><span data-stu-id="172cd-116">-Collections</span></span>
<span data-ttu-id="172cd-117">Массив параметров коллекции MongoDb, возвращаемого New-AzureRmDmsMongoDbDatabaseSetting звонка.</span><span class="sxs-lookup"><span data-stu-id="172cd-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="172cd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172cd-118">CommonParameters</span></span>
<span data-ttu-id="172cd-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="172cd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172cd-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="172cd-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172cd-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="172cd-121">INPUTS</span></span>

### <span data-ttu-id="172cd-122">Нет</span><span class="sxs-lookup"><span data-stu-id="172cd-122">None</span></span>

## <span data-ttu-id="172cd-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="172cd-123">OUTPUTS</span></span>

### <span data-ttu-id="172cd-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="172cd-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="172cd-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="172cd-125">NOTES</span></span>

## <span data-ttu-id="172cd-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="172cd-126">RELATED LINKS</span></span>
