---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: d571eb887069aa5c28029dfa98ab022c1d82fc88
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508382"
---
# <span data-ttu-id="4fb14-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="4fb14-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="4fb14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fb14-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb14-103">Возвращает повторение или повторение задания анализа для data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4fb14-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="4fb14-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4fb14-104">SYNTAX</span></span>

### <span data-ttu-id="4fb14-105">GetAllInAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4fb14-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fb14-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="4fb14-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fb14-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fb14-107">DESCRIPTION</span></span>
<span data-ttu-id="4fb14-108">**Get-AzDataLakeAnalyticsJobRecurrence** получает указанное повторение задания Azure Data Lake Analytics или список повторения.</span><span class="sxs-lookup"><span data-stu-id="4fb14-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="4fb14-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4fb14-109">EXAMPLES</span></span>

### <span data-ttu-id="4fb14-110">Пример 1. Получить определенное повторение</span><span class="sxs-lookup"><span data-stu-id="4fb14-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="4fb14-111">Эта команда возвращает указанное повторение задания с ид '83cb7ad2-3523-4b82-b909-d478b0d8aea3' в учетной записи contosoadla.</span><span class="sxs-lookup"><span data-stu-id="4fb14-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="4fb14-112">Пример 2. Получить список всех повторений в учетной записи</span><span class="sxs-lookup"><span data-stu-id="4fb14-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="4fb14-113">Эта команда возвращает список всех повторений в учетной записи contosoadla.</span><span class="sxs-lookup"><span data-stu-id="4fb14-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="4fb14-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fb14-114">PARAMETERS</span></span>

### <span data-ttu-id="4fb14-115">-Account</span><span class="sxs-lookup"><span data-stu-id="4fb14-115">-Account</span></span>
<span data-ttu-id="4fb14-116">Имя учетной записи Data Lake Analytics, под которой вы хотите восстановить повторение задания.</span><span class="sxs-lookup"><span data-stu-id="4fb14-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="4fb14-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb14-117">-DefaultProfile</span></span>
<span data-ttu-id="4fb14-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4fb14-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fb14-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="4fb14-119">-RecurrenceId</span></span>
<span data-ttu-id="4fb14-120">ID of the specific job recurrence to return information for.</span><span class="sxs-lookup"><span data-stu-id="4fb14-120">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb14-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="4fb14-121">-SubmittedAfter</span></span>
<span data-ttu-id="4fb14-122">Необязательный фильтр, который возвращает повторяющиеся задания только после заданного времени.</span><span class="sxs-lookup"><span data-stu-id="4fb14-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="4fb14-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="4fb14-123">-SubmittedBefore</span></span>
<span data-ttu-id="4fb14-124">Необязательный фильтр, который возвращает повторяющиеся задания, только отправленные до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="4fb14-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="4fb14-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb14-125">CommonParameters</span></span>
<span data-ttu-id="4fb14-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fb14-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb14-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb14-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb14-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fb14-128">INPUTS</span></span>

### <span data-ttu-id="4fb14-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4fb14-129">System.String</span></span>

### <span data-ttu-id="4fb14-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4fb14-130">System.Guid</span></span>

### <span data-ttu-id="4fb14-131">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4fb14-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4fb14-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4fb14-132">OUTPUTS</span></span>

### <span data-ttu-id="4fb14-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="4fb14-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="4fb14-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4fb14-134">NOTES</span></span>

## <span data-ttu-id="4fb14-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fb14-135">RELATED LINKS</span></span>
