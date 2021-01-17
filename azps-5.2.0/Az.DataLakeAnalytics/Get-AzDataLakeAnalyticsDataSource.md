---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: e14e4c1b58b24cb8065681ae806789cd1252a0db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328373"
---
# <span data-ttu-id="1f148-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1f148-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="1f148-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f148-102">SYNOPSIS</span></span>
<span data-ttu-id="1f148-103">Получает источник данных Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1f148-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="1f148-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1f148-104">SYNTAX</span></span>

### <span data-ttu-id="1f148-105">GetAllDataSources (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f148-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f148-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1f148-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f148-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1f148-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f148-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f148-108">DESCRIPTION</span></span>
<span data-ttu-id="1f148-109">Для получения источника данных Azure Data Lake Analytics возвращается cmdlet **Get-AzDataLakeAnalyticsDataSource.**</span><span class="sxs-lookup"><span data-stu-id="1f148-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="1f148-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1f148-110">EXAMPLES</span></span>

### <span data-ttu-id="1f148-111">Пример 1. Источник данных из учетной записи</span><span class="sxs-lookup"><span data-stu-id="1f148-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="1f148-112">Эта команда получает источник данных ContosoAdls из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1f148-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="1f148-113">Пример 2. Просмотр списка учетных записей Data Lake Store в учетной записи Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="1f148-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="1f148-114">Эта команда получает все учетные записи Data Lake Store из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1f148-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="1f148-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f148-115">PARAMETERS</span></span>

### <span data-ttu-id="1f148-116">-Account</span><span class="sxs-lookup"><span data-stu-id="1f148-116">-Account</span></span>
<span data-ttu-id="1f148-117">Указывает учетную запись Data Lake Analytics, которая получает источники данных этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f148-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="1f148-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="1f148-118">-Blob</span></span>
<span data-ttu-id="1f148-119">Имя источника данных хранилища BLOB-источников Azure.</span><span class="sxs-lookup"><span data-stu-id="1f148-119">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="1f148-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1f148-120">-DataLakeStore</span></span>
<span data-ttu-id="1f148-121">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1f148-121">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1f148-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f148-122">-DefaultProfile</span></span>
<span data-ttu-id="1f148-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1f148-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f148-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f148-124">-ResourceGroupName</span></span>
<span data-ttu-id="1f148-125">Имя группы ресурсов, которая содержит источник данных.</span><span class="sxs-lookup"><span data-stu-id="1f148-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="1f148-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f148-126">CommonParameters</span></span>
<span data-ttu-id="1f148-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f148-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f148-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f148-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f148-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f148-129">INPUTS</span></span>

### <span data-ttu-id="1f148-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1f148-130">System.String</span></span>

## <span data-ttu-id="1f148-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f148-131">OUTPUTS</span></span>

### <span data-ttu-id="1f148-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="1f148-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="1f148-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="1f148-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="1f148-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="1f148-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="1f148-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1f148-135">NOTES</span></span>

## <span data-ttu-id="1f148-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f148-136">RELATED LINKS</span></span>

[<span data-ttu-id="1f148-137">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1f148-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="1f148-138">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1f148-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="1f148-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1f148-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


