---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
ms.openlocfilehash: 49aa971dcc9d46f5a063042cbcdf8ca449c41e94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231177"
---
# <span data-ttu-id="f59a8-101">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="f59a8-101">Get-AzBatchPoolStatistic</span></span>

## <span data-ttu-id="f59a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f59a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f59a8-103">Получает сводную статистику пула для пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f59a8-103">Gets pool summary statistics for a Batch account.</span></span>

## <span data-ttu-id="f59a8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f59a8-104">SYNTAX</span></span>

```
Get-AzBatchPoolStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f59a8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f59a8-105">DESCRIPTION</span></span>
<span data-ttu-id="f59a8-106">Для **всех пулов** в указанной учетной записи возвращается статистика по продолжительности работы.</span><span class="sxs-lookup"><span data-stu-id="f59a8-106">The **Get-AzBatchPoolStatistic** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="f59a8-107">Статистика агрегируется по всем пулам учетной записи — от создания учетной записи до времени последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="f59a8-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="f59a8-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f59a8-108">EXAMPLES</span></span>

### <span data-ttu-id="f59a8-109">Пример 1. Просмотр статистики ресурсов по всем пулам в учетной записи</span><span class="sxs-lookup"><span data-stu-id="f59a8-109">Example 1: Get resource statistics of all pools in an account</span></span>
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

<span data-ttu-id="f59a8-110">Первая команда создает ссылку на ключи учетных записей для пакетной учетной записи ContosoBatchAccount с помощью **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="f59a8-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="f59a8-111">Эта ссылка на объект сохраняется в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="f59a8-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="f59a8-112">Вторая команда получает статистику по всем пулам в указанной учетной записи, а затем сохраняет их в $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="f59a8-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="f59a8-113">В конечной команде отображается свойство **ResourceStatistics** $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="f59a8-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="f59a8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f59a8-114">PARAMETERS</span></span>

### <span data-ttu-id="f59a8-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f59a8-115">-BatchContext</span></span>
<span data-ttu-id="f59a8-116">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="f59a8-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f59a8-117">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f59a8-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f59a8-118">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="f59a8-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f59a8-119">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f59a8-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f59a8-120">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f59a8-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f59a8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59a8-121">-DefaultProfile</span></span>
<span data-ttu-id="f59a8-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f59a8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f59a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59a8-123">CommonParameters</span></span>
<span data-ttu-id="f59a8-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f59a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59a8-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f59a8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59a8-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f59a8-126">INPUTS</span></span>

### <span data-ttu-id="f59a8-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f59a8-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f59a8-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f59a8-128">OUTPUTS</span></span>

### <span data-ttu-id="f59a8-129">Microsoft.Azure.Commands.Batch. Models.PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="f59a8-129">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="f59a8-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f59a8-130">NOTES</span></span>

## <span data-ttu-id="f59a8-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f59a8-131">RELATED LINKS</span></span>

[<span data-ttu-id="f59a8-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f59a8-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f59a8-133">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="f59a8-133">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)

[<span data-ttu-id="f59a8-134">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="f59a8-134">Get-AzBatchJobStatistic</span></span>](./Get-AzBatchJobStatistic.md)
