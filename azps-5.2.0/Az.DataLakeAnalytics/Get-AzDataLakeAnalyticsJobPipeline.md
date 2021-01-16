---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 1d13d1b6e55831c972457c5a6a5aadc427ecb3a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406607"
---
# <span data-ttu-id="a7d4e-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="a7d4e-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="a7d4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d4e-103">Позволяет получить конвейер работы или конвейеры анализа для озера данных.</span><span class="sxs-lookup"><span data-stu-id="a7d4e-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="a7d4e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7d4e-104">SYNTAX</span></span>

### <span data-ttu-id="a7d4e-105">GetAllInAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7d4e-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7d4e-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="a7d4e-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7d4e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7d4e-107">DESCRIPTION</span></span>
<span data-ttu-id="a7d4e-108">**Get-AzDataLakeAnalyticsJobPipeline** получает определенный конвейер azure Data Lake Analytics или список конвейеров.</span><span class="sxs-lookup"><span data-stu-id="a7d4e-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="a7d4e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7d4e-109">EXAMPLES</span></span>

### <span data-ttu-id="a7d4e-110">Пример 1. Получить указанный канал</span><span class="sxs-lookup"><span data-stu-id="a7d4e-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="a7d4e-111">Эта команда получает указанный канал с ид '83cb7ad2-3523-4b82-b909-d478b0d8aea3' в учетной записи contosoadla.</span><span class="sxs-lookup"><span data-stu-id="a7d4e-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="a7d4e-112">Пример 2. Получить список всех каналов в учетной записи</span><span class="sxs-lookup"><span data-stu-id="a7d4e-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="a7d4e-113">Эта команда получает список всех каналов в учетной записи contosoadla.</span><span class="sxs-lookup"><span data-stu-id="a7d4e-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="a7d4e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7d4e-114">PARAMETERS</span></span>

### <span data-ttu-id="a7d4e-115">-Account</span><span class="sxs-lookup"><span data-stu-id="a7d4e-115">-Account</span></span>
<span data-ttu-id="a7d4e-116">Имя учетной записи Data Lake Analytics, под которой вы хотите получить канал задания.</span><span class="sxs-lookup"><span data-stu-id="a7d4e-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="a7d4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d4e-117">-DefaultProfile</span></span>
<span data-ttu-id="a7d4e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a7d4e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7d4e-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="a7d4e-119">-PipelineId</span></span>
<span data-ttu-id="a7d4e-120">ID of the specific job pipeline to return information for.</span><span class="sxs-lookup"><span data-stu-id="a7d4e-120">ID of the specific job pipeline to return information for.</span></span>

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

### <span data-ttu-id="a7d4e-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="a7d4e-121">-SubmittedAfter</span></span>
<span data-ttu-id="a7d4e-122">Необязательный фильтр, который возвращает конвейеры задания, отправленные только после заданного времени.</span><span class="sxs-lookup"><span data-stu-id="a7d4e-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="a7d4e-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="a7d4e-123">-SubmittedBefore</span></span>
<span data-ttu-id="a7d4e-124">Необязательный фильтр, который возвращает конвейеры задания, только отправленные до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="a7d4e-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="a7d4e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d4e-125">CommonParameters</span></span>
<span data-ttu-id="a7d4e-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d4e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d4e-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7d4e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d4e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7d4e-128">INPUTS</span></span>

### <span data-ttu-id="a7d4e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a7d4e-129">System.String</span></span>

### <span data-ttu-id="a7d4e-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a7d4e-130">System.Guid</span></span>

### <span data-ttu-id="a7d4e-131">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a7d4e-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a7d4e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7d4e-132">OUTPUTS</span></span>

### <span data-ttu-id="a7d4e-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="a7d4e-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="a7d4e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7d4e-134">NOTES</span></span>

## <span data-ttu-id="a7d4e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7d4e-135">RELATED LINKS</span></span>