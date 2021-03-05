---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: cf4512bc0d219c164be6543d5633a43c9052cc4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004616"
---
# <span data-ttu-id="d1a52-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d1a52-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="d1a52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1a52-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a52-103">Задает расписание задания.</span><span class="sxs-lookup"><span data-stu-id="d1a52-103">Sets a job schedule.</span></span>

## <span data-ttu-id="d1a52-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d1a52-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1a52-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1a52-105">DESCRIPTION</span></span>
<span data-ttu-id="d1a52-106">**Cmdlet Set-AzBatchJobSchedule** задает расписание задания в службе Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="d1a52-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="d1a52-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d1a52-107">EXAMPLES</span></span>

### <span data-ttu-id="d1a52-108">Пример 1. Обновление расписания работы</span><span class="sxs-lookup"><span data-stu-id="d1a52-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="d1a52-109">Первая команда получает задание с помощью **Get-AzBatchJobSchedule,** а затем сохраняет его в $JobSchedule переменной.</span><span class="sxs-lookup"><span data-stu-id="d1a52-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="d1a52-110">Вторая команда изменяет интервал повторения для `$JobSchedule.Schedule` объекта.</span><span class="sxs-lookup"><span data-stu-id="d1a52-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="d1a52-111">Конечная команда обновляет пакетную службу в соответствие с локальным объектом в $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="d1a52-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="d1a52-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1a52-112">PARAMETERS</span></span>

### <span data-ttu-id="d1a52-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d1a52-113">-BatchContext</span></span>
<span data-ttu-id="d1a52-114">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="d1a52-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d1a52-115">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d1a52-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d1a52-116">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="d1a52-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d1a52-117">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d1a52-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d1a52-118">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d1a52-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d1a52-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a52-119">-DefaultProfile</span></span>
<span data-ttu-id="d1a52-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a52-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1a52-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="d1a52-121">-JobSchedule</span></span>
<span data-ttu-id="d1a52-122">Указывает объект **PSCloudJobSchedule,** который представляет расписание задания.</span><span class="sxs-lookup"><span data-stu-id="d1a52-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="d1a52-123">Чтобы получить объект **PSCloudJobSchedule,** воспользуйтесь Get-AzBatchJobSchedule..</span><span class="sxs-lookup"><span data-stu-id="d1a52-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="d1a52-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a52-124">CommonParameters</span></span>
<span data-ttu-id="d1a52-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a52-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a52-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1a52-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a52-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1a52-127">INPUTS</span></span>

### <span data-ttu-id="d1a52-128">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d1a52-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="d1a52-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d1a52-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d1a52-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d1a52-130">OUTPUTS</span></span>

### <span data-ttu-id="d1a52-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="d1a52-131">System.Void</span></span>

## <span data-ttu-id="d1a52-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d1a52-132">NOTES</span></span>

## <span data-ttu-id="d1a52-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1a52-133">RELATED LINKS</span></span>

[<span data-ttu-id="d1a52-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d1a52-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="d1a52-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d1a52-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="d1a52-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d1a52-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="d1a52-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d1a52-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="d1a52-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d1a52-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="d1a52-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d1a52-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


