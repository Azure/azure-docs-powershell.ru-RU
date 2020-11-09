---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313151"
---
# <span data-ttu-id="fc9db-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="fc9db-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="fc9db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc9db-102">SYNOPSIS</span></span>
<span data-ttu-id="fc9db-103">Создание параметров коллекции для миграции в соответствии с mongoDb миграции</span><span class="sxs-lookup"><span data-stu-id="fc9db-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="fc9db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc9db-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="fc9db-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc9db-105">DESCRIPTION</span></span>
<span data-ttu-id="fc9db-106">Командлет New-AzDataMigrationMongoDbCollectionSetting создает объект параметра миграции, который определяет параметры пропускной способности и удаления.</span><span class="sxs-lookup"><span data-stu-id="fc9db-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="fc9db-107">Выходные данные командлетом является пара значение ключа с именем коллекции и значением параметра.</span><span class="sxs-lookup"><span data-stu-id="fc9db-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="fc9db-108">Выходные данные используются при сборке параметров уровня базы данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="fc9db-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="fc9db-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc9db-109">EXAMPLES</span></span>

### <span data-ttu-id="fc9db-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc9db-110">Example 1</span></span>
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## <span data-ttu-id="fc9db-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc9db-111">PARAMETERS</span></span>

### <span data-ttu-id="fc9db-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fc9db-112">-Name</span></span>
<span data-ttu-id="fc9db-113">Имя коллекции</span><span class="sxs-lookup"><span data-stu-id="fc9db-113">Name of the collection</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9db-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="fc9db-114">-ShardKey</span></span>
<span data-ttu-id="fc9db-115">Список ключей сегментов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="fc9db-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="fc9db-116">Для целевого объекта mongoDb можно задать порядковый номер ключа сегмента "ShardKeyName: Order", где порядковый номер 1,-1 или Empty для хеширования, например "_id, адрес электронной почты:-1".</span><span class="sxs-lookup"><span data-stu-id="fc9db-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9db-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="fc9db-117">-TargetRequestUnit</span></span>
<span data-ttu-id="fc9db-118">Выделенное значение единицы запроса коллекции.</span><span class="sxs-lookup"><span data-stu-id="fc9db-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="fc9db-119">Если не установлено, в этой коллекции используется общая база данных RU.</span><span class="sxs-lookup"><span data-stu-id="fc9db-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="fc9db-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="fc9db-120">-CanDelete</span></span>
<span data-ttu-id="fc9db-121">Следует ли удалять целевые данные, если переключатель установлен, он будет очищен при миграции</span><span class="sxs-lookup"><span data-stu-id="fc9db-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="fc9db-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc9db-122">CommonParameters</span></span>
<span data-ttu-id="fc9db-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc9db-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc9db-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc9db-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc9db-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc9db-125">INPUTS</span></span>

### <span data-ttu-id="fc9db-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="fc9db-126">None</span></span>

## <span data-ttu-id="fc9db-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc9db-127">OUTPUTS</span></span>

### <span data-ttu-id="fc9db-128">Microsoft. Azure. Commands. Migration. Models. MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="fc9db-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="fc9db-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc9db-129">NOTES</span></span>

## <span data-ttu-id="fc9db-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc9db-130">RELATED LINKS</span></span>