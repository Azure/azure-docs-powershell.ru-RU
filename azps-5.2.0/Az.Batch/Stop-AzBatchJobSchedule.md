---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: b236f163a6c5c849fcbfcea0a19dac955e15c798
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409095"
---
# <span data-ttu-id="ab51f-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ab51f-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="ab51f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab51f-102">SYNOPSIS</span></span>
<span data-ttu-id="ab51f-103">Остановка графика пакетных задания.</span><span class="sxs-lookup"><span data-stu-id="ab51f-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="ab51f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ab51f-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab51f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab51f-105">DESCRIPTION</span></span>
<span data-ttu-id="ab51f-106">**Из-за нее календарь stop-AzBatchJobSchedule** останавливает расписание обработки пакетных рабочих мест Azure.</span><span class="sxs-lookup"><span data-stu-id="ab51f-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="ab51f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ab51f-107">EXAMPLES</span></span>

### <span data-ttu-id="ab51f-108">Пример 1. Остановка расписания работы</span><span class="sxs-lookup"><span data-stu-id="ab51f-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="ab51f-109">Эта команда останавливает расписание задания с расписанием задания ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="ab51f-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="ab51f-110">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="ab51f-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="ab51f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab51f-111">PARAMETERS</span></span>

### <span data-ttu-id="ab51f-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ab51f-112">-BatchContext</span></span>
<span data-ttu-id="ab51f-113">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="ab51f-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ab51f-114">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ab51f-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ab51f-115">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="ab51f-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ab51f-116">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab51f-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ab51f-117">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ab51f-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ab51f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab51f-118">-DefaultProfile</span></span>
<span data-ttu-id="ab51f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab51f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab51f-120">-Id</span><span class="sxs-lookup"><span data-stu-id="ab51f-120">-Id</span></span>
<span data-ttu-id="ab51f-121">Определяет код расписания задания, который останавливает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab51f-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="ab51f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab51f-122">CommonParameters</span></span>
<span data-ttu-id="ab51f-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab51f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab51f-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab51f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab51f-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab51f-125">INPUTS</span></span>

### <span data-ttu-id="ab51f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ab51f-126">System.String</span></span>

### <span data-ttu-id="ab51f-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ab51f-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ab51f-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ab51f-128">OUTPUTS</span></span>

### <span data-ttu-id="ab51f-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="ab51f-129">System.Void</span></span>

## <span data-ttu-id="ab51f-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ab51f-130">NOTES</span></span>

## <span data-ttu-id="ab51f-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab51f-131">RELATED LINKS</span></span>

[<span data-ttu-id="ab51f-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ab51f-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="ab51f-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ab51f-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="ab51f-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ab51f-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ab51f-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ab51f-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="ab51f-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ab51f-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="ab51f-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ab51f-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="ab51f-138">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="ab51f-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
