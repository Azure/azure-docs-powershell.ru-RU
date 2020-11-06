---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: a3eff47b688f2f426c4f255d400ce1ef73c3c027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559879"
---
# <span data-ttu-id="18440-101">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="18440-101">Add-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="18440-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18440-102">SYNOPSIS</span></span>
<span data-ttu-id="18440-103">Добавляет источник данных в учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="18440-103">Adds a data source to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18440-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18440-104">SYNTAX</span></span>

### <span data-ttu-id="18440-105">Добавление учетной записи Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="18440-105">Add a Data Lake storage account</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18440-106">Добавление учетной записи хранилища BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="18440-106">Add a Blob storage account</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18440-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18440-107">DESCRIPTION</span></span>
<span data-ttu-id="18440-108">Командлет **Add-AzureRmDataLakeAnalyticsDataSource** добавляет источник данных в учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="18440-108">The **Add-AzureRmDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="18440-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18440-109">EXAMPLES</span></span>

### <span data-ttu-id="18440-110">Пример 1: Добавление источника данных в учетную запись</span><span class="sxs-lookup"><span data-stu-id="18440-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="18440-111">Эта команда добавляет источник данных Data Lake Store в учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="18440-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="18440-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18440-112">PARAMETERS</span></span>

### <span data-ttu-id="18440-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="18440-113">-AccessKey</span></span>
<span data-ttu-id="18440-114">Задает клавишу доступа для учетной записи хранилища BLOB-объектов Azure, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="18440-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Blob storage account
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18440-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="18440-115">-Account</span></span>
<span data-ttu-id="18440-116">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="18440-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="18440-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="18440-117">-Blob</span></span>
<span data-ttu-id="18440-118">Указывает имя учетной записи хранилища BLOB-объектов Azure, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="18440-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18440-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="18440-119">-DataLakeStore</span></span>
<span data-ttu-id="18440-120">Указывает имя учетной записи для Azure Data Lake Store, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="18440-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Data Lake storage account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18440-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18440-121">-ResourceGroupName</span></span>
<span data-ttu-id="18440-122">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="18440-122">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18440-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18440-123">-DefaultProfile</span></span>
<span data-ttu-id="18440-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18440-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18440-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18440-125">CommonParameters</span></span>
<span data-ttu-id="18440-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18440-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18440-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18440-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18440-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18440-128">INPUTS</span></span>

## <span data-ttu-id="18440-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18440-129">OUTPUTS</span></span>

### <span data-ttu-id="18440-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="18440-130">None</span></span>

## <span data-ttu-id="18440-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="18440-131">NOTES</span></span>

## <span data-ttu-id="18440-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18440-132">RELATED LINKS</span></span>

[<span data-ttu-id="18440-133">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="18440-133">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="18440-134">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="18440-134">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


