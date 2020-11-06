---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: a1841fb569cf6ef29bad685679372e0385133568
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569996"
---
# <span data-ttu-id="0a0c2-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0a0c2-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="0a0c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0c2-103">Создание расписания заданий в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a0c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a0c2-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a0c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a0c2-105">DESCRIPTION</span></span>
<span data-ttu-id="0a0c2-106">Командлет **New-AzureBatchJobSchedule** создает расписание задач в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="0a0c2-107">Параметр *BatchAccountContext* указывает учетную запись, в которой этот командлет создает расписание.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="0a0c2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a0c2-108">EXAMPLES</span></span>

### <span data-ttu-id="0a0c2-109">Пример 1: Создание расписания задания</span><span class="sxs-lookup"><span data-stu-id="0a0c2-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="0a0c2-110">В этом примере создается расписание задания.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-110">This example creates a job schedule.</span></span>

<span data-ttu-id="0a0c2-111">Первые пять команд создают и изменяют объекты **PSSchedule** , **PSJobSpecification** и **PSPoolInformation** .</span><span class="sxs-lookup"><span data-stu-id="0a0c2-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="0a0c2-112">Команды используют командлеты New-Object и стандартный синтаксис PowerShell для Azure.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="0a0c2-113">Команды хранят эти объекты в переменных $Schedule и $JobSpecification.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>

<span data-ttu-id="0a0c2-114">В последней команде создается расписание заданий с ИДЕНТИФИКАТОРом JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="0a0c2-115">В этом расписании создаются задания с интервалом повторения в один день.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="0a0c2-116">Задания выполняются в пуле с ИД ContosoPool06, как указано в пятом команде.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="0a0c2-117">Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="0a0c2-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a0c2-118">PARAMETERS</span></span>

### <span data-ttu-id="0a0c2-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0a0c2-119">-BatchContext</span></span>
<span data-ttu-id="0a0c2-120">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0a0c2-121">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0a0c2-122">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0a0c2-123">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0a0c2-124">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0a0c2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0c2-125">-DefaultProfile</span></span>
<span data-ttu-id="0a0c2-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a0c2-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0a0c2-127">-DisplayName</span></span>
<span data-ttu-id="0a0c2-128">Задает отображаемое имя расписания задания.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-128">Specifies a display name for the job schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a0c2-129">-ID</span><span class="sxs-lookup"><span data-stu-id="0a0c2-129">-Id</span></span>
<span data-ttu-id="0a0c2-130">Указывает идентификатор расписания задания, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a0c2-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="0a0c2-131">-JobSpecification</span></span>
<span data-ttu-id="0a0c2-132">Задает сведения о заданиях, которые включает этот командлет в расписание задания.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: PSJobSpecification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a0c2-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0a0c2-133">-Metadata</span></span>
<span data-ttu-id="0a0c2-134">Задает метаданные в виде пар "ключ-значение", которые нужно добавить в расписание задания.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="0a0c2-135">Ключом является имя метаданных.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-135">The key is the metadata name.</span></span>
<span data-ttu-id="0a0c2-136">Значением является значение метаданных.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-136">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a0c2-137">-Планирование</span><span class="sxs-lookup"><span data-stu-id="0a0c2-137">-Schedule</span></span>
<span data-ttu-id="0a0c2-138">Указывает расписание, определяющее время создания заданий.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-138">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: PSSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a0c2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0c2-139">CommonParameters</span></span>
<span data-ttu-id="0a0c2-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0c2-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a0c2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0c2-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a0c2-142">INPUTS</span></span>

### <span data-ttu-id="0a0c2-143">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0a0c2-143">BatchAccountContext</span></span>
<span data-ttu-id="0a0c2-144">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0a0c2-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="0a0c2-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a0c2-145">OUTPUTS</span></span>

## <span data-ttu-id="0a0c2-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a0c2-146">NOTES</span></span>

## <span data-ttu-id="0a0c2-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a0c2-147">RELATED LINKS</span></span>

[<span data-ttu-id="0a0c2-148">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0a0c2-148">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="0a0c2-149">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0a0c2-149">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="0a0c2-150">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0a0c2-150">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0a0c2-151">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0a0c2-151">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="0a0c2-152">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0a0c2-152">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="0a0c2-153">Остановить-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0a0c2-153">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="0a0c2-154">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="0a0c2-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


