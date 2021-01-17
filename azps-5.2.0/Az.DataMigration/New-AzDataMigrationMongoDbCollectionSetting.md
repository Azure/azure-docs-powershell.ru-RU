---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402927"
---
# <span data-ttu-id="a75fe-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="a75fe-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="a75fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a75fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a75fe-103">Создает параметры сбора для миграции в соответствии с миграцией mongoDb.</span><span class="sxs-lookup"><span data-stu-id="a75fe-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="a75fe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a75fe-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="a75fe-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a75fe-105">DESCRIPTION</span></span>
<span data-ttu-id="a75fe-106">С New-AzDataMigrationMongoDbCollectionSetting создается объект параметров миграции, который определяет пропускную способность и поведение удаления.</span><span class="sxs-lookup"><span data-stu-id="a75fe-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="a75fe-107">Выходные данные, которые можно выдать, являются парой ключевых значений с именем коллекции и значением параметра.</span><span class="sxs-lookup"><span data-stu-id="a75fe-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="a75fe-108">Выходные данные используются для сборки параметров миграции на уровне базы данных.</span><span class="sxs-lookup"><span data-stu-id="a75fe-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="a75fe-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a75fe-109">EXAMPLES</span></span>

### <span data-ttu-id="a75fe-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a75fe-110">Example 1</span></span>
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

## <span data-ttu-id="a75fe-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a75fe-111">PARAMETERS</span></span>

### <span data-ttu-id="a75fe-112">-Name</span><span class="sxs-lookup"><span data-stu-id="a75fe-112">-Name</span></span>
<span data-ttu-id="a75fe-113">Имя коллекции</span><span class="sxs-lookup"><span data-stu-id="a75fe-113">Name of the collection</span></span>

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

### <span data-ttu-id="a75fe-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="a75fe-114">-ShardKey</span></span>
<span data-ttu-id="a75fe-115">Разделенный запятой список разделов.</span><span class="sxs-lookup"><span data-stu-id="a75fe-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="a75fe-116">Для целевого показателя mongoDb вы можете указать порядок нажатия ключа «ShardKeyName:Order», где для hashed задан порядок 1, -1 или пустой, например "_id,email:-1".</span><span class="sxs-lookup"><span data-stu-id="a75fe-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="a75fe-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="a75fe-117">-TargetRequestUnit</span></span>
<span data-ttu-id="a75fe-118">Значение единицы специального запроса коллекции.</span><span class="sxs-lookup"><span data-stu-id="a75fe-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="a75fe-119">Если она не за установлена, в коллекции используется общая база данных RU.</span><span class="sxs-lookup"><span data-stu-id="a75fe-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="a75fe-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="a75fe-120">-CanDelete</span></span>
<span data-ttu-id="a75fe-121">Должны ли удаляться целевые данные, если этот переключатель установлен, они будут удалены при миграции</span><span class="sxs-lookup"><span data-stu-id="a75fe-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="a75fe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a75fe-122">CommonParameters</span></span>
<span data-ttu-id="a75fe-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a75fe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a75fe-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a75fe-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a75fe-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a75fe-125">INPUTS</span></span>

### <span data-ttu-id="a75fe-126">Нет</span><span class="sxs-lookup"><span data-stu-id="a75fe-126">None</span></span>

## <span data-ttu-id="a75fe-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a75fe-127">OUTPUTS</span></span>

### <span data-ttu-id="a75fe-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="a75fe-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="a75fe-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a75fe-129">NOTES</span></span>

## <span data-ttu-id="a75fe-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a75fe-130">RELATED LINKS</span></span>
