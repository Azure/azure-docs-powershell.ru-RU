---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066842"
---
# <span data-ttu-id="3835e-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="3835e-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="3835e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3835e-102">SYNOPSIS</span></span>
<span data-ttu-id="3835e-103">Возвращает элемент каталога Data Lake Analytics или типы элементов.</span><span class="sxs-lookup"><span data-stu-id="3835e-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="3835e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3835e-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3835e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3835e-105">DESCRIPTION</span></span>
<span data-ttu-id="3835e-106">Команда **Get-AzDataLakeAnalyticsCatalogItem** получает указанный элемент каталога Azure Data Lake Analytics или получает элементы каталога указанного типа.</span><span class="sxs-lookup"><span data-stu-id="3835e-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="3835e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3835e-107">EXAMPLES</span></span>

### <span data-ttu-id="3835e-108">Пример 1: получение указанной базы данных</span><span class="sxs-lookup"><span data-stu-id="3835e-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="3835e-109">Эта команда получает указанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="3835e-109">This command gets the specified database.</span></span>

### <span data-ttu-id="3835e-110">Пример 2: получение таблиц в указанной базе данных и схеме</span><span class="sxs-lookup"><span data-stu-id="3835e-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="3835e-111">Эта команда возвращает список таблиц в указанной базе данных.</span><span class="sxs-lookup"><span data-stu-id="3835e-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="3835e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3835e-112">PARAMETERS</span></span>

### <span data-ttu-id="3835e-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="3835e-113">-Account</span></span>
<span data-ttu-id="3835e-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3835e-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="3835e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3835e-115">-DefaultProfile</span></span>
<span data-ttu-id="3835e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3835e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3835e-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="3835e-117">-ItemType</span></span>
<span data-ttu-id="3835e-118">Указывает тип элемента каталога для выбранных или указанных элементов.</span><span class="sxs-lookup"><span data-stu-id="3835e-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="3835e-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3835e-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3835e-120">База</span><span class="sxs-lookup"><span data-stu-id="3835e-120">Database</span></span>
- <span data-ttu-id="3835e-121">Схемы</span><span class="sxs-lookup"><span data-stu-id="3835e-121">Schema</span></span>
- <span data-ttu-id="3835e-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="3835e-122">Assembly</span></span>
- <span data-ttu-id="3835e-123">Таблич</span><span class="sxs-lookup"><span data-stu-id="3835e-123">Table</span></span>
- <span data-ttu-id="3835e-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="3835e-124">TableValuedFunction</span></span>
- <span data-ttu-id="3835e-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="3835e-125">TableStatistics</span></span>
- <span data-ttu-id="3835e-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="3835e-126">ExternalDataSource</span></span>
- <span data-ttu-id="3835e-127">Технический</span><span class="sxs-lookup"><span data-stu-id="3835e-127">View</span></span>
- <span data-ttu-id="3835e-128">Процедур</span><span class="sxs-lookup"><span data-stu-id="3835e-128">Procedure</span></span>
- <span data-ttu-id="3835e-129">Скрыт</span><span class="sxs-lookup"><span data-stu-id="3835e-129">Secret</span></span>
- <span data-ttu-id="3835e-130">Член</span><span class="sxs-lookup"><span data-stu-id="3835e-130">Credential</span></span>
- <span data-ttu-id="3835e-131">Лично</span><span class="sxs-lookup"><span data-stu-id="3835e-131">Types</span></span>
- <span data-ttu-id="3835e-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="3835e-132">TablePartition</span></span>

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

### <span data-ttu-id="3835e-133">-Path</span><span class="sxs-lookup"><span data-stu-id="3835e-133">-Path</span></span>
<span data-ttu-id="3835e-134">Задает многокомпонентный путь к извлекаемому элементу или к родительскому элементу списка элементов.</span><span class="sxs-lookup"><span data-stu-id="3835e-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="3835e-135">Части пути должны быть разделены точкой (.).</span><span class="sxs-lookup"><span data-stu-id="3835e-135">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="3835e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3835e-136">CommonParameters</span></span>
<span data-ttu-id="3835e-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3835e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3835e-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3835e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3835e-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3835e-139">INPUTS</span></span>

### <span data-ttu-id="3835e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3835e-140">System.String</span></span>

### <span data-ttu-id="3835e-141">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="3835e-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="3835e-142">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="3835e-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="3835e-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3835e-143">OUTPUTS</span></span>

### <span data-ttu-id="3835e-144">Microsoft. Azure. Management. данных Lake. Analytics. Models. CatalogItem</span><span class="sxs-lookup"><span data-stu-id="3835e-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="3835e-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="3835e-145">NOTES</span></span>

## <span data-ttu-id="3835e-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3835e-146">RELATED LINKS</span></span>

[<span data-ttu-id="3835e-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="3835e-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


