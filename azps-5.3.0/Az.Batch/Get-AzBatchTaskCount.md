---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509666"
---
# <span data-ttu-id="32a10-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="32a10-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="32a10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32a10-102">SYNOPSIS</span></span>
<span data-ttu-id="32a10-103">Возвращает количество задач для указанного задания.</span><span class="sxs-lookup"><span data-stu-id="32a10-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="32a10-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32a10-104">SYNTAX</span></span>

### <span data-ttu-id="32a10-105">ИД</span><span class="sxs-lookup"><span data-stu-id="32a10-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32a10-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="32a10-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32a10-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32a10-107">DESCRIPTION</span></span>
<span data-ttu-id="32a10-108">Для выполнения пакетных заданий количество пакетных задач Azure получается с использованием **cmdlet Get-AzBatchTaskCount.**</span><span class="sxs-lookup"><span data-stu-id="32a10-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="32a10-109">Задание можно указать с помощью *параметров JobId* и *JobId.*</span><span class="sxs-lookup"><span data-stu-id="32a10-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="32a10-110">Подсчитываются количество задач по активным, запущенным или завершенным задачам, а также количество успешно выполненных или сбойных задач.</span><span class="sxs-lookup"><span data-stu-id="32a10-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="32a10-111">Задачи в состоянии подготовки посчитаются работающими.</span><span class="sxs-lookup"><span data-stu-id="32a10-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="32a10-112">Если состояние проверки неоценен, пакетная служба не может проверить количество состояния в состоянии задач, как полось в API задач списка.</span><span class="sxs-lookup"><span data-stu-id="32a10-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="32a10-113">Если задание содержит более 200 000 задач, проверку можно не оценки.</span><span class="sxs-lookup"><span data-stu-id="32a10-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="32a10-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32a10-114">EXAMPLES</span></span>

### <span data-ttu-id="32a10-115">Пример 1. Подсчет задач по ИД</span><span class="sxs-lookup"><span data-stu-id="32a10-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="32a10-116">Эта команда получает количество задач для задания01.</span><span class="sxs-lookup"><span data-stu-id="32a10-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="32a10-117">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="32a10-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="32a10-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32a10-118">PARAMETERS</span></span>

### <span data-ttu-id="32a10-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="32a10-119">-BatchContext</span></span>
<span data-ttu-id="32a10-120">Экземпляр BatchAccountContext, который используется при взаимодействии со службой batch.</span><span class="sxs-lookup"><span data-stu-id="32a10-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="32a10-121">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="32a10-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="32a10-122">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="32a10-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="32a10-123">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="32a10-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="32a10-124">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="32a10-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="32a10-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a10-125">-DefaultProfile</span></span>
<span data-ttu-id="32a10-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32a10-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32a10-127">-Job</span><span class="sxs-lookup"><span data-stu-id="32a10-127">-Job</span></span>
<span data-ttu-id="32a10-128">Задание, которое содержит задачи, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32a10-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="32a10-129">Чтобы получить объект **PSCloudJob,** используйте Get-AzBatchJob-код.</span><span class="sxs-lookup"><span data-stu-id="32a10-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32a10-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="32a10-130">-JobId</span></span>
<span data-ttu-id="32a10-131">ИД задания, для которого требуется подсчитать количество задач.</span><span class="sxs-lookup"><span data-stu-id="32a10-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a10-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a10-132">CommonParameters</span></span>
<span data-ttu-id="32a10-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32a10-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a10-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32a10-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a10-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32a10-135">INPUTS</span></span>

### <span data-ttu-id="32a10-136">System.String</span><span class="sxs-lookup"><span data-stu-id="32a10-136">System.String</span></span>

### <span data-ttu-id="32a10-137">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="32a10-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="32a10-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="32a10-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="32a10-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32a10-139">OUTPUTS</span></span>

### <span data-ttu-id="32a10-140">Microsoft.Azure.Commands.Batch. Models.PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="32a10-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="32a10-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32a10-141">NOTES</span></span>

## <span data-ttu-id="32a10-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32a10-142">RELATED LINKS</span></span>

[<span data-ttu-id="32a10-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="32a10-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="32a10-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="32a10-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="32a10-145">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="32a10-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
