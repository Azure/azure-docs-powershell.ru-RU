---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 80ee6f881731f61b045e448e8a231ae9c971552d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566236"
---
# <span data-ttu-id="7e1dc-101">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="7e1dc-101">Get-AzureBatchJobStatistics</span></span>

## <span data-ttu-id="7e1dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="7e1dc-103">Возвращает сводную статистику по заданиям для учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-103">Gets job summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e1dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e1dc-104">SYNTAX</span></span>

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e1dc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e1dc-105">DESCRIPTION</span></span>
<span data-ttu-id="7e1dc-106">Командлет **Get-AzureBatchJobStatistics** получает сводную статистику времени выполнения для всех заданий в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-106">The **Get-AzureBatchJobStatistics** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="7e1dc-107">Статистические данные объединяются во всех заданиях, которые когда-либо существовали в учетной записи, от создания учетной записи до последнего обновления статистики.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="7e1dc-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e1dc-108">EXAMPLES</span></span>

### <span data-ttu-id="7e1dc-109">Пример 1: Получение сводных статистических данных для всех заданий</span><span class="sxs-lookup"><span data-stu-id="7e1dc-109">Example 1: Get summary statistics for all jobs</span></span>
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

<span data-ttu-id="7e1dc-110">Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="7e1dc-111">Команда сохраняет ссылку на этот объект в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="7e1dc-112">Вторая команда возвращает сводную статистику для всех заданий.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="7e1dc-113">В команде используется значение $Context из первой команды.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="7e1dc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e1dc-114">PARAMETERS</span></span>

### <span data-ttu-id="7e1dc-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7e1dc-115">-BatchContext</span></span>
<span data-ttu-id="7e1dc-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7e1dc-117">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7e1dc-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7e1dc-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7e1dc-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e1dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e1dc-121">-DefaultProfile</span></span>
<span data-ttu-id="7e1dc-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e1dc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e1dc-123">CommonParameters</span></span>
<span data-ttu-id="7e1dc-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e1dc-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e1dc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e1dc-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e1dc-126">INPUTS</span></span>

### <span data-ttu-id="7e1dc-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7e1dc-127">BatchAccountContext</span></span>
<span data-ttu-id="7e1dc-128">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7e1dc-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="7e1dc-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e1dc-129">OUTPUTS</span></span>

### <span data-ttu-id="7e1dc-130">PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="7e1dc-130">PSJobStatistics</span></span>

## <span data-ttu-id="7e1dc-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e1dc-131">NOTES</span></span>

## <span data-ttu-id="7e1dc-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e1dc-132">RELATED LINKS</span></span>

[<span data-ttu-id="7e1dc-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7e1dc-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7e1dc-134">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="7e1dc-134">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="7e1dc-135">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="7e1dc-135">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)


