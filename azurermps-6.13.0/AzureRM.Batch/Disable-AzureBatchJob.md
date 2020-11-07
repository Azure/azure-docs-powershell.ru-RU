---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: 141702ec7c60dcdb2dd94d5e259b2f14c8475316
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732806"
---
# <span data-ttu-id="a4010-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4010-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="a4010-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4010-102">SYNOPSIS</span></span>
<span data-ttu-id="a4010-103">Отключение пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="a4010-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4010-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4010-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4010-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4010-105">DESCRIPTION</span></span>
<span data-ttu-id="a4010-106">Командлет **Disable-AzureBatchJob** Отключает пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="a4010-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="a4010-107">После включения задания может выполняться новая задача.</span><span class="sxs-lookup"><span data-stu-id="a4010-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="a4010-108">Отключенные задания не выполняют новые задачи.</span><span class="sxs-lookup"><span data-stu-id="a4010-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="a4010-109">Вы можете включить отключенное задание позже.</span><span class="sxs-lookup"><span data-stu-id="a4010-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="a4010-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4010-110">EXAMPLES</span></span>

### <span data-ttu-id="a4010-111">Пример 1: отключение пакетного задания</span><span class="sxs-lookup"><span data-stu-id="a4010-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="a4010-112">Эта команда отключает задачу с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="a4010-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="a4010-113">Команда прекращает выполнение активных задач для задания.</span><span class="sxs-lookup"><span data-stu-id="a4010-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="a4010-114">Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="a4010-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a4010-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4010-115">PARAMETERS</span></span>

### <span data-ttu-id="a4010-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a4010-116">-BatchContext</span></span>
<span data-ttu-id="a4010-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="a4010-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a4010-118">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="a4010-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a4010-119">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="a4010-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a4010-120">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="a4010-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a4010-121">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a4010-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a4010-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4010-122">-DefaultProfile</span></span>
<span data-ttu-id="a4010-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4010-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4010-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="a4010-124">-DisableJobOption</span></span>
<span data-ttu-id="a4010-125">Указывает, что делать с активными задачами, связанными с заданием, которое отключается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a4010-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="a4010-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a4010-126">Valid values are:</span></span> 
- <span data-ttu-id="a4010-127">Возобновляемая очередь</span><span class="sxs-lookup"><span data-stu-id="a4010-127">Requeue</span></span> 
- <span data-ttu-id="a4010-128">Разорван</span><span class="sxs-lookup"><span data-stu-id="a4010-128">Terminate</span></span> 
- <span data-ttu-id="a4010-129">Ожидающе</span><span class="sxs-lookup"><span data-stu-id="a4010-129">Wait</span></span>

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

### <span data-ttu-id="a4010-130">-ID</span><span class="sxs-lookup"><span data-stu-id="a4010-130">-Id</span></span>
<span data-ttu-id="a4010-131">Указывает ИД задания, которое отключает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a4010-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="a4010-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4010-132">CommonParameters</span></span>
<span data-ttu-id="a4010-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4010-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4010-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4010-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4010-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4010-135">INPUTS</span></span>

### <span data-ttu-id="a4010-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a4010-136">System.String</span></span>

### <span data-ttu-id="a4010-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a4010-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="a4010-138">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a4010-138">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="a4010-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4010-139">OUTPUTS</span></span>

### <span data-ttu-id="a4010-140">System. void</span><span class="sxs-lookup"><span data-stu-id="a4010-140">System.Void</span></span>

## <span data-ttu-id="a4010-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4010-141">NOTES</span></span>

## <span data-ttu-id="a4010-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4010-142">RELATED LINKS</span></span>

[<span data-ttu-id="a4010-143">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4010-143">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="a4010-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a4010-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a4010-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4010-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="a4010-146">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4010-146">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="a4010-147">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4010-147">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="a4010-148">Остановить-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4010-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="a4010-149">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="a4010-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


