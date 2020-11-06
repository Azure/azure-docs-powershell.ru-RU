---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 03b7e3999fbc482223365b59867c02c75e9d5ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565270"
---
# <span data-ttu-id="44524-101">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="44524-101">Get-AzureBatchJobStatistics</span></span>

## <span data-ttu-id="44524-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44524-102">SYNOPSIS</span></span>
<span data-ttu-id="44524-103">Возвращает сводную статистику по заданиям для учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="44524-103">Gets job summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44524-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44524-104">SYNTAX</span></span>

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44524-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44524-105">DESCRIPTION</span></span>
<span data-ttu-id="44524-106">Командлет **Get-AzureBatchJobStatistics** получает сводную статистику времени выполнения для всех заданий в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="44524-106">The **Get-AzureBatchJobStatistics** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="44524-107">Статистические данные объединяются во всех заданиях, которые когда-либо существовали в учетной записи, от создания учетной записи до последнего обновления статистики.</span><span class="sxs-lookup"><span data-stu-id="44524-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="44524-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44524-108">EXAMPLES</span></span>

### <span data-ttu-id="44524-109">Пример 1: Получение сводных статистических данных для всех заданий</span><span class="sxs-lookup"><span data-stu-id="44524-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzureBatchJobStatistics -BatchContext $Context
FailedTaskCount    : 330
KernelCpuTime      : 00:24:31.8440000
LastUpdateTime     : 5/16/2016 6:00:00 PM
ReadIOGiB          : 38.1271341182292
ReadIOps           : 26546054
StartTime          : 11/3/2015 9:47:14 PM
SucceededTaskCount : 766
TaskRetryCount     : 0
Url                : https://accountname.westus.batch.azure.com/lifetimejobstats
UserCpuTime        : 20:55:50.3200000
WaitTime           : 03:54:49.8530000
WallClockTime      : 20:55:50.3200000
WriteIOGiB         : 0.159623090177774
WriteIOps          : 146946
```

<span data-ttu-id="44524-110">Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="44524-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="44524-111">Команда сохраняет ссылку на этот объект в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="44524-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="44524-112">Вторая команда возвращает сводную статистику для всех заданий.</span><span class="sxs-lookup"><span data-stu-id="44524-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="44524-113">В команде используется значение $Context из первой команды.</span><span class="sxs-lookup"><span data-stu-id="44524-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="44524-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44524-114">PARAMETERS</span></span>

### <span data-ttu-id="44524-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="44524-115">-BatchContext</span></span>
<span data-ttu-id="44524-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="44524-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="44524-117">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="44524-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44524-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44524-118">-DefaultProfile</span></span>
<span data-ttu-id="44524-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44524-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44524-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44524-120">CommonParameters</span></span>
<span data-ttu-id="44524-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44524-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44524-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44524-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44524-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44524-123">INPUTS</span></span>

### <span data-ttu-id="44524-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="44524-124">BatchAccountContext</span></span>
<span data-ttu-id="44524-125">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="44524-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="44524-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44524-126">OUTPUTS</span></span>

### <span data-ttu-id="44524-127">PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="44524-127">PSJobStatistics</span></span>

## <span data-ttu-id="44524-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="44524-128">NOTES</span></span>

## <span data-ttu-id="44524-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44524-129">RELATED LINKS</span></span>

[<span data-ttu-id="44524-130">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="44524-130">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="44524-131">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="44524-131">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="44524-132">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="44524-132">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)


