---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationsqlserversqldbselecteddb
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
ms.openlocfilehash: 1be43b5d08011a71ec093df2f93c63dd04c6004d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563564"
---
# <span data-ttu-id="b2b94-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span><span class="sxs-lookup"><span data-stu-id="b2b94-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span></span>

## <span data-ttu-id="b2b94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2b94-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b94-103">Создает объект MigrateSqlServerSqlDbDatabaseInput, содержащий сведения об исходной и целевой базах данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="b2b94-103">Creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2b94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2b94-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSqlServerSqlDbSelectedDB [-Id <String>] [-Name <String>] [-TargetDatabaseName <String>]
 [-MakeSourceDbReadOnly] [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="b2b94-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2b94-105">DESCRIPTION</span></span>
<span data-ttu-id="b2b94-106">Командлет New-AzureRmDataMigrationSqlServerSqlDbSelectedDB создает объект MigrateSqlServerSqlDbDatabaseInput, содержащий сведения об исходных и целевых базах данных, а также о сопоставлениях таблиц для миграции.</span><span class="sxs-lookup"><span data-stu-id="b2b94-106">The New-AzureRmDataMigrationSqlServerSqlDbSelectedDB cmdlet creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="b2b94-107">Этот командлет можно использовать в качестве параметра с помощью командлета New-AzureRmDataMigrationTask.</span><span class="sxs-lookup"><span data-stu-id="b2b94-107">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="b2b94-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2b94-108">EXAMPLES</span></span>

### <span data-ttu-id="b2b94-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b2b94-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSqlServerSqlDbSelectedDB  -Name AdventuerWorks2016 -TargetDatabaseName AdventureWorks2016
 -MakeSourceDbReadOnly -TableMap $tableMap
```

<span data-ttu-id="b2b94-110">В приведенном выше примере создается объект MigrateSqlServerSqlDbDatabaseInput для переноса базы данных **AdventureWorks2016** в базу данных SQL Azure с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="b2b94-110">The above example creates MigrateSqlServerSqlDbDatabaseInput object for migrating the **AdventureWorks2016** database to a SQL Azure database with the same name.</span></span>

## <span data-ttu-id="b2b94-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2b94-111">PARAMETERS</span></span>

### <span data-ttu-id="b2b94-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2b94-112">-Confirm</span></span>
<span data-ttu-id="b2b94-113">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b2b94-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b94-114">-DefaultProfile</span></span>
<span data-ttu-id="b2b94-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2b94-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b94-116">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="b2b94-116">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="b2b94-117">Настройка базы данных в режим только для чтения перед миграцией</span><span class="sxs-lookup"><span data-stu-id="b2b94-117">Set Database to readonly before migration</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b94-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2b94-118">-Name</span></span>
<span data-ttu-id="b2b94-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="b2b94-119">The name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b94-120">-TableMap</span><span class="sxs-lookup"><span data-stu-id="b2b94-120">-TableMap</span></span>
<span data-ttu-id="b2b94-121">Сопоставление исходного кода с целевыми таблицами</span><span class="sxs-lookup"><span data-stu-id="b2b94-121">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b94-122">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b2b94-122">-TargetDatabaseName</span></span>
<span data-ttu-id="b2b94-123">Имя целевой базы данных.</span><span class="sxs-lookup"><span data-stu-id="b2b94-123">The name of the target Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="b2b94-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2b94-124">INPUTS</span></span>

### <span data-ttu-id="b2b94-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="b2b94-125">None</span></span>


## <span data-ttu-id="b2b94-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2b94-126">OUTPUTS</span></span>

### <span data-ttu-id="b2b94-127">Microsoft. Azure. Management. Migration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="b2b94-127">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>


## <span data-ttu-id="b2b94-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2b94-128">NOTES</span></span>

## <span data-ttu-id="b2b94-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2b94-129">RELATED LINKS</span></span>


