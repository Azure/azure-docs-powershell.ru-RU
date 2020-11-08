---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242819"
---
# <span data-ttu-id="31875-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="31875-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="31875-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31875-102">SYNOPSIS</span></span>
<span data-ttu-id="31875-103">Создание параметров базы данных для миграции для миграции mongoDb</span><span class="sxs-lookup"><span data-stu-id="31875-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="31875-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31875-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="31875-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31875-105">DESCRIPTION</span></span>
<span data-ttu-id="31875-106">Командлет New-AzDataMigrationMongoDbDatabaseSetting создает объект параметра миграции, который определяет параметры пропускной способности и удаления.</span><span class="sxs-lookup"><span data-stu-id="31875-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="31875-107">Вывод — это пара значений ключа с именем коллекции и значением параметра, которые можно использовать при вызове задачи миграции.</span><span class="sxs-lookup"><span data-stu-id="31875-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="31875-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31875-108">EXAMPLES</span></span>

### <span data-ttu-id="31875-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31875-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="31875-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31875-110">PARAMETERS</span></span>

### <span data-ttu-id="31875-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31875-111">-Name</span></span>
<span data-ttu-id="31875-112">Имя базы данных</span><span class="sxs-lookup"><span data-stu-id="31875-112">Name of the database</span></span>

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
### <span data-ttu-id="31875-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="31875-113">-TargetRequestUnit</span></span>
<span data-ttu-id="31875-114">Значение единицы запроса выделенного уровня базы данных.</span><span class="sxs-lookup"><span data-stu-id="31875-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="31875-115">Если не установлено, в этой коллекции используется общая база данных RU.</span><span class="sxs-lookup"><span data-stu-id="31875-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="31875-116">-Коллекции</span><span class="sxs-lookup"><span data-stu-id="31875-116">-Collections</span></span>
<span data-ttu-id="31875-117">Массив объектов параметров коллекции MongoDb, возвращенных с помощью вызова New-AzureRmDmsMongoDbDatabaseSetting.</span><span class="sxs-lookup"><span data-stu-id="31875-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="31875-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31875-118">CommonParameters</span></span>
<span data-ttu-id="31875-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31875-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31875-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31875-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31875-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31875-121">INPUTS</span></span>

### <span data-ttu-id="31875-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="31875-122">None</span></span>

## <span data-ttu-id="31875-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31875-123">OUTPUTS</span></span>

### <span data-ttu-id="31875-124">Microsoft. Azure. Commands. Migration. Models. MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="31875-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="31875-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="31875-125">NOTES</span></span>

## <span data-ttu-id="31875-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31875-126">RELATED LINKS</span></span>
