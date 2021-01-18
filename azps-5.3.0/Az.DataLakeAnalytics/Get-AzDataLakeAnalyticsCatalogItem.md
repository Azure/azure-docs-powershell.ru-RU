---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518869"
---
# <span data-ttu-id="a092d-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="a092d-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="a092d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a092d-102">SYNOPSIS</span></span>
<span data-ttu-id="a092d-103">Возвращает элемент каталога или типы элементов в средстве анализа для озера Данных.</span><span class="sxs-lookup"><span data-stu-id="a092d-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="a092d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a092d-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a092d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a092d-105">DESCRIPTION</span></span>
<span data-ttu-id="a092d-106">**Get-AzDataLakeAnalyticsCatalogItem** получает указанный элемент каталога Azure Data Lake Analytics или возвращает элементы каталога указанного типа.</span><span class="sxs-lookup"><span data-stu-id="a092d-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="a092d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a092d-107">EXAMPLES</span></span>

### <span data-ttu-id="a092d-108">Пример 1. Получить указанную базу данных</span><span class="sxs-lookup"><span data-stu-id="a092d-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="a092d-109">Эта команда получает указанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="a092d-109">This command gets the specified database.</span></span>

### <span data-ttu-id="a092d-110">Пример 2. Доступ к таблицам в указанной базе данных и схеме</span><span class="sxs-lookup"><span data-stu-id="a092d-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="a092d-111">Эта команда получает список таблиц в указанной базе данных.</span><span class="sxs-lookup"><span data-stu-id="a092d-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="a092d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a092d-112">PARAMETERS</span></span>

### <span data-ttu-id="a092d-113">-Account</span><span class="sxs-lookup"><span data-stu-id="a092d-113">-Account</span></span>
<span data-ttu-id="a092d-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a092d-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a092d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a092d-115">-DefaultProfile</span></span>
<span data-ttu-id="a092d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a092d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a092d-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="a092d-117">-ItemType</span></span>
<span data-ttu-id="a092d-118">Определяет тип элемента каталога, извлекаемого или указанного в списке.</span><span class="sxs-lookup"><span data-stu-id="a092d-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="a092d-119">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="a092d-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a092d-120">База данных</span><span class="sxs-lookup"><span data-stu-id="a092d-120">Database</span></span>
- <span data-ttu-id="a092d-121">Схема</span><span class="sxs-lookup"><span data-stu-id="a092d-121">Schema</span></span>
- <span data-ttu-id="a092d-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="a092d-122">Assembly</span></span>
- <span data-ttu-id="a092d-123">Таблица</span><span class="sxs-lookup"><span data-stu-id="a092d-123">Table</span></span>
- <span data-ttu-id="a092d-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="a092d-124">TableValuedFunction</span></span>
- <span data-ttu-id="a092d-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="a092d-125">TableStatistics</span></span>
- <span data-ttu-id="a092d-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="a092d-126">ExternalDataSource</span></span>
- <span data-ttu-id="a092d-127">"Вид"</span><span class="sxs-lookup"><span data-stu-id="a092d-127">View</span></span>
- <span data-ttu-id="a092d-128">Процедура</span><span class="sxs-lookup"><span data-stu-id="a092d-128">Procedure</span></span>
- <span data-ttu-id="a092d-129">Секретная</span><span class="sxs-lookup"><span data-stu-id="a092d-129">Secret</span></span>
- <span data-ttu-id="a092d-130">Учетные данные</span><span class="sxs-lookup"><span data-stu-id="a092d-130">Credential</span></span>
- <span data-ttu-id="a092d-131">Типы</span><span class="sxs-lookup"><span data-stu-id="a092d-131">Types</span></span>
- <span data-ttu-id="a092d-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="a092d-132">TablePartition</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a092d-133">-Path</span><span class="sxs-lookup"><span data-stu-id="a092d-133">-Path</span></span>
<span data-ttu-id="a092d-134">Путь к элементу с несколькими элементами, которые нужно извлечь, или к родительскому элементу элементов списка.</span><span class="sxs-lookup"><span data-stu-id="a092d-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="a092d-135">Части пути должны быть разделены точками (.).</span><span class="sxs-lookup"><span data-stu-id="a092d-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a092d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a092d-136">CommonParameters</span></span>
<span data-ttu-id="a092d-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a092d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a092d-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a092d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a092d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a092d-139">INPUTS</span></span>

### <span data-ttu-id="a092d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a092d-140">System.String</span></span>

### <span data-ttu-id="a092d-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="a092d-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="a092d-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="a092d-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="a092d-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a092d-143">OUTPUTS</span></span>

### <span data-ttu-id="a092d-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span><span class="sxs-lookup"><span data-stu-id="a092d-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="a092d-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a092d-145">NOTES</span></span>

## <span data-ttu-id="a092d-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a092d-146">RELATED LINKS</span></span>

[<span data-ttu-id="a092d-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="a092d-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


