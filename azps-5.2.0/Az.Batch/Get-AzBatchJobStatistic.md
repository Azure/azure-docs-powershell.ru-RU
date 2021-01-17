---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: 11532648242438983ae1bc9222dbc3ac12fa05e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417884"
---
# <span data-ttu-id="d5a63-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="d5a63-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="d5a63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5a63-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a63-103">Получает сводную статистику по заданиям для учетной записи пакета.</span><span class="sxs-lookup"><span data-stu-id="d5a63-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="d5a63-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d5a63-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5a63-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5a63-105">DESCRIPTION</span></span>
<span data-ttu-id="d5a63-106">Для всех заданий в учетной записи Azure Batch можно получить сводную статистику по всем заданиям в **Get-AzBatchJobStatistic.**</span><span class="sxs-lookup"><span data-stu-id="d5a63-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="d5a63-107">Статистика агрегируется по всем заданиям в учетной записи— от создания учетной записи до времени последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="d5a63-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="d5a63-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d5a63-108">EXAMPLES</span></span>

### <span data-ttu-id="d5a63-109">Пример 1. Получить сводную статистику по всем заданиям</span><span class="sxs-lookup"><span data-stu-id="d5a63-109">Example 1: Get summary statistics for all jobs</span></span>
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

<span data-ttu-id="d5a63-110">Первая команда создает ссылку на ключи учетных записей для пакетной учетной записи ContosoBatchAccount с помощью **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="d5a63-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="d5a63-111">Эта ссылка на объект сохраняется в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="d5a63-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="d5a63-112">Вторая команда получает сводную статистику по всем заданиям.</span><span class="sxs-lookup"><span data-stu-id="d5a63-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="d5a63-113">Для этой команды $Context значение первой команды.</span><span class="sxs-lookup"><span data-stu-id="d5a63-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="d5a63-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5a63-114">PARAMETERS</span></span>

### <span data-ttu-id="d5a63-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d5a63-115">-BatchContext</span></span>
<span data-ttu-id="d5a63-116">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="d5a63-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d5a63-117">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d5a63-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d5a63-118">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="d5a63-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d5a63-119">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d5a63-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d5a63-120">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d5a63-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d5a63-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a63-121">-DefaultProfile</span></span>
<span data-ttu-id="d5a63-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a63-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5a63-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a63-123">CommonParameters</span></span>
<span data-ttu-id="d5a63-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a63-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a63-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5a63-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a63-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5a63-126">INPUTS</span></span>

### <span data-ttu-id="d5a63-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d5a63-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d5a63-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5a63-128">OUTPUTS</span></span>

### <span data-ttu-id="d5a63-129">Microsoft.Azure.Commands.Batch. Models.PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="d5a63-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="d5a63-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d5a63-130">NOTES</span></span>

## <span data-ttu-id="d5a63-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5a63-131">RELATED LINKS</span></span>

[<span data-ttu-id="d5a63-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d5a63-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d5a63-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="d5a63-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="d5a63-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="d5a63-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)
