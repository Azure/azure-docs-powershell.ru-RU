---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: a25c31c0b73a42e0d64b567b6bc2529bf4ebf258
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245993"
---
# <span data-ttu-id="aa3b0-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="aa3b0-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="aa3b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa3b0-102">SYNOPSIS</span></span>
<span data-ttu-id="aa3b0-103">Отключение пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-103">Disables a Batch job.</span></span>

## <span data-ttu-id="aa3b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa3b0-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa3b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa3b0-105">DESCRIPTION</span></span>
<span data-ttu-id="aa3b0-106">Командлет **Disable-AzBatchJob** Отключает пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="aa3b0-107">После включения задания может выполняться новая задача.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="aa3b0-108">Отключенные задания не выполняют новые задачи.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="aa3b0-109">Вы можете включить отключенное задание позже.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="aa3b0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa3b0-110">EXAMPLES</span></span>

### <span data-ttu-id="aa3b0-111">Пример 1: отключение пакетного задания</span><span class="sxs-lookup"><span data-stu-id="aa3b0-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="aa3b0-112">Эта команда отключает задачу с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="aa3b0-113">Команда прекращает выполнение активных задач для задания.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="aa3b0-114">Используйте командлет **Get-AzBatchAccountKey** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="aa3b0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa3b0-115">PARAMETERS</span></span>

### <span data-ttu-id="aa3b0-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="aa3b0-116">-BatchContext</span></span>
<span data-ttu-id="aa3b0-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="aa3b0-118">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="aa3b0-119">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="aa3b0-120">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="aa3b0-121">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="aa3b0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa3b0-122">-DefaultProfile</span></span>
<span data-ttu-id="aa3b0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa3b0-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="aa3b0-124">-DisableJobOption</span></span>
<span data-ttu-id="aa3b0-125">Указывает, что делать с активными задачами, связанными с заданием, которое отключается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="aa3b0-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="aa3b0-126">Valid values are:</span></span>
- <span data-ttu-id="aa3b0-127">Возобновляемая очередь</span><span class="sxs-lookup"><span data-stu-id="aa3b0-127">Requeue</span></span>
- <span data-ttu-id="aa3b0-128">Разорван</span><span class="sxs-lookup"><span data-stu-id="aa3b0-128">Terminate</span></span>
- <span data-ttu-id="aa3b0-129">Ожидающе</span><span class="sxs-lookup"><span data-stu-id="aa3b0-129">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa3b0-130">-ID</span><span class="sxs-lookup"><span data-stu-id="aa3b0-130">-Id</span></span>
<span data-ttu-id="aa3b0-131">Указывает ИД задания, которое отключает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa3b0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa3b0-132">CommonParameters</span></span>
<span data-ttu-id="aa3b0-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa3b0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa3b0-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa3b0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa3b0-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa3b0-135">INPUTS</span></span>

### <span data-ttu-id="aa3b0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="aa3b0-136">System.String</span></span>

### <span data-ttu-id="aa3b0-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aa3b0-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="aa3b0-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa3b0-138">OUTPUTS</span></span>

### <span data-ttu-id="aa3b0-139">System. void</span><span class="sxs-lookup"><span data-stu-id="aa3b0-139">System.Void</span></span>

## <span data-ttu-id="aa3b0-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa3b0-140">NOTES</span></span>

## <span data-ttu-id="aa3b0-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa3b0-141">RELATED LINKS</span></span>

[<span data-ttu-id="aa3b0-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="aa3b0-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="aa3b0-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="aa3b0-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="aa3b0-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="aa3b0-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="aa3b0-145">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="aa3b0-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="aa3b0-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="aa3b0-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="aa3b0-147">Остановить-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="aa3b0-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="aa3b0-148">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="aa3b0-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
