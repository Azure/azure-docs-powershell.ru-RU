---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: e3cd26859578c63cf5b74d41642cc26a22451858
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077253"
---
# <span data-ttu-id="5a599-101">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5a599-101">New-AzBatchJobSchedule</span></span>

## <span data-ttu-id="5a599-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a599-102">SYNOPSIS</span></span>
<span data-ttu-id="5a599-103">Создание расписания заданий в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="5a599-103">Creates a job schedule in the Batch service.</span></span>

## <span data-ttu-id="5a599-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a599-104">SYNTAX</span></span>

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a599-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a599-105">DESCRIPTION</span></span>
<span data-ttu-id="5a599-106">Командлет **New-AzBatchJobSchedule** создает расписание задач в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="5a599-106">The **New-AzBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="5a599-107">Параметр *BatchAccountContext* указывает учетную запись, в которой этот командлет создает расписание.</span><span class="sxs-lookup"><span data-stu-id="5a599-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="5a599-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a599-108">EXAMPLES</span></span>

### <span data-ttu-id="5a599-109">Пример 1: Создание расписания задания</span><span class="sxs-lookup"><span data-stu-id="5a599-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="5a599-110">В этом примере создается расписание задания.</span><span class="sxs-lookup"><span data-stu-id="5a599-110">This example creates a job schedule.</span></span>
<span data-ttu-id="5a599-111">Первые пять команд создают и изменяют объекты **PSSchedule** , **PSJobSpecification** и **PSPoolInformation** .</span><span class="sxs-lookup"><span data-stu-id="5a599-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="5a599-112">Команды используют командлеты New-Object и стандартный синтаксис PowerShell для Azure.</span><span class="sxs-lookup"><span data-stu-id="5a599-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="5a599-113">Команды хранят эти объекты в переменных $Schedule и $JobSpecification.</span><span class="sxs-lookup"><span data-stu-id="5a599-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="5a599-114">В последней команде создается расписание заданий с ИДЕНТИФИКАТОРом JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="5a599-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="5a599-115">В этом расписании создаются задания с интервалом повторения в один день.</span><span class="sxs-lookup"><span data-stu-id="5a599-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="5a599-116">Задания выполняются в пуле с ИД ContosoPool06, как указано в пятом команде.</span><span class="sxs-lookup"><span data-stu-id="5a599-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="5a599-117">Используйте командлет **Get-AzBatchAccountKey** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="5a599-117">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5a599-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a599-118">PARAMETERS</span></span>

### <span data-ttu-id="5a599-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5a599-119">-BatchContext</span></span>
<span data-ttu-id="5a599-120">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="5a599-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5a599-121">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="5a599-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5a599-122">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="5a599-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5a599-123">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="5a599-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5a599-124">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5a599-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5a599-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a599-125">-DefaultProfile</span></span>
<span data-ttu-id="5a599-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a599-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a599-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5a599-127">-DisplayName</span></span>
<span data-ttu-id="5a599-128">Задает отображаемое имя расписания задания.</span><span class="sxs-lookup"><span data-stu-id="5a599-128">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="5a599-129">-ID</span><span class="sxs-lookup"><span data-stu-id="5a599-129">-Id</span></span>
<span data-ttu-id="5a599-130">Указывает идентификатор расписания задания, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5a599-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5a599-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="5a599-131">-JobSpecification</span></span>
<span data-ttu-id="5a599-132">Задает сведения о заданиях, которые включает этот командлет в расписание задания.</span><span class="sxs-lookup"><span data-stu-id="5a599-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="5a599-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5a599-133">-Metadata</span></span>
<span data-ttu-id="5a599-134">Задает метаданные в виде пар "ключ-значение", которые нужно добавить в расписание задания.</span><span class="sxs-lookup"><span data-stu-id="5a599-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="5a599-135">Ключом является имя метаданных.</span><span class="sxs-lookup"><span data-stu-id="5a599-135">The key is the metadata name.</span></span>
<span data-ttu-id="5a599-136">Значением является значение метаданных.</span><span class="sxs-lookup"><span data-stu-id="5a599-136">The value is the metadata value.</span></span>

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

### <span data-ttu-id="5a599-137">-Планирование</span><span class="sxs-lookup"><span data-stu-id="5a599-137">-Schedule</span></span>
<span data-ttu-id="5a599-138">Указывает расписание, определяющее время создания заданий.</span><span class="sxs-lookup"><span data-stu-id="5a599-138">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="5a599-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a599-139">CommonParameters</span></span>
<span data-ttu-id="5a599-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a599-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a599-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a599-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a599-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a599-142">INPUTS</span></span>

### <span data-ttu-id="5a599-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5a599-143">System.String</span></span>

### <span data-ttu-id="5a599-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5a599-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5a599-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a599-145">OUTPUTS</span></span>

### <span data-ttu-id="5a599-146">System. void</span><span class="sxs-lookup"><span data-stu-id="5a599-146">System.Void</span></span>

## <span data-ttu-id="5a599-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a599-147">NOTES</span></span>

## <span data-ttu-id="5a599-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a599-148">RELATED LINKS</span></span>

[<span data-ttu-id="5a599-149">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5a599-149">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="5a599-150">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5a599-150">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="5a599-151">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5a599-151">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5a599-152">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5a599-152">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="5a599-153">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5a599-153">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="5a599-154">Остановить-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5a599-154">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="5a599-155">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="5a599-155">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

