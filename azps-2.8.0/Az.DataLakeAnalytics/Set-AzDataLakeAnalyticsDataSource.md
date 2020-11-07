---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 8fece6d480ee2210ff66256e02baaf6a11f9c1f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721357"
---
# <span data-ttu-id="bd75d-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="bd75d-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="bd75d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd75d-102">SYNOPSIS</span></span>
<span data-ttu-id="bd75d-103">Изменение сведений об источнике данных учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bd75d-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="bd75d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd75d-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd75d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd75d-105">DESCRIPTION</span></span>
<span data-ttu-id="bd75d-106">Командлет **Set-AzDataLakeAnalyticsDataSource** изменяет сведения об источнике данных учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bd75d-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="bd75d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd75d-107">EXAMPLES</span></span>

### <span data-ttu-id="bd75d-108">Пример 1: изменение клавиши доступа для источника данных</span><span class="sxs-lookup"><span data-stu-id="bd75d-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="bd75d-109">Эта команда изменяет ключ доступа, хранящийся в источнике данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="bd75d-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="bd75d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd75d-110">PARAMETERS</span></span>

### <span data-ttu-id="bd75d-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="bd75d-111">-AccessKey</span></span>
<span data-ttu-id="bd75d-112">Указывает новый ключ доступа источника данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="bd75d-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="bd75d-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="bd75d-113">-Account</span></span>
<span data-ttu-id="bd75d-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bd75d-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="bd75d-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="bd75d-115">-Blob</span></span>
<span data-ttu-id="bd75d-116">Указывает имя источника данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="bd75d-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="bd75d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd75d-117">-DefaultProfile</span></span>
<span data-ttu-id="bd75d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bd75d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd75d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd75d-119">-ResourceGroupName</span></span>
<span data-ttu-id="bd75d-120">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bd75d-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="bd75d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd75d-121">CommonParameters</span></span>
<span data-ttu-id="bd75d-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd75d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd75d-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd75d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd75d-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd75d-124">INPUTS</span></span>

### <span data-ttu-id="bd75d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bd75d-125">System.String</span></span>

## <span data-ttu-id="bd75d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd75d-126">OUTPUTS</span></span>

### <span data-ttu-id="bd75d-127">System. void</span><span class="sxs-lookup"><span data-stu-id="bd75d-127">System.Void</span></span>

## <span data-ttu-id="bd75d-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd75d-128">NOTES</span></span>

## <span data-ttu-id="bd75d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd75d-129">RELATED LINKS</span></span>

[<span data-ttu-id="bd75d-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="bd75d-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="bd75d-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="bd75d-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


