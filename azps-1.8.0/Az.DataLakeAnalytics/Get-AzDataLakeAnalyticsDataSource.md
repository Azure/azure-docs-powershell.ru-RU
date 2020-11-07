---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 29f9315063db7d6bb16f8656950da39e70ddced9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900869"
---
# <span data-ttu-id="a1ad4-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a1ad4-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="a1ad4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ad4-103">Возвращает источник данных Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a1ad4-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="a1ad4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1ad4-104">SYNTAX</span></span>

### <span data-ttu-id="a1ad4-105">GetAllDataSources (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1ad4-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1ad4-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a1ad4-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1ad4-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1ad4-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1ad4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1ad4-108">DESCRIPTION</span></span>
<span data-ttu-id="a1ad4-109">Командлет **Get-AzDataLakeAnalyticsDataSource** получает источник данных Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a1ad4-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="a1ad4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1ad4-110">EXAMPLES</span></span>

### <span data-ttu-id="a1ad4-111">Пример 1: получение источника данных из учетной записи</span><span class="sxs-lookup"><span data-stu-id="a1ad4-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="a1ad4-112">Эта команда получает источник данных Data Lake Store с именем ContosoAdls из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a1ad4-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="a1ad4-113">Пример 2: получение списка учетных записей для Data Lake Store в учетной записи Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="a1ad4-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="a1ad4-114">Эта команда получает все учетные записи для Data Lake Store из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a1ad4-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a1ad4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1ad4-115">PARAMETERS</span></span>

### <span data-ttu-id="a1ad4-116">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="a1ad4-116">-Account</span></span>
<span data-ttu-id="a1ad4-117">Указывает учетную запись Data Lake Analytics, которую этот командлет получает для источников данных.</span><span class="sxs-lookup"><span data-stu-id="a1ad4-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="a1ad4-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="a1ad4-118">-Blob</span></span>
<span data-ttu-id="a1ad4-119">Указывает имя источника данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="a1ad4-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1ad4-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a1ad4-120">-DataLakeStore</span></span>
<span data-ttu-id="a1ad4-121">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a1ad4-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDataLakeStoreAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1ad4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1ad4-122">-DefaultProfile</span></span>
<span data-ttu-id="a1ad4-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a1ad4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1ad4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1ad4-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1ad4-125">Указывает имя группы ресурсов, которая содержит источник данных.</span><span class="sxs-lookup"><span data-stu-id="a1ad4-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="a1ad4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ad4-126">CommonParameters</span></span>
<span data-ttu-id="a1ad4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1ad4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ad4-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1ad4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ad4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1ad4-129">INPUTS</span></span>

### <span data-ttu-id="a1ad4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a1ad4-130">System.String</span></span>

## <span data-ttu-id="a1ad4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1ad4-131">OUTPUTS</span></span>

### <span data-ttu-id="a1ad4-132">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="a1ad4-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="a1ad4-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="a1ad4-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="a1ad4-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="a1ad4-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="a1ad4-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1ad4-135">NOTES</span></span>

## <span data-ttu-id="a1ad4-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1ad4-136">RELATED LINKS</span></span>

[<span data-ttu-id="a1ad4-137">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a1ad4-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="a1ad4-138">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a1ad4-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="a1ad4-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a1ad4-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


