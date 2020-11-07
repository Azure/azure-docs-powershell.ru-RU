---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: d0430b283f122b5da41392a04fc9827bc03e3082
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733868"
---
# <span data-ttu-id="7d9e4-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="7d9e4-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="7d9e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d9e4-102">SYNOPSIS</span></span>
<span data-ttu-id="7d9e4-103">Возвращает повторение или повторения задания Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7d9e4-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d9e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d9e4-104">SYNTAX</span></span>

### <span data-ttu-id="7d9e4-105">GetAllInAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d9e4-105">GetAllInAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d9e4-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="7d9e4-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d9e4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d9e4-107">DESCRIPTION</span></span>
<span data-ttu-id="7d9e4-108">Элемент **Get-AzureRmDataLakeAnalyticsJobRecurrence** возвращает указанное повторение задания Azure Data Lake Analytics или список повторений.</span><span class="sxs-lookup"><span data-stu-id="7d9e4-108">The **Get-AzureRmDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="7d9e4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d9e4-109">EXAMPLES</span></span>

### <span data-ttu-id="7d9e4-110">Пример 1: получение указанного повторения</span><span class="sxs-lookup"><span data-stu-id="7d9e4-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="7d9e4-111">Эта команда получает повторение указанной задачи с идентификатором "83cb7ad2-3523-4b82-b909-d478b0d8aea3" в учетной записи "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="7d9e4-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="7d9e4-112">Пример 2: получение списка всех повторений в учетной записи</span><span class="sxs-lookup"><span data-stu-id="7d9e4-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="7d9e4-113">Эта команда возвращает список всех повторений в учетной записи "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="7d9e4-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="7d9e4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d9e4-114">PARAMETERS</span></span>

### <span data-ttu-id="7d9e4-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="7d9e4-115">-Account</span></span>
<span data-ttu-id="7d9e4-116">Имя учетной записи Data Lake Analytics, под которой требуется получить повторение задачи.</span><span class="sxs-lookup"><span data-stu-id="7d9e4-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="7d9e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d9e4-117">-DefaultProfile</span></span>
<span data-ttu-id="7d9e4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7d9e4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d9e4-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="7d9e4-119">-RecurrenceId</span></span>
<span data-ttu-id="7d9e4-120">Идентификатор определенного повторения задания, сведения о котором нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="7d9e4-120">ID of the specific job recurrence to return information for.</span></span>

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

### <span data-ttu-id="7d9e4-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="7d9e4-121">-SubmittedAfter</span></span>
<span data-ttu-id="7d9e4-122">Необязательный фильтр, возвращающий повторения заданий, отправленные только по истечении заданного времени.</span><span class="sxs-lookup"><span data-stu-id="7d9e4-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="7d9e4-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="7d9e4-123">-SubmittedBefore</span></span>
<span data-ttu-id="7d9e4-124">Необязательный фильтр, возвращающий повторение заданий (-ов), отправленных только до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="7d9e4-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="7d9e4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d9e4-125">CommonParameters</span></span>
<span data-ttu-id="7d9e4-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d9e4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d9e4-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d9e4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d9e4-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d9e4-128">INPUTS</span></span>

### <span data-ttu-id="7d9e4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7d9e4-129">System.String</span></span>

### <span data-ttu-id="7d9e4-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7d9e4-130">System.Guid</span></span>

### <span data-ttu-id="7d9e4-131">System. Nullable "1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7d9e4-131">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7d9e4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d9e4-132">OUTPUTS</span></span>

### <span data-ttu-id="7d9e4-133">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="7d9e4-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="7d9e4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d9e4-134">NOTES</span></span>

## <span data-ttu-id="7d9e4-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d9e4-135">RELATED LINKS</span></span>
