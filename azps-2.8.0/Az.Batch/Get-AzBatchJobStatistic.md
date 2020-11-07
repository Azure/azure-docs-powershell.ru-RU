---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: b2c62cf91410e2604875df6f82237445e153f6aa
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913079"
---
# <span data-ttu-id="aeaf3-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="aeaf3-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="aeaf3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aeaf3-102">SYNOPSIS</span></span>
<span data-ttu-id="aeaf3-103">Возвращает сводную статистику по заданиям для учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="aeaf3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aeaf3-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aeaf3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aeaf3-105">DESCRIPTION</span></span>
<span data-ttu-id="aeaf3-106">Командлет **Get-AzBatchJobStatistic** получает сводную статистику времени выполнения для всех заданий в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="aeaf3-107">Статистические данные объединяются во всех заданиях, которые когда-либо существовали в учетной записи, от создания учетной записи до последнего обновления статистики.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="aeaf3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aeaf3-108">EXAMPLES</span></span>

### <span data-ttu-id="aeaf3-109">Пример 1: Получение сводных статистических данных для всех заданий</span><span class="sxs-lookup"><span data-stu-id="aeaf3-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzBatchJobStatistic -BatchContext $Context
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

<span data-ttu-id="aeaf3-110">Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="aeaf3-111">Команда сохраняет ссылку на этот объект в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="aeaf3-112">Вторая команда возвращает сводную статистику для всех заданий.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="aeaf3-113">В команде используется значение $Context из первой команды.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="aeaf3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aeaf3-114">PARAMETERS</span></span>

### <span data-ttu-id="aeaf3-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="aeaf3-115">-BatchContext</span></span>
<span data-ttu-id="aeaf3-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="aeaf3-117">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="aeaf3-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="aeaf3-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="aeaf3-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="aeaf3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeaf3-121">-DefaultProfile</span></span>
<span data-ttu-id="aeaf3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aeaf3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeaf3-123">CommonParameters</span></span>
<span data-ttu-id="aeaf3-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aeaf3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeaf3-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeaf3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeaf3-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aeaf3-126">INPUTS</span></span>

### <span data-ttu-id="aeaf3-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aeaf3-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="aeaf3-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aeaf3-128">OUTPUTS</span></span>

### <span data-ttu-id="aeaf3-129">Microsoft.Azure.Commands.BatCH. Models. PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="aeaf3-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="aeaf3-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="aeaf3-130">NOTES</span></span>

## <span data-ttu-id="aeaf3-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aeaf3-131">RELATED LINKS</span></span>

[<span data-ttu-id="aeaf3-132">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="aeaf3-132">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="aeaf3-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="aeaf3-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="aeaf3-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="aeaf3-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)


