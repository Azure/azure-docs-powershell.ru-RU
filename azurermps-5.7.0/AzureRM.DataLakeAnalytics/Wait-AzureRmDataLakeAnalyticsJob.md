---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/wait-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 43af4abf52c3441f25ec57ce659b6c4e47a79cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568597"
---
# <span data-ttu-id="aaaa0-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="aaaa0-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="aaaa0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aaaa0-102">SYNOPSIS</span></span>
<span data-ttu-id="aaaa0-103">Ожидание завершения задания.</span><span class="sxs-lookup"><span data-stu-id="aaaa0-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaaa0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aaaa0-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaaa0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaaa0-105">DESCRIPTION</span></span>
<span data-ttu-id="aaaa0-106">Командлет **Wait-AzureRmDataLakeAnalyticsJob** ожидает завершения задания Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="aaaa0-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="aaaa0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aaaa0-107">EXAMPLES</span></span>

### <span data-ttu-id="aaaa0-108">Пример 1: ожидание завершения задания</span><span class="sxs-lookup"><span data-stu-id="aaaa0-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="aaaa0-109">Следующая команда ожидает завершения задания с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="aaaa0-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="aaaa0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aaaa0-110">PARAMETERS</span></span>

### <span data-ttu-id="aaaa0-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="aaaa0-111">-Account</span></span>
<span data-ttu-id="aaaa0-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="aaaa0-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="aaaa0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaaa0-113">-DefaultProfile</span></span>
<span data-ttu-id="aaaa0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aaaa0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaaa0-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="aaaa0-115">-JobId</span></span>
<span data-ttu-id="aaaa0-116">Указывает идентификатор задания, которое требуется подождать.</span><span class="sxs-lookup"><span data-stu-id="aaaa0-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaaa0-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="aaaa0-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="aaaa0-118">Задает количество секунд ожидания перед выходом из ожидания.</span><span class="sxs-lookup"><span data-stu-id="aaaa0-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaaa0-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="aaaa0-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="aaaa0-120">Укажите количество секунд, которое проходит между проверками состояния задания.</span><span class="sxs-lookup"><span data-stu-id="aaaa0-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaaa0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaaa0-121">CommonParameters</span></span>
<span data-ttu-id="aaaa0-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aaaa0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaaa0-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaaa0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaaa0-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aaaa0-124">INPUTS</span></span>

### <span data-ttu-id="aaaa0-125">GUID</span><span class="sxs-lookup"><span data-stu-id="aaaa0-125">Guid</span></span>
<span data-ttu-id="aaaa0-126">Параметр "JobId" принимает значение типа "GUID" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="aaaa0-126">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="aaaa0-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaaa0-127">OUTPUTS</span></span>

### <span data-ttu-id="aaaa0-128">JobInformation</span><span class="sxs-lookup"><span data-stu-id="aaaa0-128">JobInformation</span></span>
<span data-ttu-id="aaaa0-129">Окончательные сведения о задании для завершенного задания.</span><span class="sxs-lookup"><span data-stu-id="aaaa0-129">The final job details for the completed job.</span></span>

## <span data-ttu-id="aaaa0-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="aaaa0-130">NOTES</span></span>

## <span data-ttu-id="aaaa0-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aaaa0-131">RELATED LINKS</span></span>

[<span data-ttu-id="aaaa0-132">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="aaaa0-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="aaaa0-133">Остановить-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="aaaa0-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="aaaa0-134">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="aaaa0-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


