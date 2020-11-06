---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/add-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 1f2fe13567bd17170fd73854ce5554a693210c7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561863"
---
# <span data-ttu-id="1c4f8-101">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1c4f8-101">Add-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="1c4f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="1c4f8-103">Добавляет источник данных в учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1c4f8-103">Adds a data source to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c4f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c4f8-104">SYNTAX</span></span>

### <span data-ttu-id="1c4f8-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c4f8-105">AddDataLakeStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c4f8-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c4f8-106">AddBlobStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c4f8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c4f8-107">DESCRIPTION</span></span>
<span data-ttu-id="1c4f8-108">Командлет **Add-AzureRmDataLakeAnalyticsDataSource** добавляет источник данных в учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1c4f8-108">The **Add-AzureRmDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1c4f8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c4f8-109">EXAMPLES</span></span>

### <span data-ttu-id="1c4f8-110">Пример 1: Добавление источника данных в учетную запись</span><span class="sxs-lookup"><span data-stu-id="1c4f8-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="1c4f8-111">Эта команда добавляет источник данных Data Lake Store в учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1c4f8-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="1c4f8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c4f8-112">PARAMETERS</span></span>

### <span data-ttu-id="1c4f8-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="1c4f8-113">-AccessKey</span></span>
<span data-ttu-id="1c4f8-114">Задает клавишу доступа для учетной записи хранилища BLOB-объектов Azure, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="1c4f8-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddBlobStorageAccount
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c4f8-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="1c4f8-115">-Account</span></span>
<span data-ttu-id="1c4f8-116">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1c4f8-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="1c4f8-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="1c4f8-117">-Blob</span></span>
<span data-ttu-id="1c4f8-118">Указывает имя учетной записи хранилища BLOB-объектов Azure, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="1c4f8-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c4f8-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1c4f8-119">-DataLakeStore</span></span>
<span data-ttu-id="1c4f8-120">Указывает имя учетной записи для Azure Data Lake Store, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="1c4f8-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddDataLakeStorageAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c4f8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c4f8-121">-DefaultProfile</span></span>
<span data-ttu-id="1c4f8-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1c4f8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c4f8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c4f8-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c4f8-124">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1c4f8-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c4f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c4f8-125">CommonParameters</span></span>
<span data-ttu-id="1c4f8-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c4f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c4f8-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c4f8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c4f8-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c4f8-128">INPUTS</span></span>

### <span data-ttu-id="1c4f8-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="1c4f8-129">None</span></span>
<span data-ttu-id="1c4f8-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1c4f8-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c4f8-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c4f8-131">OUTPUTS</span></span>

### <span data-ttu-id="1c4f8-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="1c4f8-132">None</span></span>

## <span data-ttu-id="1c4f8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c4f8-133">NOTES</span></span>

## <span data-ttu-id="1c4f8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c4f8-134">RELATED LINKS</span></span>

[<span data-ttu-id="1c4f8-135">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1c4f8-135">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="1c4f8-136">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1c4f8-136">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


