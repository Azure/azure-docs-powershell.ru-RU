---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b7a608e4bed6e68f06660f10f2ef72effb6ad18b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732540"
---
# <span data-ttu-id="7b2da-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="7b2da-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="7b2da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b2da-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2da-103">Возвращает элемент каталога Data Lake Analytics или типы элементов.</span><span class="sxs-lookup"><span data-stu-id="7b2da-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b2da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b2da-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b2da-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b2da-105">DESCRIPTION</span></span>
<span data-ttu-id="7b2da-106">Команда **Get-AzureRmDataLakeAnalyticsCatalogItem** получает указанный элемент каталога Azure Data Lake Analytics или получает элементы каталога указанного типа.</span><span class="sxs-lookup"><span data-stu-id="7b2da-106">The **Get-AzureRmDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="7b2da-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b2da-107">EXAMPLES</span></span>

### <span data-ttu-id="7b2da-108">Пример 1: получение указанной базы данных</span><span class="sxs-lookup"><span data-stu-id="7b2da-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="7b2da-109">Эта команда получает указанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="7b2da-109">This command gets the specified database.</span></span>

### <span data-ttu-id="7b2da-110">Пример 2: получение таблиц в указанной базе данных и схеме</span><span class="sxs-lookup"><span data-stu-id="7b2da-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="7b2da-111">Эта команда возвращает список таблиц в указанной базе данных.</span><span class="sxs-lookup"><span data-stu-id="7b2da-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="7b2da-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b2da-112">PARAMETERS</span></span>

### <span data-ttu-id="7b2da-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="7b2da-113">-Account</span></span>
<span data-ttu-id="7b2da-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7b2da-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b2da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2da-115">-DefaultProfile</span></span>
<span data-ttu-id="7b2da-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7b2da-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b2da-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="7b2da-117">-ItemType</span></span>
<span data-ttu-id="7b2da-118">Указывает тип элемента каталога для выбранных или указанных элементов.</span><span class="sxs-lookup"><span data-stu-id="7b2da-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="7b2da-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7b2da-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b2da-120">База</span><span class="sxs-lookup"><span data-stu-id="7b2da-120">Database</span></span>
- <span data-ttu-id="7b2da-121">Схемы</span><span class="sxs-lookup"><span data-stu-id="7b2da-121">Schema</span></span>
- <span data-ttu-id="7b2da-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="7b2da-122">Assembly</span></span>
- <span data-ttu-id="7b2da-123">Таблич</span><span class="sxs-lookup"><span data-stu-id="7b2da-123">Table</span></span>
- <span data-ttu-id="7b2da-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="7b2da-124">TableValuedFunction</span></span>
- <span data-ttu-id="7b2da-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="7b2da-125">TableStatistics</span></span>
- <span data-ttu-id="7b2da-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="7b2da-126">ExternalDataSource</span></span>
- <span data-ttu-id="7b2da-127">Технический</span><span class="sxs-lookup"><span data-stu-id="7b2da-127">View</span></span>
- <span data-ttu-id="7b2da-128">Процедур</span><span class="sxs-lookup"><span data-stu-id="7b2da-128">Procedure</span></span>
- <span data-ttu-id="7b2da-129">Скрыт</span><span class="sxs-lookup"><span data-stu-id="7b2da-129">Secret</span></span>
- <span data-ttu-id="7b2da-130">Член</span><span class="sxs-lookup"><span data-stu-id="7b2da-130">Credential</span></span>
- <span data-ttu-id="7b2da-131">Лично</span><span class="sxs-lookup"><span data-stu-id="7b2da-131">Types</span></span>
- <span data-ttu-id="7b2da-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="7b2da-132">TablePartition</span></span>

```yaml
Type: CatalogItemType
Parameter Sets: (All)
Aliases: 
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b2da-133">-Path</span><span class="sxs-lookup"><span data-stu-id="7b2da-133">-Path</span></span>
<span data-ttu-id="7b2da-134">Задает многокомпонентный путь к извлекаемому элементу или к родительскому элементу списка элементов.</span><span class="sxs-lookup"><span data-stu-id="7b2da-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="7b2da-135">Части пути должны быть разделены точкой (.).</span><span class="sxs-lookup"><span data-stu-id="7b2da-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b2da-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2da-136">CommonParameters</span></span>
<span data-ttu-id="7b2da-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b2da-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2da-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b2da-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2da-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b2da-139">INPUTS</span></span>

### <span data-ttu-id="7b2da-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="7b2da-140">None</span></span>
<span data-ttu-id="7b2da-141">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7b2da-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b2da-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b2da-142">OUTPUTS</span></span>

### <span data-ttu-id="7b2da-143">CatalogItem</span><span class="sxs-lookup"><span data-stu-id="7b2da-143">CatalogItem</span></span>
<span data-ttu-id="7b2da-144">Указанный элемент каталога.</span><span class="sxs-lookup"><span data-stu-id="7b2da-144">The specified catalog item.</span></span>

### <span data-ttu-id="7b2da-145">Список<CatalogItem></span><span class="sxs-lookup"><span data-stu-id="7b2da-145">List<CatalogItem></span></span>
<span data-ttu-id="7b2da-146">Список указанных элементов каталога под соответствующим контейнером.</span><span class="sxs-lookup"><span data-stu-id="7b2da-146">The list of the specified catalog items underneath their corresponding container.</span></span>

## <span data-ttu-id="7b2da-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b2da-147">NOTES</span></span>

## <span data-ttu-id="7b2da-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b2da-148">RELATED LINKS</span></span>

[<span data-ttu-id="7b2da-149">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="7b2da-149">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


