---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 0dd0dfb25959ed3a5753ae6bd19b0500d4742634
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313505"
---
# <span data-ttu-id="cc1d4-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="cc1d4-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="cc1d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc1d4-102">SYNOPSIS</span></span>
<span data-ttu-id="cc1d4-103">Изменение сведений об источнике данных учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cc1d4-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="cc1d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc1d4-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc1d4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc1d4-105">DESCRIPTION</span></span>
<span data-ttu-id="cc1d4-106">Командлет **Set-AzDataLakeAnalyticsDataSource** изменяет сведения об источнике данных учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cc1d4-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="cc1d4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc1d4-107">EXAMPLES</span></span>

### <span data-ttu-id="cc1d4-108">Пример 1: изменение клавиши доступа для источника данных</span><span class="sxs-lookup"><span data-stu-id="cc1d4-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="cc1d4-109">Эта команда изменяет ключ доступа, хранящийся в источнике данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="cc1d4-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="cc1d4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc1d4-110">PARAMETERS</span></span>

### <span data-ttu-id="cc1d4-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="cc1d4-111">-AccessKey</span></span>
<span data-ttu-id="cc1d4-112">Указывает новый ключ доступа источника данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="cc1d4-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="cc1d4-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="cc1d4-113">-Account</span></span>
<span data-ttu-id="cc1d4-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cc1d4-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="cc1d4-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="cc1d4-115">-Blob</span></span>
<span data-ttu-id="cc1d4-116">Указывает имя источника данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="cc1d4-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="cc1d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc1d4-117">-DefaultProfile</span></span>
<span data-ttu-id="cc1d4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cc1d4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc1d4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc1d4-119">-ResourceGroupName</span></span>
<span data-ttu-id="cc1d4-120">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cc1d4-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="cc1d4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc1d4-121">CommonParameters</span></span>
<span data-ttu-id="cc1d4-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc1d4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc1d4-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc1d4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc1d4-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc1d4-124">INPUTS</span></span>

### <span data-ttu-id="cc1d4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cc1d4-125">System.String</span></span>

## <span data-ttu-id="cc1d4-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc1d4-126">OUTPUTS</span></span>

### <span data-ttu-id="cc1d4-127">System. void</span><span class="sxs-lookup"><span data-stu-id="cc1d4-127">System.Void</span></span>

## <span data-ttu-id="cc1d4-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc1d4-128">NOTES</span></span>

## <span data-ttu-id="cc1d4-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc1d4-129">RELATED LINKS</span></span>

[<span data-ttu-id="cc1d4-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="cc1d4-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="cc1d4-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="cc1d4-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


