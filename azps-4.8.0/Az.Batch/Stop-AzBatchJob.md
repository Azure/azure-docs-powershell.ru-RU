---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: ffaac0bdd4a144cc3979da052c0c40cb824862f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079833"
---
# <span data-ttu-id="a302e-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a302e-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="a302e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a302e-102">SYNOPSIS</span></span>
<span data-ttu-id="a302e-103">Останавливает пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="a302e-103">Stops a Batch job.</span></span>

## <span data-ttu-id="a302e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a302e-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a302e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a302e-105">DESCRIPTION</span></span>
<span data-ttu-id="a302e-106">Командлет **Stop-AzBatchJob** останавливает пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="a302e-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="a302e-107">Эта команда помечает задачу как завершенную.</span><span class="sxs-lookup"><span data-stu-id="a302e-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="a302e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a302e-108">EXAMPLES</span></span>

### <span data-ttu-id="a302e-109">Пример 1: остановка пакетного задания</span><span class="sxs-lookup"><span data-stu-id="a302e-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="a302e-110">Эта команда останавливает задачу с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="a302e-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="a302e-111">В команде указывается причина, по которой вы решили остановить задание.</span><span class="sxs-lookup"><span data-stu-id="a302e-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="a302e-112">Используйте командлет Get-AzBatchAccountKey для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="a302e-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a302e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a302e-113">PARAMETERS</span></span>

### <span data-ttu-id="a302e-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a302e-114">-BatchContext</span></span>
<span data-ttu-id="a302e-115">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="a302e-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a302e-116">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="a302e-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a302e-117">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="a302e-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a302e-118">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="a302e-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a302e-119">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a302e-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a302e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a302e-120">-DefaultProfile</span></span>
<span data-ttu-id="a302e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a302e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a302e-122">-ID</span><span class="sxs-lookup"><span data-stu-id="a302e-122">-Id</span></span>
<span data-ttu-id="a302e-123">Указывает идентификатор задания, которое останавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a302e-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="a302e-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="a302e-124">-TerminateReason</span></span>
<span data-ttu-id="a302e-125">Указывает причину, по которой вы решили остановить задание.</span><span class="sxs-lookup"><span data-stu-id="a302e-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="a302e-126">Этот командлет хранит этот текст как свойство **TerminateReason** задания.</span><span class="sxs-lookup"><span data-stu-id="a302e-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="a302e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a302e-127">CommonParameters</span></span>
<span data-ttu-id="a302e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a302e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a302e-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a302e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a302e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a302e-130">INPUTS</span></span>

### <span data-ttu-id="a302e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a302e-131">System.String</span></span>

### <span data-ttu-id="a302e-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a302e-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a302e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a302e-133">OUTPUTS</span></span>

### <span data-ttu-id="a302e-134">System. void</span><span class="sxs-lookup"><span data-stu-id="a302e-134">System.Void</span></span>

## <span data-ttu-id="a302e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a302e-135">NOTES</span></span>

## <span data-ttu-id="a302e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a302e-136">RELATED LINKS</span></span>

[<span data-ttu-id="a302e-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a302e-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="a302e-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a302e-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="a302e-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a302e-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a302e-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a302e-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="a302e-141">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a302e-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="a302e-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a302e-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="a302e-143">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="a302e-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)