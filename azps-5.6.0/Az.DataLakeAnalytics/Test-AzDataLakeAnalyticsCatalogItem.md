---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2642a310e2a318498b3d170b463ac7e366bf5818
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957336"
---
# <span data-ttu-id="e58ef-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="e58ef-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="e58ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e58ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e58ef-103">Проверяет наличие элемента каталога.</span><span class="sxs-lookup"><span data-stu-id="e58ef-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="e58ef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e58ef-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e58ef-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e58ef-105">DESCRIPTION</span></span>
<span data-ttu-id="e58ef-106">**Cmdlet Test-AzDataLakeAnalyticsCatalogItem** проверяет наличие элемента каталога Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e58ef-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="e58ef-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e58ef-107">EXAMPLES</span></span>

### <span data-ttu-id="e58ef-108">Пример 1. Проверка на существования элемента каталога</span><span class="sxs-lookup"><span data-stu-id="e58ef-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="e58ef-109">Эта команда проверяет, существует ли указанный элемент схемы.</span><span class="sxs-lookup"><span data-stu-id="e58ef-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="e58ef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e58ef-110">PARAMETERS</span></span>

### <span data-ttu-id="e58ef-111">-Account</span><span class="sxs-lookup"><span data-stu-id="e58ef-111">-Account</span></span>
<span data-ttu-id="e58ef-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e58ef-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e58ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e58ef-113">-DefaultProfile</span></span>
<span data-ttu-id="e58ef-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e58ef-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e58ef-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="e58ef-115">-ItemType</span></span>
<span data-ttu-id="e58ef-116">Определяет тип элемента каталога для проверки.</span><span class="sxs-lookup"><span data-stu-id="e58ef-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="e58ef-117">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="e58ef-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e58ef-118">База данных</span><span class="sxs-lookup"><span data-stu-id="e58ef-118">Database</span></span>
- <span data-ttu-id="e58ef-119">Схема</span><span class="sxs-lookup"><span data-stu-id="e58ef-119">Schema</span></span>
- <span data-ttu-id="e58ef-120">Сборка</span><span class="sxs-lookup"><span data-stu-id="e58ef-120">Assembly</span></span>
- <span data-ttu-id="e58ef-121">Таблица</span><span class="sxs-lookup"><span data-stu-id="e58ef-121">Table</span></span>
- <span data-ttu-id="e58ef-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="e58ef-122">TablePartition</span></span>
- <span data-ttu-id="e58ef-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="e58ef-123">TableValuedFunction</span></span>
- <span data-ttu-id="e58ef-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="e58ef-124">TableStatistics</span></span>
- <span data-ttu-id="e58ef-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="e58ef-125">ExternalDataSource</span></span>
- <span data-ttu-id="e58ef-126">"Вид"</span><span class="sxs-lookup"><span data-stu-id="e58ef-126">View</span></span>
- <span data-ttu-id="e58ef-127">Процедура</span><span class="sxs-lookup"><span data-stu-id="e58ef-127">Procedure</span></span>
- <span data-ttu-id="e58ef-128">Секретная</span><span class="sxs-lookup"><span data-stu-id="e58ef-128">Secret</span></span>
- <span data-ttu-id="e58ef-129">Учетные данные</span><span class="sxs-lookup"><span data-stu-id="e58ef-129">Credential</span></span>
- <span data-ttu-id="e58ef-130">Типы</span><span class="sxs-lookup"><span data-stu-id="e58ef-130">Types</span></span>

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

### <span data-ttu-id="e58ef-131">-Path</span><span class="sxs-lookup"><span data-stu-id="e58ef-131">-Path</span></span>
<span data-ttu-id="e58ef-132">Путь к элементу, извлекаемого из списка, или путь к родительскому элементу элемента списка.</span><span class="sxs-lookup"><span data-stu-id="e58ef-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="e58ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e58ef-133">CommonParameters</span></span>
<span data-ttu-id="e58ef-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e58ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e58ef-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e58ef-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e58ef-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e58ef-136">INPUTS</span></span>

### <span data-ttu-id="e58ef-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e58ef-137">System.String</span></span>

### <span data-ttu-id="e58ef-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="e58ef-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="e58ef-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="e58ef-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="e58ef-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e58ef-140">OUTPUTS</span></span>

### <span data-ttu-id="e58ef-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e58ef-141">System.Boolean</span></span>

## <span data-ttu-id="e58ef-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e58ef-142">NOTES</span></span>

## <span data-ttu-id="e58ef-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e58ef-143">RELATED LINKS</span></span>

[<span data-ttu-id="e58ef-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="e58ef-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


