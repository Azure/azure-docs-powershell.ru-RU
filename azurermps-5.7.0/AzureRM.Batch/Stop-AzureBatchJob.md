---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 0f33807c112ea770e3d02d972d52ca7a166bb791
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559299"
---
# <span data-ttu-id="9d1da-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9d1da-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="9d1da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d1da-102">SYNOPSIS</span></span>
<span data-ttu-id="9d1da-103">Останавливает пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="9d1da-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d1da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d1da-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d1da-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d1da-105">DESCRIPTION</span></span>
<span data-ttu-id="9d1da-106">Командлет **Stop-AzureBatchJob** останавливает пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="9d1da-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="9d1da-107">Эта команда помечает задачу как завершенную.</span><span class="sxs-lookup"><span data-stu-id="9d1da-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="9d1da-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d1da-108">EXAMPLES</span></span>

### <span data-ttu-id="9d1da-109">Пример 1: остановка пакетного задания</span><span class="sxs-lookup"><span data-stu-id="9d1da-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="9d1da-110">Эта команда останавливает задачу с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="9d1da-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="9d1da-111">В команде указывается причина, по которой вы решили остановить задание.</span><span class="sxs-lookup"><span data-stu-id="9d1da-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="9d1da-112">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="9d1da-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="9d1da-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d1da-113">PARAMETERS</span></span>

### <span data-ttu-id="9d1da-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9d1da-114">-BatchContext</span></span>
<span data-ttu-id="9d1da-115">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="9d1da-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9d1da-116">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="9d1da-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9d1da-117">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="9d1da-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9d1da-118">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="9d1da-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9d1da-119">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9d1da-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9d1da-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d1da-120">-DefaultProfile</span></span>
<span data-ttu-id="9d1da-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d1da-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d1da-122">-ID</span><span class="sxs-lookup"><span data-stu-id="9d1da-122">-Id</span></span>
<span data-ttu-id="9d1da-123">Указывает идентификатор задания, которое останавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9d1da-123">Specifies the ID of the job that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1da-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="9d1da-124">-TerminateReason</span></span>
<span data-ttu-id="9d1da-125">Указывает причину, по которой вы решили остановить задание.</span><span class="sxs-lookup"><span data-stu-id="9d1da-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="9d1da-126">Этот командлет хранит этот текст как свойство **TerminateReason** задания.</span><span class="sxs-lookup"><span data-stu-id="9d1da-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d1da-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d1da-127">CommonParameters</span></span>
<span data-ttu-id="9d1da-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d1da-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d1da-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d1da-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d1da-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d1da-130">INPUTS</span></span>

### <span data-ttu-id="9d1da-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9d1da-131">BatchAccountContext</span></span>
<span data-ttu-id="9d1da-132">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9d1da-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="9d1da-133">Подстрок</span><span class="sxs-lookup"><span data-stu-id="9d1da-133">String</span></span>
<span data-ttu-id="9d1da-134">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9d1da-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="9d1da-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d1da-135">OUTPUTS</span></span>

## <span data-ttu-id="9d1da-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d1da-136">NOTES</span></span>

## <span data-ttu-id="9d1da-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d1da-137">RELATED LINKS</span></span>

[<span data-ttu-id="9d1da-138">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9d1da-138">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="9d1da-139">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9d1da-139">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="9d1da-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9d1da-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9d1da-141">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9d1da-141">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="9d1da-142">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9d1da-142">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="9d1da-143">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="9d1da-143">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="9d1da-144">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="9d1da-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


