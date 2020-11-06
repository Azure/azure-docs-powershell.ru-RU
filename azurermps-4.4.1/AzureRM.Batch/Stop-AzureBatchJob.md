---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 8893ed4002e576e257cd9b885d5773c5851edde0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566756"
---
# <span data-ttu-id="a8760-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a8760-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="a8760-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8760-102">SYNOPSIS</span></span>
<span data-ttu-id="a8760-103">Останавливает пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="a8760-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8760-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8760-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8760-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8760-105">DESCRIPTION</span></span>
<span data-ttu-id="a8760-106">Командлет **Stop-AzureBatchJob** останавливает пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="a8760-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="a8760-107">Эта команда помечает задачу как завершенную.</span><span class="sxs-lookup"><span data-stu-id="a8760-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="a8760-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8760-108">EXAMPLES</span></span>

### <span data-ttu-id="a8760-109">Пример 1: остановка пакетного задания</span><span class="sxs-lookup"><span data-stu-id="a8760-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="a8760-110">Эта команда останавливает задачу с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="a8760-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="a8760-111">В команде указывается причина, по которой вы решили остановить задание.</span><span class="sxs-lookup"><span data-stu-id="a8760-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="a8760-112">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="a8760-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a8760-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8760-113">PARAMETERS</span></span>

### <span data-ttu-id="a8760-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a8760-114">-BatchContext</span></span>
<span data-ttu-id="a8760-115">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="a8760-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a8760-116">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="a8760-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="a8760-117">-ID</span><span class="sxs-lookup"><span data-stu-id="a8760-117">-Id</span></span>
<span data-ttu-id="a8760-118">Указывает идентификатор задания, которое останавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a8760-118">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="a8760-119">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="a8760-119">-TerminateReason</span></span>
<span data-ttu-id="a8760-120">Указывает причину, по которой вы решили остановить задание.</span><span class="sxs-lookup"><span data-stu-id="a8760-120">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="a8760-121">Этот командлет хранит этот текст как свойство **TerminateReason** задания.</span><span class="sxs-lookup"><span data-stu-id="a8760-121">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8760-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8760-122">-DefaultProfile</span></span>
<span data-ttu-id="a8760-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8760-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8760-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8760-124">CommonParameters</span></span>
<span data-ttu-id="a8760-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8760-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8760-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8760-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8760-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8760-127">INPUTS</span></span>

### <span data-ttu-id="a8760-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a8760-128">BatchAccountContext</span></span>
<span data-ttu-id="a8760-129">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a8760-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a8760-130">Подстрок</span><span class="sxs-lookup"><span data-stu-id="a8760-130">String</span></span>
<span data-ttu-id="a8760-131">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a8760-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a8760-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8760-132">OUTPUTS</span></span>

## <span data-ttu-id="a8760-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8760-133">NOTES</span></span>

## <span data-ttu-id="a8760-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8760-134">RELATED LINKS</span></span>

[<span data-ttu-id="a8760-135">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a8760-135">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="a8760-136">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a8760-136">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="a8760-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a8760-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a8760-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a8760-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="a8760-139">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a8760-139">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="a8760-140">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a8760-140">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="a8760-141">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="a8760-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


