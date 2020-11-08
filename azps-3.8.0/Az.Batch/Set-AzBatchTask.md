---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 80cfa0453bf521ee8b29fb6a330ec194ada84383
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077244"
---
# <span data-ttu-id="88075-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88075-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="88075-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88075-102">SYNOPSIS</span></span>
<span data-ttu-id="88075-103">Обновляет свойства задачи.</span><span class="sxs-lookup"><span data-stu-id="88075-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="88075-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88075-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88075-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88075-105">DESCRIPTION</span></span>
<span data-ttu-id="88075-106">Командлет **Set-AzBatchTask** обновляет свойства задачи в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="88075-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="88075-107">Используйте командлет Get-AzBatchTask, чтобы получить объект **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="88075-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="88075-108">Измените свойства объекта, а затем используйте текущий командлет для фиксации изменений в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="88075-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="88075-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88075-109">EXAMPLES</span></span>

### <span data-ttu-id="88075-110">Пример 1: обновление задачи</span><span class="sxs-lookup"><span data-stu-id="88075-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="88075-111">Первая команда получает задачу с помощью **Get-AzBatchTask** , а затем сохраняет ее в переменной $Task.</span><span class="sxs-lookup"><span data-stu-id="88075-111">The first command gets a task by using **Get-AzBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="88075-112">Следующие две команды изменяют ограничения задачи в $Task.</span><span class="sxs-lookup"><span data-stu-id="88075-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="88075-113">Последняя команда обновляет пакетную службу таким образом, чтобы она соответствовала локальному объекту в $Task.</span><span class="sxs-lookup"><span data-stu-id="88075-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="88075-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88075-114">PARAMETERS</span></span>

### <span data-ttu-id="88075-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="88075-115">-BatchContext</span></span>
<span data-ttu-id="88075-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="88075-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="88075-117">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="88075-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="88075-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="88075-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="88075-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="88075-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="88075-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="88075-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="88075-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88075-121">-DefaultProfile</span></span>
<span data-ttu-id="88075-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88075-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88075-123">-Задача</span><span class="sxs-lookup"><span data-stu-id="88075-123">-Task</span></span>
<span data-ttu-id="88075-124">Указывает **PSCloudTask** , на который этот командлет обновляет службу пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="88075-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88075-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88075-125">CommonParameters</span></span>
<span data-ttu-id="88075-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88075-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88075-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88075-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88075-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88075-128">INPUTS</span></span>

### <span data-ttu-id="88075-129">Microsoft.Azure.Commands.BatCH. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="88075-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="88075-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="88075-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="88075-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88075-131">OUTPUTS</span></span>

### <span data-ttu-id="88075-132">System. void</span><span class="sxs-lookup"><span data-stu-id="88075-132">System.Void</span></span>

## <span data-ttu-id="88075-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="88075-133">NOTES</span></span>

## <span data-ttu-id="88075-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88075-134">RELATED LINKS</span></span>

[<span data-ttu-id="88075-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88075-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="88075-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="88075-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="88075-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88075-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="88075-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88075-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="88075-139">Остановить-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88075-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="88075-140">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="88075-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


