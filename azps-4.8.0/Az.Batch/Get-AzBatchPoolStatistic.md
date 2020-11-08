---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
ms.openlocfilehash: 49aa971dcc9d46f5a063042cbcdf8ca449c41e94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242615"
---
# <span data-ttu-id="df9a4-101">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="df9a4-101">Get-AzBatchPoolStatistic</span></span>

## <span data-ttu-id="df9a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="df9a4-103">Возвращает сводную статистику пула для учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="df9a4-103">Gets pool summary statistics for a Batch account.</span></span>

## <span data-ttu-id="df9a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df9a4-104">SYNTAX</span></span>

```
Get-AzBatchPoolStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df9a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df9a4-105">DESCRIPTION</span></span>
<span data-ttu-id="df9a4-106">Командлет **Get-AzBatchPoolStatistic** получает статистику времени жизни для всех пулов в указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="df9a4-106">The **Get-AzBatchPoolStatistic** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="df9a4-107">Статистические данные объединяются во всех пулах, которые когда-либо существовали в учетной записи, от создания учетной записи до последнего обновления статистики.</span><span class="sxs-lookup"><span data-stu-id="df9a4-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="df9a4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df9a4-108">EXAMPLES</span></span>

### <span data-ttu-id="df9a4-109">Пример 1: получение статистики по ресурсам всех пулов в учетной записи</span><span class="sxs-lookup"><span data-stu-id="df9a4-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzBatchPoolStatistic -BatchContext $Context
PS C:\> $PoolStatistics.ResourceStatistics
AverageCpuPercentage : 0.351232518750755
AverageDiskGiB       : 55.2569014701165
AverageMemoryGiB     : 2.87273772318252
DiskReadGiB          : 45.1326256990433
DiskReadIOps         : 878278
DiskWriteGiB         : 1230.72120628133
DiskWriteIOps        : 176832212
LastUpdateTime       : 5/16/2016 4:30:00 PM
NetworkReadGiB       : 29.3502839952707
NetworkWriteGiB      : 25.5208827350289
PeakDiskGiB          : 21.9638671875
PeakMemoryGiB        : 1.11184692382813
StartTime            : 2/10/2016 7:07:24 PM
```

<span data-ttu-id="df9a4-110">Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="df9a4-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="df9a4-111">Команда сохраняет ссылку на этот объект в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="df9a4-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="df9a4-112">Вторая команда возвращает статистику всех пулов в указанной учетной записи, а затем сохраняет их в $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="df9a4-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="df9a4-113">В последней команде отображается свойство **ResourceStatistics** для $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="df9a4-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="df9a4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df9a4-114">PARAMETERS</span></span>

### <span data-ttu-id="df9a4-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="df9a4-115">-BatchContext</span></span>
<span data-ttu-id="df9a4-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="df9a4-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="df9a4-117">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="df9a4-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="df9a4-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="df9a4-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="df9a4-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="df9a4-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="df9a4-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="df9a4-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="df9a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df9a4-121">-DefaultProfile</span></span>
<span data-ttu-id="df9a4-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df9a4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df9a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df9a4-123">CommonParameters</span></span>
<span data-ttu-id="df9a4-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df9a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df9a4-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df9a4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df9a4-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df9a4-126">INPUTS</span></span>

### <span data-ttu-id="df9a4-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="df9a4-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="df9a4-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df9a4-128">OUTPUTS</span></span>

### <span data-ttu-id="df9a4-129">Microsoft.Azure.Commands.BatCH. Models. PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="df9a4-129">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="df9a4-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="df9a4-130">NOTES</span></span>

## <span data-ttu-id="df9a4-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df9a4-131">RELATED LINKS</span></span>

[<span data-ttu-id="df9a4-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="df9a4-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="df9a4-133">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="df9a4-133">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)

[<span data-ttu-id="df9a4-134">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="df9a4-134">Get-AzBatchJobStatistic</span></span>](./Get-AzBatchJobStatistic.md)
