---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: b7f2c6f2077d0b7e9c7510f6984ada15a65d6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734866"
---
# <span data-ttu-id="241d5-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="241d5-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="241d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="241d5-102">SYNOPSIS</span></span>
<span data-ttu-id="241d5-103">Возвращает источник данных Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="241d5-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="241d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="241d5-104">SYNTAX</span></span>

### <span data-ttu-id="241d5-105">Список всех источников данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="241d5-105">List all data sources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="241d5-106">Получение учетной записи для Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="241d5-106">Get a Data Lake Store account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="241d5-107">Получение учетной записи хранилища BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="241d5-107">Get a Blob storage account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="241d5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="241d5-108">DESCRIPTION</span></span>
<span data-ttu-id="241d5-109">Командлет **Get-AzureRmDataLakeAnalyticsDataSource** получает источник данных Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="241d5-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="241d5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="241d5-110">EXAMPLES</span></span>

### <span data-ttu-id="241d5-111">Пример 1: получение источника данных из учетной записи</span><span class="sxs-lookup"><span data-stu-id="241d5-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="241d5-112">Эта команда получает источник данных Data Lake Store с именем ContosoAdls из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="241d5-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="241d5-113">Пример 2: получение списка учетных записей для Data Lake Store в учетной записи Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="241d5-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="241d5-114">Эта команда получает все учетные записи для Data Lake Store из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="241d5-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="241d5-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="241d5-115">PARAMETERS</span></span>

### <span data-ttu-id="241d5-116">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="241d5-116">-Account</span></span>
<span data-ttu-id="241d5-117">Указывает учетную запись Data Lake Analytics, которую этот командлет получает для источников данных.</span><span class="sxs-lookup"><span data-stu-id="241d5-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="241d5-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="241d5-118">-Blob</span></span>
<span data-ttu-id="241d5-119">Указывает имя источника данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="241d5-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241d5-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="241d5-120">-DataLakeStore</span></span>
<span data-ttu-id="241d5-121">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="241d5-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Data Lake Store account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241d5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="241d5-122">-ResourceGroupName</span></span>
<span data-ttu-id="241d5-123">Указывает имя группы ресурсов, которая содержит источник данных.</span><span class="sxs-lookup"><span data-stu-id="241d5-123">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="241d5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="241d5-124">-DefaultProfile</span></span>
<span data-ttu-id="241d5-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="241d5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="241d5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241d5-126">CommonParameters</span></span>
<span data-ttu-id="241d5-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="241d5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241d5-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="241d5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241d5-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="241d5-129">INPUTS</span></span>

## <span data-ttu-id="241d5-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="241d5-130">OUTPUTS</span></span>

### <span data-ttu-id="241d5-131">PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="241d5-131">PSStorageAccountInfo</span></span>
<span data-ttu-id="241d5-132">Указанные данные учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="241d5-132">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="241d5-133">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="241d5-133">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="241d5-134">Сведения об учетной записи, указанные в Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="241d5-134">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="241d5-135">Список<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="241d5-135">List<AdlDataSource></span></span>
<span data-ttu-id="241d5-136">Список учетных записей хранения Azure и учетные записи Data Lake Store для указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="241d5-136">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="241d5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="241d5-137">NOTES</span></span>

## <span data-ttu-id="241d5-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="241d5-138">RELATED LINKS</span></span>

[<span data-ttu-id="241d5-139">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="241d5-139">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="241d5-140">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="241d5-140">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="241d5-141">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="241d5-141">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


