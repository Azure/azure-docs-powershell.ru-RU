---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: 34d2921526f54e20697a11cf17708fef50e49fc2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561860"
---
# <span data-ttu-id="6ea50-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="6ea50-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="6ea50-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ea50-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea50-103">Возвращает повторение или повторения задания Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6ea50-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ea50-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ea50-104">SYNTAX</span></span>

### <span data-ttu-id="6ea50-105">GetAllInAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ea50-105">GetAllInAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ea50-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="6ea50-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ea50-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ea50-107">DESCRIPTION</span></span>
<span data-ttu-id="6ea50-108">Элемент **Get-AzureRmDataLakeAnalyticsJobRecurrence** возвращает указанное повторение задания Azure Data Lake Analytics или список повторений.</span><span class="sxs-lookup"><span data-stu-id="6ea50-108">The **Get-AzureRmDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="6ea50-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ea50-109">EXAMPLES</span></span>

### <span data-ttu-id="6ea50-110">Пример 1: получение указанного повторения</span><span class="sxs-lookup"><span data-stu-id="6ea50-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="6ea50-111">Эта команда получает повторение указанной задачи с идентификатором "83cb7ad2-3523-4b82-b909-d478b0d8aea3" в учетной записи "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="6ea50-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="6ea50-112">Пример 2: получение списка всех повторений в учетной записи</span><span class="sxs-lookup"><span data-stu-id="6ea50-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="6ea50-113">Эта команда возвращает список всех повторений в учетной записи "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="6ea50-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="6ea50-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ea50-114">PARAMETERS</span></span>

### <span data-ttu-id="6ea50-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6ea50-115">-Account</span></span>
<span data-ttu-id="6ea50-116">Имя учетной записи Data Lake Analytics, под которой требуется получить повторение задачи.</span><span class="sxs-lookup"><span data-stu-id="6ea50-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea50-117">-DefaultProfile</span></span>
<span data-ttu-id="6ea50-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6ea50-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ea50-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="6ea50-119">-RecurrenceId</span></span>
<span data-ttu-id="6ea50-120">Идентификатор определенного повторения задания, сведения о котором нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="6ea50-120">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea50-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="6ea50-121">-SubmittedAfter</span></span>
<span data-ttu-id="6ea50-122">Необязательный фильтр, возвращающий повторения заданий, отправленные только по истечении заданного времени.</span><span class="sxs-lookup"><span data-stu-id="6ea50-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea50-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="6ea50-123">-SubmittedBefore</span></span>
<span data-ttu-id="6ea50-124">Необязательный фильтр, возвращающий повторение заданий (-ов), отправленных только до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="6ea50-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea50-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea50-125">CommonParameters</span></span>
<span data-ttu-id="6ea50-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ea50-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea50-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ea50-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea50-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ea50-128">INPUTS</span></span>

### <span data-ttu-id="6ea50-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6ea50-129">System.String</span></span>
<span data-ttu-id="6ea50-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6ea50-130">System.Guid</span></span>

## <span data-ttu-id="6ea50-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ea50-131">OUTPUTS</span></span>

### <span data-ttu-id="6ea50-132">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="6ea50-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="6ea50-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ea50-133">NOTES</span></span>

## <span data-ttu-id="6ea50-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ea50-134">RELATED LINKS</span></span>

