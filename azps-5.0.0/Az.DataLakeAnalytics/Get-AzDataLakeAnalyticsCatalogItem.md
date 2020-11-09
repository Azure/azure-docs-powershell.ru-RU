---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313625"
---
# <span data-ttu-id="a9682-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="a9682-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="a9682-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9682-102">SYNOPSIS</span></span>
<span data-ttu-id="a9682-103">Возвращает элемент каталога Data Lake Analytics или типы элементов.</span><span class="sxs-lookup"><span data-stu-id="a9682-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="a9682-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9682-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9682-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9682-105">DESCRIPTION</span></span>
<span data-ttu-id="a9682-106">Команда **Get-AzDataLakeAnalyticsCatalogItem** получает указанный элемент каталога Azure Data Lake Analytics или получает элементы каталога указанного типа.</span><span class="sxs-lookup"><span data-stu-id="a9682-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="a9682-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9682-107">EXAMPLES</span></span>

### <span data-ttu-id="a9682-108">Пример 1: получение указанной базы данных</span><span class="sxs-lookup"><span data-stu-id="a9682-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="a9682-109">Эта команда получает указанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="a9682-109">This command gets the specified database.</span></span>

### <span data-ttu-id="a9682-110">Пример 2: получение таблиц в указанной базе данных и схеме</span><span class="sxs-lookup"><span data-stu-id="a9682-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="a9682-111">Эта команда возвращает список таблиц в указанной базе данных.</span><span class="sxs-lookup"><span data-stu-id="a9682-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="a9682-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9682-112">PARAMETERS</span></span>

### <span data-ttu-id="a9682-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="a9682-113">-Account</span></span>
<span data-ttu-id="a9682-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a9682-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a9682-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9682-115">-DefaultProfile</span></span>
<span data-ttu-id="a9682-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a9682-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9682-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="a9682-117">-ItemType</span></span>
<span data-ttu-id="a9682-118">Указывает тип элемента каталога для выбранных или указанных элементов.</span><span class="sxs-lookup"><span data-stu-id="a9682-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="a9682-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a9682-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a9682-120">База</span><span class="sxs-lookup"><span data-stu-id="a9682-120">Database</span></span>
- <span data-ttu-id="a9682-121">Схемы</span><span class="sxs-lookup"><span data-stu-id="a9682-121">Schema</span></span>
- <span data-ttu-id="a9682-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="a9682-122">Assembly</span></span>
- <span data-ttu-id="a9682-123">Таблич</span><span class="sxs-lookup"><span data-stu-id="a9682-123">Table</span></span>
- <span data-ttu-id="a9682-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="a9682-124">TableValuedFunction</span></span>
- <span data-ttu-id="a9682-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="a9682-125">TableStatistics</span></span>
- <span data-ttu-id="a9682-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="a9682-126">ExternalDataSource</span></span>
- <span data-ttu-id="a9682-127">Технический</span><span class="sxs-lookup"><span data-stu-id="a9682-127">View</span></span>
- <span data-ttu-id="a9682-128">Процедур</span><span class="sxs-lookup"><span data-stu-id="a9682-128">Procedure</span></span>
- <span data-ttu-id="a9682-129">Скрыт</span><span class="sxs-lookup"><span data-stu-id="a9682-129">Secret</span></span>
- <span data-ttu-id="a9682-130">Член</span><span class="sxs-lookup"><span data-stu-id="a9682-130">Credential</span></span>
- <span data-ttu-id="a9682-131">Лично</span><span class="sxs-lookup"><span data-stu-id="a9682-131">Types</span></span>
- <span data-ttu-id="a9682-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="a9682-132">TablePartition</span></span>

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

### <span data-ttu-id="a9682-133">-Path</span><span class="sxs-lookup"><span data-stu-id="a9682-133">-Path</span></span>
<span data-ttu-id="a9682-134">Задает многокомпонентный путь к извлекаемому элементу или к родительскому элементу списка элементов.</span><span class="sxs-lookup"><span data-stu-id="a9682-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="a9682-135">Части пути должны быть разделены точкой (.).</span><span class="sxs-lookup"><span data-stu-id="a9682-135">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="a9682-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9682-136">CommonParameters</span></span>
<span data-ttu-id="a9682-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9682-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9682-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9682-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9682-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9682-139">INPUTS</span></span>

### <span data-ttu-id="a9682-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a9682-140">System.String</span></span>

### <span data-ttu-id="a9682-141">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="a9682-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="a9682-142">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="a9682-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="a9682-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9682-143">OUTPUTS</span></span>

### <span data-ttu-id="a9682-144">Microsoft. Azure. Management. данных Lake. Analytics. Models. CatalogItem</span><span class="sxs-lookup"><span data-stu-id="a9682-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="a9682-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9682-145">NOTES</span></span>

## <span data-ttu-id="a9682-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9682-146">RELATED LINKS</span></span>

[<span data-ttu-id="a9682-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="a9682-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


