---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: 791562b4cfa7f2ee5cb446e70cad59074389c25c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731823"
---
# <span data-ttu-id="bd8b1-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="bd8b1-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="bd8b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd8b1-103">Останавливает пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-103">Stops a Batch job.</span></span>

## <span data-ttu-id="bd8b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd8b1-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd8b1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd8b1-105">DESCRIPTION</span></span>
<span data-ttu-id="bd8b1-106">Командлет **Stop-AzBatchJob** останавливает пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="bd8b1-107">Эта команда помечает задачу как завершенную.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="bd8b1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd8b1-108">EXAMPLES</span></span>

### <span data-ttu-id="bd8b1-109">Пример 1: остановка пакетного задания</span><span class="sxs-lookup"><span data-stu-id="bd8b1-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="bd8b1-110">Эта команда останавливает задачу с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="bd8b1-111">В команде указывается причина, по которой вы решили остановить задание.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="bd8b1-112">Используйте командлет Get-AzBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-112">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="bd8b1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd8b1-113">PARAMETERS</span></span>

### <span data-ttu-id="bd8b1-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bd8b1-114">-BatchContext</span></span>
<span data-ttu-id="bd8b1-115">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bd8b1-116">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bd8b1-117">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-117">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bd8b1-118">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bd8b1-119">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bd8b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd8b1-120">-DefaultProfile</span></span>
<span data-ttu-id="bd8b1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd8b1-122">-ID</span><span class="sxs-lookup"><span data-stu-id="bd8b1-122">-Id</span></span>
<span data-ttu-id="bd8b1-123">Указывает идентификатор задания, которое останавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="bd8b1-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="bd8b1-124">-TerminateReason</span></span>
<span data-ttu-id="bd8b1-125">Указывает причину, по которой вы решили остановить задание.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="bd8b1-126">Этот командлет хранит этот текст как свойство **TerminateReason** задания.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="bd8b1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd8b1-127">CommonParameters</span></span>
<span data-ttu-id="bd8b1-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd8b1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd8b1-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd8b1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd8b1-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd8b1-130">INPUTS</span></span>

### <span data-ttu-id="bd8b1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bd8b1-131">System.String</span></span>

### <span data-ttu-id="bd8b1-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bd8b1-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bd8b1-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd8b1-133">OUTPUTS</span></span>

### <span data-ttu-id="bd8b1-134">System. void</span><span class="sxs-lookup"><span data-stu-id="bd8b1-134">System.Void</span></span>

## <span data-ttu-id="bd8b1-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd8b1-135">NOTES</span></span>

## <span data-ttu-id="bd8b1-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd8b1-136">RELATED LINKS</span></span>

[<span data-ttu-id="bd8b1-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="bd8b1-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="bd8b1-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="bd8b1-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="bd8b1-139">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bd8b1-139">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bd8b1-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="bd8b1-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="bd8b1-141">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="bd8b1-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="bd8b1-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="bd8b1-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="bd8b1-143">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="bd8b1-143">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


