---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: c17a58cee2b5f13345997b97ce00792a8b9c9a0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567772"
---
# <span data-ttu-id="b6164-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="b6164-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="b6164-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6164-102">SYNOPSIS</span></span>
<span data-ttu-id="b6164-103">Возвращает конвейер заданий или конвейеров для задания Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6164-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6164-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6164-104">SYNTAX</span></span>

### <span data-ttu-id="b6164-105">GetAllInAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6164-105">GetAllInAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6164-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="b6164-106">GetBySpecificJobPipeline</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6164-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6164-107">DESCRIPTION</span></span>
<span data-ttu-id="b6164-108">Элемент **Get-AzureRmDataLakeAnalyticsJobPipeline** Возвращает указанный конвейер задания Azure Data Lake Analytics или список конвейеров.</span><span class="sxs-lookup"><span data-stu-id="b6164-108">The **Get-AzureRmDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="b6164-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6164-109">EXAMPLES</span></span>

### <span data-ttu-id="b6164-110">Пример 1: получение указанного конвейера</span><span class="sxs-lookup"><span data-stu-id="b6164-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="b6164-111">Эта команда получает указанный конвейер с идентификатором "83cb7ad2-3523-4b82-b909-d478b0d8aea3" в учетной записи "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="b6164-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="b6164-112">Пример 2: получение списка всех конвейеров в учетной записи</span><span class="sxs-lookup"><span data-stu-id="b6164-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="b6164-113">Эта команда возвращает список всех конвейеров в учетной записи "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="b6164-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="b6164-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6164-114">PARAMETERS</span></span>

### <span data-ttu-id="b6164-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b6164-115">-Account</span></span>
<span data-ttu-id="b6164-116">Имя учетной записи Data Lake Analytics, под которой требуется получить конвейер заданий.</span><span class="sxs-lookup"><span data-stu-id="b6164-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="b6164-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6164-117">-DefaultProfile</span></span>
<span data-ttu-id="b6164-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b6164-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6164-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="b6164-119">-PipelineId</span></span>
<span data-ttu-id="b6164-120">Идентификатор определенного конвейера заданий, для которого нужно вернуть сведения.</span><span class="sxs-lookup"><span data-stu-id="b6164-120">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6164-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="b6164-121">-SubmittedAfter</span></span>
<span data-ttu-id="b6164-122">Необязательный фильтр, который возвращает данные о конвейерах заданий, отправленных только по истечении заданного времени.</span><span class="sxs-lookup"><span data-stu-id="b6164-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6164-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="b6164-123">-SubmittedBefore</span></span>
<span data-ttu-id="b6164-124">Необязательный фильтр, который возвращает данные о конвейерах заданий, отправленных только до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="b6164-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6164-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6164-125">CommonParameters</span></span>
<span data-ttu-id="b6164-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6164-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6164-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6164-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6164-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6164-128">INPUTS</span></span>

### <span data-ttu-id="b6164-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b6164-129">System.String</span></span>

### <span data-ttu-id="b6164-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b6164-130">System.Guid</span></span>

### <span data-ttu-id="b6164-131">System. Nullable "1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b6164-131">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b6164-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6164-132">OUTPUTS</span></span>

### <span data-ttu-id="b6164-133">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="b6164-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="b6164-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6164-134">NOTES</span></span>

## <span data-ttu-id="b6164-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6164-135">RELATED LINKS</span></span>
