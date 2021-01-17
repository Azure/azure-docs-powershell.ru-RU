---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 0dd0dfb25959ed3a5753ae6bd19b0500d4742634
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401367"
---
# <span data-ttu-id="e8bc2-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="e8bc2-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="e8bc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="e8bc2-103">Изменяет сведения об источнике данных учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e8bc2-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="e8bc2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e8bc2-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8bc2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8bc2-105">DESCRIPTION</span></span>
<span data-ttu-id="e8bc2-106">**Cmdlet Set-AzDataLakeAnalyticsDataSource** изменяет сведения об источнике данных учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e8bc2-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e8bc2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e8bc2-107">EXAMPLES</span></span>

### <span data-ttu-id="e8bc2-108">Пример 1. Изменение ключа доступа к источнику данных</span><span class="sxs-lookup"><span data-stu-id="e8bc2-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="e8bc2-109">Эта команда изменяет ключ доступа, хранимый для источника данных хранилища BLOB-приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="e8bc2-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="e8bc2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8bc2-110">PARAMETERS</span></span>

### <span data-ttu-id="e8bc2-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="e8bc2-111">-AccessKey</span></span>
<span data-ttu-id="e8bc2-112">Указывает новый ключ доступа к источнику данных хранилища BLOB-элементов Azure.</span><span class="sxs-lookup"><span data-stu-id="e8bc2-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bc2-113">-Account</span><span class="sxs-lookup"><span data-stu-id="e8bc2-113">-Account</span></span>
<span data-ttu-id="e8bc2-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e8bc2-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e8bc2-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="e8bc2-115">-Blob</span></span>
<span data-ttu-id="e8bc2-116">Имя источника данных хранилища BLOB-источников Azure.</span><span class="sxs-lookup"><span data-stu-id="e8bc2-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bc2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8bc2-117">-DefaultProfile</span></span>
<span data-ttu-id="e8bc2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e8bc2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8bc2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8bc2-119">-ResourceGroupName</span></span>
<span data-ttu-id="e8bc2-120">Имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e8bc2-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="e8bc2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8bc2-121">CommonParameters</span></span>
<span data-ttu-id="e8bc2-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8bc2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8bc2-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8bc2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8bc2-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8bc2-124">INPUTS</span></span>

### <span data-ttu-id="e8bc2-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e8bc2-125">System.String</span></span>

## <span data-ttu-id="e8bc2-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e8bc2-126">OUTPUTS</span></span>

### <span data-ttu-id="e8bc2-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="e8bc2-127">System.Void</span></span>

## <span data-ttu-id="e8bc2-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e8bc2-128">NOTES</span></span>

## <span data-ttu-id="e8bc2-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8bc2-129">RELATED LINKS</span></span>

[<span data-ttu-id="e8bc2-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="e8bc2-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="e8bc2-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="e8bc2-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


