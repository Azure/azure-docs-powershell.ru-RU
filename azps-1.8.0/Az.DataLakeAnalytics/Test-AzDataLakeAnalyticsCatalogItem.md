---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 03289ddc0b3d51ea73ee13609650665b458a7acb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900814"
---
# <span data-ttu-id="cfc1e-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="cfc1e-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="cfc1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cfc1e-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc1e-103">Проверка существования элемента каталога.</span><span class="sxs-lookup"><span data-stu-id="cfc1e-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="cfc1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cfc1e-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfc1e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfc1e-105">DESCRIPTION</span></span>
<span data-ttu-id="cfc1e-106">Командлет **Test-AzDataLakeAnalyticsCatalogItem** проверяет наличие элемента каталога Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cfc1e-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="cfc1e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cfc1e-107">EXAMPLES</span></span>

### <span data-ttu-id="cfc1e-108">Пример 1: Проверка наличия элемента каталога</span><span class="sxs-lookup"><span data-stu-id="cfc1e-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="cfc1e-109">Эта команда проверяет, существует ли указанный элемент схемы.</span><span class="sxs-lookup"><span data-stu-id="cfc1e-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="cfc1e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cfc1e-110">PARAMETERS</span></span>

### <span data-ttu-id="cfc1e-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="cfc1e-111">-Account</span></span>
<span data-ttu-id="cfc1e-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cfc1e-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="cfc1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc1e-113">-DefaultProfile</span></span>
<span data-ttu-id="cfc1e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cfc1e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfc1e-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="cfc1e-115">-ItemType</span></span>
<span data-ttu-id="cfc1e-116">Указывает тип элемента каталога для элемента, который нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="cfc1e-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="cfc1e-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cfc1e-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfc1e-118">База</span><span class="sxs-lookup"><span data-stu-id="cfc1e-118">Database</span></span>
- <span data-ttu-id="cfc1e-119">Схемы</span><span class="sxs-lookup"><span data-stu-id="cfc1e-119">Schema</span></span>
- <span data-ttu-id="cfc1e-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="cfc1e-120">Assembly</span></span>
- <span data-ttu-id="cfc1e-121">Таблич</span><span class="sxs-lookup"><span data-stu-id="cfc1e-121">Table</span></span>
- <span data-ttu-id="cfc1e-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="cfc1e-122">TablePartition</span></span>
- <span data-ttu-id="cfc1e-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="cfc1e-123">TableValuedFunction</span></span>
- <span data-ttu-id="cfc1e-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="cfc1e-124">TableStatistics</span></span>
- <span data-ttu-id="cfc1e-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="cfc1e-125">ExternalDataSource</span></span>
- <span data-ttu-id="cfc1e-126">Технический</span><span class="sxs-lookup"><span data-stu-id="cfc1e-126">View</span></span>
- <span data-ttu-id="cfc1e-127">Процедур</span><span class="sxs-lookup"><span data-stu-id="cfc1e-127">Procedure</span></span>
- <span data-ttu-id="cfc1e-128">Скрыт</span><span class="sxs-lookup"><span data-stu-id="cfc1e-128">Secret</span></span>
- <span data-ttu-id="cfc1e-129">Член</span><span class="sxs-lookup"><span data-stu-id="cfc1e-129">Credential</span></span>
- <span data-ttu-id="cfc1e-130">Лично</span><span class="sxs-lookup"><span data-stu-id="cfc1e-130">Types</span></span>

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

### <span data-ttu-id="cfc1e-131">-Path</span><span class="sxs-lookup"><span data-stu-id="cfc1e-131">-Path</span></span>
<span data-ttu-id="cfc1e-132">Задает путь к извлекаемому элементу или путь к родительскому элементу для списка элементов.</span><span class="sxs-lookup"><span data-stu-id="cfc1e-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfc1e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc1e-133">CommonParameters</span></span>
<span data-ttu-id="cfc1e-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cfc1e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc1e-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfc1e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc1e-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cfc1e-136">INPUTS</span></span>

### <span data-ttu-id="cfc1e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cfc1e-137">System.String</span></span>

### <span data-ttu-id="cfc1e-138">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="cfc1e-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="cfc1e-139">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="cfc1e-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="cfc1e-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfc1e-140">OUTPUTS</span></span>

### <span data-ttu-id="cfc1e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cfc1e-141">System.Boolean</span></span>

## <span data-ttu-id="cfc1e-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="cfc1e-142">NOTES</span></span>

## <span data-ttu-id="cfc1e-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfc1e-143">RELATED LINKS</span></span>

[<span data-ttu-id="cfc1e-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="cfc1e-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


