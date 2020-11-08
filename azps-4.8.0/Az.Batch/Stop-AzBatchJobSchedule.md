---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: b236f163a6c5c849fcbfcea0a19dac955e15c798
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079163"
---
# <span data-ttu-id="e7051-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7051-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="e7051-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7051-102">SYNOPSIS</span></span>
<span data-ttu-id="e7051-103">Остановка пакетного задания в расписании.</span><span class="sxs-lookup"><span data-stu-id="e7051-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="e7051-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7051-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7051-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7051-105">DESCRIPTION</span></span>
<span data-ttu-id="e7051-106">Командлет **Stop-AzBatchJobSchedule** прекращает выполнение пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="e7051-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="e7051-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7051-107">EXAMPLES</span></span>

### <span data-ttu-id="e7051-108">Пример 1: остановка расписания задания</span><span class="sxs-lookup"><span data-stu-id="e7051-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="e7051-109">Эта команда останавливает расписание задач с ИДЕНТИФИКАТОРом JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="e7051-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="e7051-110">Используйте командлет Get-AzBatchAccountKey для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="e7051-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e7051-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7051-111">PARAMETERS</span></span>

### <span data-ttu-id="e7051-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e7051-112">-BatchContext</span></span>
<span data-ttu-id="e7051-113">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="e7051-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e7051-114">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="e7051-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e7051-115">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="e7051-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e7051-116">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="e7051-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e7051-117">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e7051-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e7051-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7051-118">-DefaultProfile</span></span>
<span data-ttu-id="e7051-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7051-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7051-120">-ID</span><span class="sxs-lookup"><span data-stu-id="e7051-120">-Id</span></span>
<span data-ttu-id="e7051-121">Указывает идентификатор расписания задания, которое останавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e7051-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="e7051-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7051-122">CommonParameters</span></span>
<span data-ttu-id="e7051-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7051-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7051-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7051-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7051-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7051-125">INPUTS</span></span>

### <span data-ttu-id="e7051-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e7051-126">System.String</span></span>

### <span data-ttu-id="e7051-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e7051-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e7051-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7051-128">OUTPUTS</span></span>

### <span data-ttu-id="e7051-129">System. void</span><span class="sxs-lookup"><span data-stu-id="e7051-129">System.Void</span></span>

## <span data-ttu-id="e7051-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7051-130">NOTES</span></span>

## <span data-ttu-id="e7051-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7051-131">RELATED LINKS</span></span>

[<span data-ttu-id="e7051-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7051-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="e7051-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7051-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="e7051-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e7051-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e7051-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7051-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="e7051-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7051-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="e7051-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7051-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="e7051-138">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="e7051-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)