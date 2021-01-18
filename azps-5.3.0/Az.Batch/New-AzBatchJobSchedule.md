---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: ab1293bf147424bb9a7315cb541b9bf22fe4a357
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509637"
---
# <span data-ttu-id="f1c07-101">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f1c07-101">New-AzBatchJobSchedule</span></span>

## <span data-ttu-id="f1c07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1c07-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c07-103">Создает расписание задания в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="f1c07-103">Creates a job schedule in the Batch service.</span></span>

## <span data-ttu-id="f1c07-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1c07-104">SYNTAX</span></span>

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1c07-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1c07-105">DESCRIPTION</span></span>
<span data-ttu-id="f1c07-106">Для создания расписания рабочих мест в службе Azure Batch создается календарный план **New-AzBatchJobSchedule.**</span><span class="sxs-lookup"><span data-stu-id="f1c07-106">The **New-AzBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="f1c07-107">Параметр *BatchAccountContext* определяет учетную запись, в которой этот cmdlet создает расписание.</span><span class="sxs-lookup"><span data-stu-id="f1c07-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="f1c07-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1c07-108">EXAMPLES</span></span>

### <span data-ttu-id="f1c07-109">Пример 1. Создание расписания работы</span><span class="sxs-lookup"><span data-stu-id="f1c07-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="f1c07-110">В этом примере создается расписание работы.</span><span class="sxs-lookup"><span data-stu-id="f1c07-110">This example creates a job schedule.</span></span>
<span data-ttu-id="f1c07-111">Первые пять команд создают и изменяют объекты **PSSchedule,** **PSJobSpecification** и **PSPoolInformation.**</span><span class="sxs-lookup"><span data-stu-id="f1c07-111">The first five commands create and modify **PSSchedule**, **PSJobSpecification**, and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="f1c07-112">Для команд используются командлет New-Object и стандартный синтаксис Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f1c07-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="f1c07-113">Эти объекты хранятся в $Schedule и $JobSpecification переменных.</span><span class="sxs-lookup"><span data-stu-id="f1c07-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="f1c07-114">Конечная команда создает расписание задания с расписанием задания ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="f1c07-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="f1c07-115">В этом расписании создаются задания с интервалом повторения один день.</span><span class="sxs-lookup"><span data-stu-id="f1c07-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="f1c07-116">Задания запускаются в пуле с ИД ContosoPool06, как указано в пятой команде.</span><span class="sxs-lookup"><span data-stu-id="f1c07-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="f1c07-117">Чтобы назначить контекст переменной $Context, используйте $Context **AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="f1c07-117">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f1c07-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1c07-118">PARAMETERS</span></span>

### <span data-ttu-id="f1c07-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f1c07-119">-BatchContext</span></span>
<span data-ttu-id="f1c07-120">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="f1c07-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f1c07-121">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f1c07-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f1c07-122">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="f1c07-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f1c07-123">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f1c07-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f1c07-124">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f1c07-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f1c07-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c07-125">-DefaultProfile</span></span>
<span data-ttu-id="f1c07-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1c07-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1c07-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f1c07-127">-DisplayName</span></span>
<span data-ttu-id="f1c07-128">Отображает имя для расписания работы.</span><span class="sxs-lookup"><span data-stu-id="f1c07-128">Specifies a display name for the job schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c07-129">-Id</span><span class="sxs-lookup"><span data-stu-id="f1c07-129">-Id</span></span>
<span data-ttu-id="f1c07-130">Определяет код расписания задания, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1c07-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c07-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="f1c07-131">-JobSpecification</span></span>
<span data-ttu-id="f1c07-132">Определяет сведения о заданиях, которые этот cmdlet включает в расписание заданий.</span><span class="sxs-lookup"><span data-stu-id="f1c07-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c07-133">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="f1c07-133">-Metadata</span></span>
<span data-ttu-id="f1c07-134">Метаданные в качестве пар ключа и значения, которые нужно добавить в расписание задания.</span><span class="sxs-lookup"><span data-stu-id="f1c07-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="f1c07-135">Ключ — это имя метаданных.</span><span class="sxs-lookup"><span data-stu-id="f1c07-135">The key is the metadata name.</span></span>
<span data-ttu-id="f1c07-136">Значение — это значение метаданных.</span><span class="sxs-lookup"><span data-stu-id="f1c07-136">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c07-137">-Расписание</span><span class="sxs-lookup"><span data-stu-id="f1c07-137">-Schedule</span></span>
<span data-ttu-id="f1c07-138">Определяет расписание, которое определяет, когда создавать задания.</span><span class="sxs-lookup"><span data-stu-id="f1c07-138">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c07-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c07-139">CommonParameters</span></span>
<span data-ttu-id="f1c07-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1c07-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c07-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1c07-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c07-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1c07-142">INPUTS</span></span>

### <span data-ttu-id="f1c07-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f1c07-143">System.String</span></span>

### <span data-ttu-id="f1c07-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f1c07-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f1c07-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1c07-145">OUTPUTS</span></span>

### <span data-ttu-id="f1c07-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="f1c07-146">System.Void</span></span>

## <span data-ttu-id="f1c07-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1c07-147">NOTES</span></span>

## <span data-ttu-id="f1c07-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1c07-148">RELATED LINKS</span></span>

[<span data-ttu-id="f1c07-149">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f1c07-149">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="f1c07-150">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f1c07-150">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="f1c07-151">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f1c07-151">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f1c07-152">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f1c07-152">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="f1c07-153">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f1c07-153">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="f1c07-154">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f1c07-154">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="f1c07-155">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="f1c07-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
