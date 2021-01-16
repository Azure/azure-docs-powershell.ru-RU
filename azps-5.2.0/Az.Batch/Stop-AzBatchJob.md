---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: ffaac0bdd4a144cc3979da052c0c40cb824862f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409100"
---
# <span data-ttu-id="6f800-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6f800-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="6f800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f800-102">SYNOPSIS</span></span>
<span data-ttu-id="6f800-103">Остановка пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="6f800-103">Stops a Batch job.</span></span>

## <span data-ttu-id="6f800-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6f800-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f800-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f800-105">DESCRIPTION</span></span>
<span data-ttu-id="6f800-106">Из-за нее можно прекратить работу пакета Azure с использованием cmdlet **Stop-AzBatchJob.**</span><span class="sxs-lookup"><span data-stu-id="6f800-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="6f800-107">Эта команда пометит задание как выполненную.</span><span class="sxs-lookup"><span data-stu-id="6f800-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="6f800-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6f800-108">EXAMPLES</span></span>

### <span data-ttu-id="6f800-109">Пример 1. Остановка пакета</span><span class="sxs-lookup"><span data-stu-id="6f800-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="6f800-110">Эта команда останавливает задание с ИД-000001.</span><span class="sxs-lookup"><span data-stu-id="6f800-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="6f800-111">Эта команда указывает причину, по которой вы решили остановить задание.</span><span class="sxs-lookup"><span data-stu-id="6f800-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="6f800-112">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="6f800-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="6f800-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f800-113">PARAMETERS</span></span>

### <span data-ttu-id="6f800-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6f800-114">-BatchContext</span></span>
<span data-ttu-id="6f800-115">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="6f800-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6f800-116">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6f800-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6f800-117">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="6f800-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6f800-118">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6f800-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6f800-119">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6f800-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6f800-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f800-120">-DefaultProfile</span></span>
<span data-ttu-id="6f800-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f800-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f800-122">-Id</span><span class="sxs-lookup"><span data-stu-id="6f800-122">-Id</span></span>
<span data-ttu-id="6f800-123">Определяет код задания, которое останавливает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f800-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="6f800-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="6f800-124">-TerminateReason</span></span>
<span data-ttu-id="6f800-125">Указывает причину, по которой вы решили прекратить работу.</span><span class="sxs-lookup"><span data-stu-id="6f800-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="6f800-126">Этот cmdlet сохраняет этот текст как свойство **TerminateReason** задания.</span><span class="sxs-lookup"><span data-stu-id="6f800-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="6f800-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f800-127">CommonParameters</span></span>
<span data-ttu-id="6f800-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f800-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f800-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f800-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f800-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f800-130">INPUTS</span></span>

### <span data-ttu-id="6f800-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6f800-131">System.String</span></span>

### <span data-ttu-id="6f800-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6f800-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6f800-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6f800-133">OUTPUTS</span></span>

### <span data-ttu-id="6f800-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="6f800-134">System.Void</span></span>

## <span data-ttu-id="6f800-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6f800-135">NOTES</span></span>

## <span data-ttu-id="6f800-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f800-136">RELATED LINKS</span></span>

[<span data-ttu-id="6f800-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6f800-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="6f800-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6f800-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="6f800-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6f800-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6f800-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6f800-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="6f800-141">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6f800-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="6f800-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6f800-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="6f800-143">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="6f800-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
