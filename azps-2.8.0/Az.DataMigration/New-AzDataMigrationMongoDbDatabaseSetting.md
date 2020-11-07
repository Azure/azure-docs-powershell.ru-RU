---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: d05b6507ea8e1d5244e23ab7b8b6222848a1d088
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721237"
---
# <span data-ttu-id="2d0cb-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="2d0cb-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="2d0cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d0cb-102">SYNOPSIS</span></span>
<span data-ttu-id="2d0cb-103">Создание параметров базы данных для миграции для миграции mongoDb</span><span class="sxs-lookup"><span data-stu-id="2d0cb-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="2d0cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d0cb-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="2d0cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d0cb-105">DESCRIPTION</span></span>
<span data-ttu-id="2d0cb-106">Командлет New-AzDataMigrationMongoDbDatabaseSetting создает объект параметра миграции, который определяет параметры пропускной способности и удаления.</span><span class="sxs-lookup"><span data-stu-id="2d0cb-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="2d0cb-107">Вывод — это пара значений ключа с именем коллекции и значением параметра, которые можно использовать при вызове задачи миграции.</span><span class="sxs-lookup"><span data-stu-id="2d0cb-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="2d0cb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d0cb-108">EXAMPLES</span></span>

### <span data-ttu-id="2d0cb-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2d0cb-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="2d0cb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d0cb-110">PARAMETERS</span></span>

### <span data-ttu-id="2d0cb-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d0cb-111">-Name</span></span>
<span data-ttu-id="2d0cb-112">Имя базы данных</span><span class="sxs-lookup"><span data-stu-id="2d0cb-112">Name of the database</span></span>

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
### <span data-ttu-id="2d0cb-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="2d0cb-113">-TargetRequestUnit</span></span>
<span data-ttu-id="2d0cb-114">Значение единицы запроса выделенного уровня базы данных.</span><span class="sxs-lookup"><span data-stu-id="2d0cb-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="2d0cb-115">Если не установлено, в этой коллекции используется общая база данных RU.</span><span class="sxs-lookup"><span data-stu-id="2d0cb-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="2d0cb-116">-Коллекции</span><span class="sxs-lookup"><span data-stu-id="2d0cb-116">-Collections</span></span>
<span data-ttu-id="2d0cb-117">Массив объектов параметров коллекции MongoDb, возвращенных с помощью вызова New-AzureRmDmsMongoDbDatabaseSetting.</span><span class="sxs-lookup"><span data-stu-id="2d0cb-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="2d0cb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d0cb-118">CommonParameters</span></span>
<span data-ttu-id="2d0cb-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d0cb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d0cb-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d0cb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d0cb-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d0cb-121">INPUTS</span></span>

### <span data-ttu-id="2d0cb-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="2d0cb-122">None</span></span>

## <span data-ttu-id="2d0cb-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d0cb-123">OUTPUTS</span></span>

### <span data-ttu-id="2d0cb-124">Microsoft. Azure. Commands. Migration. Models. MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="2d0cb-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="2d0cb-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d0cb-125">NOTES</span></span>

## <span data-ttu-id="2d0cb-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d0cb-126">RELATED LINKS</span></span>
