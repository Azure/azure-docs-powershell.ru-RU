---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: fabc983e8c7b70685477a640d408beb65251b253
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999015"
---
# <span data-ttu-id="e0b9d-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e0b9d-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="e0b9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b9d-103">Отключает пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-103">Disables a Batch job.</span></span>

## <span data-ttu-id="e0b9d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0b9d-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0b9d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0b9d-105">DESCRIPTION</span></span>
<span data-ttu-id="e0b9d-106">Для **отключения пакета Azure отключается cmdlet Disable-AzBatchJob.**</span><span class="sxs-lookup"><span data-stu-id="e0b9d-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="e0b9d-107">После этого можно выполнять новые задачи.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="e0b9d-108">Отключенные задания не запускают новые задачи.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="e0b9d-109">Вы можете включить отключенную работу позже.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="e0b9d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0b9d-110">EXAMPLES</span></span>

### <span data-ttu-id="e0b9d-111">Пример 1. Отключение задания пакета</span><span class="sxs-lookup"><span data-stu-id="e0b9d-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="e0b9d-112">Эта команда отключает задание с ИД-000001.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e0b9d-113">Команда завершает активные задачи для задания.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="e0b9d-114">Чтобы назначить контекст переменной $Context, используйте $Context **AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="e0b9d-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e0b9d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0b9d-115">PARAMETERS</span></span>

### <span data-ttu-id="e0b9d-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e0b9d-116">-BatchContext</span></span>
<span data-ttu-id="e0b9d-117">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e0b9d-118">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e0b9d-119">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e0b9d-120">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e0b9d-121">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e0b9d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b9d-122">-DefaultProfile</span></span>
<span data-ttu-id="e0b9d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0b9d-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="e0b9d-124">-DisableJobOption</span></span>
<span data-ttu-id="e0b9d-125">Определяет, что делать с активными задачами, связанными с заданием, которое отключает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="e0b9d-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e0b9d-126">Valid values are:</span></span>
- <span data-ttu-id="e0b9d-127">Просрочено</span><span class="sxs-lookup"><span data-stu-id="e0b9d-127">Requeue</span></span>
- <span data-ttu-id="e0b9d-128">Завершить</span><span class="sxs-lookup"><span data-stu-id="e0b9d-128">Terminate</span></span>
- <span data-ttu-id="e0b9d-129">Подождите</span><span class="sxs-lookup"><span data-stu-id="e0b9d-129">Wait</span></span>

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

### <span data-ttu-id="e0b9d-130">-Id</span><span class="sxs-lookup"><span data-stu-id="e0b9d-130">-Id</span></span>
<span data-ttu-id="e0b9d-131">Определяет код задания, которое этот cmdlet отключает.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="e0b9d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b9d-132">CommonParameters</span></span>
<span data-ttu-id="e0b9d-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b9d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b9d-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0b9d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b9d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0b9d-135">INPUTS</span></span>

### <span data-ttu-id="e0b9d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e0b9d-136">System.String</span></span>

### <span data-ttu-id="e0b9d-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e0b9d-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e0b9d-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0b9d-138">OUTPUTS</span></span>

### <span data-ttu-id="e0b9d-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="e0b9d-139">System.Void</span></span>

## <span data-ttu-id="e0b9d-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0b9d-140">NOTES</span></span>

## <span data-ttu-id="e0b9d-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0b9d-141">RELATED LINKS</span></span>

[<span data-ttu-id="e0b9d-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e0b9d-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="e0b9d-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e0b9d-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e0b9d-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e0b9d-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="e0b9d-145">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e0b9d-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="e0b9d-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e0b9d-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="e0b9d-147">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e0b9d-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="e0b9d-148">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="e0b9d-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
