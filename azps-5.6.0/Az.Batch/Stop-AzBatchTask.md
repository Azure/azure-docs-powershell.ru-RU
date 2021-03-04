---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 5550603bc4204937e8568b50b739ef8b8fadba14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959811"
---
# <span data-ttu-id="735b9-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="735b9-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="735b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="735b9-102">SYNOPSIS</span></span>
<span data-ttu-id="735b9-103">Остановка пакетной задачи.</span><span class="sxs-lookup"><span data-stu-id="735b9-103">Stops a Batch task.</span></span>

## <span data-ttu-id="735b9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="735b9-104">SYNTAX</span></span>

### <span data-ttu-id="735b9-105">ИД</span><span class="sxs-lookup"><span data-stu-id="735b9-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="735b9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="735b9-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="735b9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="735b9-107">DESCRIPTION</span></span>
<span data-ttu-id="735b9-108">Из-за нее можно прекратить обработку пакетной задачи Azure с использованием **cmdlet Stop-AzBatchTask.**</span><span class="sxs-lookup"><span data-stu-id="735b9-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="735b9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="735b9-109">EXAMPLES</span></span>

### <span data-ttu-id="735b9-110">Пример 1. Удаление пакетной задачи по ИД</span><span class="sxs-lookup"><span data-stu-id="735b9-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="735b9-111">Эта команда останавливает задачу с ИД задачи23 для задания с заданием 0000001.</span><span class="sxs-lookup"><span data-stu-id="735b9-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="735b9-112">Команда запросит подтверждение.</span><span class="sxs-lookup"><span data-stu-id="735b9-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="735b9-113">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="735b9-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="735b9-114">Пример 2. Остановка пакетной задачи с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="735b9-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="735b9-115">Эта команда получает задачу с пакетной задачей, которая имеет задачу "Код26" в задаче, для работы с ИД-000001, с помощью Get-AzBatchTask командлета.</span><span class="sxs-lookup"><span data-stu-id="735b9-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="735b9-116">Эта команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="735b9-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="735b9-117">Эта команда останавливает задачу.</span><span class="sxs-lookup"><span data-stu-id="735b9-117">The command stops that task.</span></span>

## <span data-ttu-id="735b9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="735b9-118">PARAMETERS</span></span>

### <span data-ttu-id="735b9-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="735b9-119">-BatchContext</span></span>
<span data-ttu-id="735b9-120">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="735b9-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="735b9-121">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="735b9-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="735b9-122">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="735b9-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="735b9-123">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="735b9-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="735b9-124">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="735b9-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="735b9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735b9-125">-DefaultProfile</span></span>
<span data-ttu-id="735b9-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="735b9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="735b9-127">-Id</span><span class="sxs-lookup"><span data-stu-id="735b9-127">-Id</span></span>
<span data-ttu-id="735b9-128">Определяет код задачи, которую останавливает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="735b9-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="735b9-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="735b9-129">-JobId</span></span>
<span data-ttu-id="735b9-130">Определяет ИД задания, которое содержит задачу.</span><span class="sxs-lookup"><span data-stu-id="735b9-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="735b9-131">-Задача</span><span class="sxs-lookup"><span data-stu-id="735b9-131">-Task</span></span>
<span data-ttu-id="735b9-132">Указывает задачу, которую останавливает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="735b9-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="735b9-133">Чтобы получить объект **PSCloudTask,** используйте Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="735b9-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="735b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735b9-134">CommonParameters</span></span>
<span data-ttu-id="735b9-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="735b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735b9-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="735b9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735b9-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="735b9-137">INPUTS</span></span>

### <span data-ttu-id="735b9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="735b9-138">System.String</span></span>

### <span data-ttu-id="735b9-139">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="735b9-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="735b9-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="735b9-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="735b9-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="735b9-141">OUTPUTS</span></span>

### <span data-ttu-id="735b9-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="735b9-142">System.Void</span></span>

## <span data-ttu-id="735b9-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="735b9-143">NOTES</span></span>

## <span data-ttu-id="735b9-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="735b9-144">RELATED LINKS</span></span>

[<span data-ttu-id="735b9-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="735b9-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="735b9-146">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="735b9-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="735b9-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="735b9-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="735b9-148">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="735b9-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
