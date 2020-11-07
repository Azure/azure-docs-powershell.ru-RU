---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: 2e19e6b1733ccc3dfe0a802756e2c0a517232803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734906"
---
# <span data-ttu-id="c750e-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="c750e-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="c750e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c750e-102">SYNOPSIS</span></span>
<span data-ttu-id="c750e-103">Отключение пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="c750e-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c750e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c750e-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c750e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c750e-105">DESCRIPTION</span></span>
<span data-ttu-id="c750e-106">Командлет **Disable-AzureBatchJob** Отключает пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="c750e-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="c750e-107">После включения задания может выполняться новая задача.</span><span class="sxs-lookup"><span data-stu-id="c750e-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="c750e-108">Отключенные задания не выполняют новые задачи.</span><span class="sxs-lookup"><span data-stu-id="c750e-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="c750e-109">Вы можете включить отключенное задание позже.</span><span class="sxs-lookup"><span data-stu-id="c750e-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="c750e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c750e-110">EXAMPLES</span></span>

### <span data-ttu-id="c750e-111">Пример 1: отключение пакетного задания</span><span class="sxs-lookup"><span data-stu-id="c750e-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="c750e-112">Эта команда отключает задачу с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="c750e-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="c750e-113">Команда прекращает выполнение активных задач для задания.</span><span class="sxs-lookup"><span data-stu-id="c750e-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="c750e-114">Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="c750e-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="c750e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c750e-115">PARAMETERS</span></span>

### <span data-ttu-id="c750e-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c750e-116">-BatchContext</span></span>
<span data-ttu-id="c750e-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="c750e-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c750e-118">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="c750e-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c750e-119">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="c750e-119">-DisableJobOption</span></span>
<span data-ttu-id="c750e-120">Указывает, что делать с активными задачами, связанными с заданием, которое отключается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c750e-120">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="c750e-121">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="c750e-121">Valid values are:</span></span> 

- <span data-ttu-id="c750e-122">Возобновляемая очередь</span><span class="sxs-lookup"><span data-stu-id="c750e-122">Requeue</span></span> 
- <span data-ttu-id="c750e-123">Разорван</span><span class="sxs-lookup"><span data-stu-id="c750e-123">Terminate</span></span> 
- <span data-ttu-id="c750e-124">Ожидающе</span><span class="sxs-lookup"><span data-stu-id="c750e-124">Wait</span></span>

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

### <span data-ttu-id="c750e-125">-ID</span><span class="sxs-lookup"><span data-stu-id="c750e-125">-Id</span></span>
<span data-ttu-id="c750e-126">Указывает ИД задания, которое отключает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c750e-126">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="c750e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c750e-127">-DefaultProfile</span></span>
<span data-ttu-id="c750e-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c750e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c750e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c750e-129">CommonParameters</span></span>
<span data-ttu-id="c750e-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c750e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c750e-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c750e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c750e-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c750e-132">INPUTS</span></span>

### <span data-ttu-id="c750e-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c750e-133">BatchAccountContext</span></span>
<span data-ttu-id="c750e-134">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c750e-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c750e-135">Подстрок</span><span class="sxs-lookup"><span data-stu-id="c750e-135">String</span></span>
<span data-ttu-id="c750e-136">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c750e-136">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c750e-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c750e-137">OUTPUTS</span></span>

## <span data-ttu-id="c750e-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c750e-138">NOTES</span></span>

## <span data-ttu-id="c750e-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c750e-139">RELATED LINKS</span></span>

[<span data-ttu-id="c750e-140">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="c750e-140">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="c750e-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c750e-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c750e-142">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="c750e-142">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="c750e-143">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="c750e-143">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="c750e-144">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="c750e-144">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="c750e-145">Остановить-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="c750e-145">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="c750e-146">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="c750e-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


