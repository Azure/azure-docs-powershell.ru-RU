---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 047d0c7c9b141f10ee3f1be2ba1e739960f2e5bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313460"
---
# <span data-ttu-id="ed5cb-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ed5cb-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="ed5cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5cb-103">Ожидание завершения задания.</span><span class="sxs-lookup"><span data-stu-id="ed5cb-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="ed5cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed5cb-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed5cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed5cb-105">DESCRIPTION</span></span>
<span data-ttu-id="ed5cb-106">Командлет **Wait-AzDataLakeAnalyticsJob** ожидает завершения задания Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ed5cb-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="ed5cb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed5cb-107">EXAMPLES</span></span>

### <span data-ttu-id="ed5cb-108">Пример 1: ожидание завершения задания</span><span class="sxs-lookup"><span data-stu-id="ed5cb-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="ed5cb-109">Следующая команда ожидает завершения задания с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="ed5cb-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="ed5cb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed5cb-110">PARAMETERS</span></span>

### <span data-ttu-id="ed5cb-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="ed5cb-111">-Account</span></span>
<span data-ttu-id="ed5cb-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ed5cb-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="ed5cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5cb-113">-DefaultProfile</span></span>
<span data-ttu-id="ed5cb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ed5cb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed5cb-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="ed5cb-115">-JobId</span></span>
<span data-ttu-id="ed5cb-116">Указывает идентификатор задания, которое требуется подождать.</span><span class="sxs-lookup"><span data-stu-id="ed5cb-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5cb-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="ed5cb-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="ed5cb-118">Задает количество секунд ожидания перед выходом из ожидания.</span><span class="sxs-lookup"><span data-stu-id="ed5cb-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5cb-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ed5cb-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="ed5cb-120">Укажите количество секунд, которое проходит между проверками состояния задания.</span><span class="sxs-lookup"><span data-stu-id="ed5cb-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5cb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5cb-121">CommonParameters</span></span>
<span data-ttu-id="ed5cb-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed5cb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5cb-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed5cb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5cb-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed5cb-124">INPUTS</span></span>

### <span data-ttu-id="ed5cb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ed5cb-125">System.String</span></span>

### <span data-ttu-id="ed5cb-126">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ed5cb-126">System.Guid</span></span>

### <span data-ttu-id="ed5cb-127">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ed5cb-127">System.Int32</span></span>

## <span data-ttu-id="ed5cb-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed5cb-128">OUTPUTS</span></span>

### <span data-ttu-id="ed5cb-129">Microsoft. Azure. Management. данных Lake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="ed5cb-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="ed5cb-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed5cb-130">NOTES</span></span>

## <span data-ttu-id="ed5cb-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed5cb-131">RELATED LINKS</span></span>

[<span data-ttu-id="ed5cb-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ed5cb-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="ed5cb-133">Остановить-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ed5cb-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="ed5cb-134">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ed5cb-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

