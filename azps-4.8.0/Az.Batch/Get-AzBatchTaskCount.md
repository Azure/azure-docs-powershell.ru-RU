---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243705"
---
# <span data-ttu-id="5fe1b-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="5fe1b-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="5fe1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5fe1b-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe1b-103">Получает количество задач для указанного задания.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="5fe1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5fe1b-104">SYNTAX</span></span>

### <span data-ttu-id="5fe1b-105">Номер</span><span class="sxs-lookup"><span data-stu-id="5fe1b-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fe1b-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="5fe1b-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fe1b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fe1b-107">DESCRIPTION</span></span>
<span data-ttu-id="5fe1b-108">Командлет **Get-AzBatchTaskCount** получает число пакетных задач Azure для пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="5fe1b-109">Укажите задание с помощью параметра *JOBID* или параметра *задания* .</span><span class="sxs-lookup"><span data-stu-id="5fe1b-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="5fe1b-110">Счетчики задач предоставляют общее количество задач по активному, выполняющемуся или завершенному состоянию задачи, а также количество задач, которые были успешно выполнены или завершились сбоем.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="5fe1b-111">Задачи в состоянии подготовки считаются запущенными.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="5fe1b-112">Если validationStatus не является действительным, служба пакетной службы не смогла проверить количество состояний задачи, как указано в API "задачи списка".</span><span class="sxs-lookup"><span data-stu-id="5fe1b-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="5fe1b-113">ValidationStatus может быть недействительным, если задание имеет более 200 000 задач.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="5fe1b-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5fe1b-114">EXAMPLES</span></span>

### <span data-ttu-id="5fe1b-115">Пример 1: получение количества задач по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="5fe1b-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="5fe1b-116">Эта команда получает количество задач для Job01 заданий.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="5fe1b-117">Используйте командлет Get-AzBatchAccountKey для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5fe1b-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5fe1b-118">PARAMETERS</span></span>

### <span data-ttu-id="5fe1b-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5fe1b-119">-BatchContext</span></span>
<span data-ttu-id="5fe1b-120">Экземпляр BatchAccountContext, который будет использоваться при взаимодействии со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="5fe1b-121">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="5fe1b-122">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="5fe1b-123">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="5fe1b-124">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5fe1b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe1b-125">-DefaultProfile</span></span>
<span data-ttu-id="5fe1b-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fe1b-127">-Job</span><span class="sxs-lookup"><span data-stu-id="5fe1b-127">-Job</span></span>
<span data-ttu-id="5fe1b-128">Указывает задание, содержащее задачи, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="5fe1b-129">Чтобы получить объект **PSCloudJob** , используйте командлет Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="5fe1b-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="5fe1b-130">-JobId</span></span>
<span data-ttu-id="5fe1b-131">Идентификатор задания, для которого требуется получить количество задач.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-131">The id of the job for which to get task counts.</span></span>

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

### <span data-ttu-id="5fe1b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe1b-132">CommonParameters</span></span>
<span data-ttu-id="5fe1b-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5fe1b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe1b-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fe1b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe1b-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5fe1b-135">INPUTS</span></span>

### <span data-ttu-id="5fe1b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5fe1b-136">System.String</span></span>

### <span data-ttu-id="5fe1b-137">Microsoft.Azure.Commands.BatCH. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="5fe1b-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="5fe1b-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5fe1b-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5fe1b-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fe1b-139">OUTPUTS</span></span>

### <span data-ttu-id="5fe1b-140">Microsoft.Azure.Commands.BatCH. Models. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="5fe1b-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="5fe1b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="5fe1b-141">NOTES</span></span>

## <span data-ttu-id="5fe1b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fe1b-142">RELATED LINKS</span></span>

[<span data-ttu-id="5fe1b-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5fe1b-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5fe1b-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5fe1b-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="5fe1b-145">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="5fe1b-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
