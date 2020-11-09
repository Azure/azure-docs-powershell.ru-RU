---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 1d13d1b6e55831c972457c5a6a5aadc427ecb3a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313586"
---
# <span data-ttu-id="86c35-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="86c35-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="86c35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86c35-102">SYNOPSIS</span></span>
<span data-ttu-id="86c35-103">Возвращает конвейер заданий или конвейеров для задания Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="86c35-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="86c35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86c35-104">SYNTAX</span></span>

### <span data-ttu-id="86c35-105">GetAllInAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86c35-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86c35-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="86c35-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86c35-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86c35-107">DESCRIPTION</span></span>
<span data-ttu-id="86c35-108">Элемент **Get-AzDataLakeAnalyticsJobPipeline** Возвращает указанный конвейер задания Azure Data Lake Analytics или список конвейеров.</span><span class="sxs-lookup"><span data-stu-id="86c35-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="86c35-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86c35-109">EXAMPLES</span></span>

### <span data-ttu-id="86c35-110">Пример 1: получение указанного конвейера</span><span class="sxs-lookup"><span data-stu-id="86c35-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="86c35-111">Эта команда получает указанный конвейер с идентификатором "83cb7ad2-3523-4b82-b909-d478b0d8aea3" в учетной записи "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="86c35-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="86c35-112">Пример 2: получение списка всех конвейеров в учетной записи</span><span class="sxs-lookup"><span data-stu-id="86c35-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="86c35-113">Эта команда возвращает список всех конвейеров в учетной записи "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="86c35-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="86c35-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86c35-114">PARAMETERS</span></span>

### <span data-ttu-id="86c35-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="86c35-115">-Account</span></span>
<span data-ttu-id="86c35-116">Имя учетной записи Data Lake Analytics, под которой требуется получить конвейер заданий.</span><span class="sxs-lookup"><span data-stu-id="86c35-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="86c35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c35-117">-DefaultProfile</span></span>
<span data-ttu-id="86c35-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="86c35-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86c35-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="86c35-119">-PipelineId</span></span>
<span data-ttu-id="86c35-120">Идентификатор определенного конвейера заданий, для которого нужно вернуть сведения.</span><span class="sxs-lookup"><span data-stu-id="86c35-120">ID of the specific job pipeline to return information for.</span></span>

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

### <span data-ttu-id="86c35-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="86c35-121">-SubmittedAfter</span></span>
<span data-ttu-id="86c35-122">Необязательный фильтр, который возвращает данные о конвейерах заданий, отправленных только по истечении заданного времени.</span><span class="sxs-lookup"><span data-stu-id="86c35-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="86c35-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="86c35-123">-SubmittedBefore</span></span>
<span data-ttu-id="86c35-124">Необязательный фильтр, который возвращает данные о конвейерах заданий, отправленных только до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="86c35-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="86c35-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c35-125">CommonParameters</span></span>
<span data-ttu-id="86c35-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86c35-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c35-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c35-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c35-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86c35-128">INPUTS</span></span>

### <span data-ttu-id="86c35-129">System. String</span><span class="sxs-lookup"><span data-stu-id="86c35-129">System.String</span></span>

### <span data-ttu-id="86c35-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="86c35-130">System.Guid</span></span>

### <span data-ttu-id="86c35-131">System. Nullable "1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="86c35-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="86c35-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86c35-132">OUTPUTS</span></span>

### <span data-ttu-id="86c35-133">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="86c35-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="86c35-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="86c35-134">NOTES</span></span>

## <span data-ttu-id="86c35-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86c35-135">RELATED LINKS</span></span>
