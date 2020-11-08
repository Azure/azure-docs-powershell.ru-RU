---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: d6a17588b5718f9a6d735521a7a136cba472ead0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249564"
---
# <span data-ttu-id="e7db3-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7db3-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="e7db3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7db3-102">SYNOPSIS</span></span>
<span data-ttu-id="e7db3-103">Задает расписание задания.</span><span class="sxs-lookup"><span data-stu-id="e7db3-103">Sets a job schedule.</span></span>

## <span data-ttu-id="e7db3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7db3-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7db3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7db3-105">DESCRIPTION</span></span>
<span data-ttu-id="e7db3-106">Командлет **Set-AzBatchJobSchedule** задает расписание заданий в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="e7db3-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="e7db3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7db3-107">EXAMPLES</span></span>

### <span data-ttu-id="e7db3-108">Пример 1: Обновление расписания задания</span><span class="sxs-lookup"><span data-stu-id="e7db3-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="e7db3-109">Первая команда получает задание с помощью **Get-AzBatchJobSchedule** , а затем сохраняет его в переменной $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="e7db3-109">The first command gets a job by using **Get-AzBatchJobSchedule** , and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="e7db3-110">Вторая команда изменяет интервал повторения для `$JobSchedule.Schedule` объекта.</span><span class="sxs-lookup"><span data-stu-id="e7db3-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="e7db3-111">Последняя команда обновляет пакетную службу таким образом, чтобы она соответствовала локальному объекту в $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="e7db3-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="e7db3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7db3-112">PARAMETERS</span></span>

### <span data-ttu-id="e7db3-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e7db3-113">-BatchContext</span></span>
<span data-ttu-id="e7db3-114">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="e7db3-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e7db3-115">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="e7db3-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e7db3-116">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="e7db3-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e7db3-117">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="e7db3-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e7db3-118">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e7db3-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e7db3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7db3-119">-DefaultProfile</span></span>
<span data-ttu-id="e7db3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7db3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7db3-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7db3-121">-JobSchedule</span></span>
<span data-ttu-id="e7db3-122">Указывает объект **PSCloudJobSchedule** , который представляет расписание задания.</span><span class="sxs-lookup"><span data-stu-id="e7db3-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="e7db3-123">Чтобы получить объект **PSCloudJobSchedule** , используйте командлет Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="e7db3-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7db3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7db3-124">CommonParameters</span></span>
<span data-ttu-id="e7db3-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7db3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7db3-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7db3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7db3-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7db3-127">INPUTS</span></span>

### <span data-ttu-id="e7db3-128">Microsoft.Azure.Commands.BatCH. Models. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7db3-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="e7db3-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e7db3-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e7db3-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7db3-130">OUTPUTS</span></span>

### <span data-ttu-id="e7db3-131">System. void</span><span class="sxs-lookup"><span data-stu-id="e7db3-131">System.Void</span></span>

## <span data-ttu-id="e7db3-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7db3-132">NOTES</span></span>

## <span data-ttu-id="e7db3-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7db3-133">RELATED LINKS</span></span>

[<span data-ttu-id="e7db3-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7db3-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="e7db3-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7db3-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="e7db3-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7db3-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="e7db3-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7db3-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="e7db3-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7db3-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="e7db3-139">Остановить-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7db3-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


