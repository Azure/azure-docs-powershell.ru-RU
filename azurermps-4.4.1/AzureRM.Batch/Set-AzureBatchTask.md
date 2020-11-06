---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: b572a7aefc3076671e78895f5fea531929858873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568332"
---
# <span data-ttu-id="40879-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="40879-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="40879-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40879-102">SYNOPSIS</span></span>
<span data-ttu-id="40879-103">Обновляет свойства задачи.</span><span class="sxs-lookup"><span data-stu-id="40879-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40879-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40879-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40879-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40879-105">DESCRIPTION</span></span>
<span data-ttu-id="40879-106">Командлет **Set-AzureBatchTask** обновляет свойства задачи в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="40879-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="40879-107">Используйте командлет Get-AzureBatchTask, чтобы получить объект **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="40879-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="40879-108">Измените свойства объекта, а затем используйте текущий командлет для фиксации изменений в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="40879-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="40879-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40879-109">EXAMPLES</span></span>

### <span data-ttu-id="40879-110">Пример 1: обновление задачи</span><span class="sxs-lookup"><span data-stu-id="40879-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="40879-111">Первая команда получает задачу с помощью **Get-AzureBatchTask** , а затем сохраняет ее в переменной $Task.</span><span class="sxs-lookup"><span data-stu-id="40879-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>

<span data-ttu-id="40879-112">Следующие две команды изменяют ограничения задачи в $Task.</span><span class="sxs-lookup"><span data-stu-id="40879-112">The next two commands modify the constraints of the task in $Task.</span></span>

<span data-ttu-id="40879-113">Последняя команда обновляет пакетную службу таким образом, чтобы она соответствовала локальному объекту в $Task.</span><span class="sxs-lookup"><span data-stu-id="40879-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="40879-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40879-114">PARAMETERS</span></span>

### <span data-ttu-id="40879-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="40879-115">-BatchContext</span></span>
<span data-ttu-id="40879-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="40879-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="40879-117">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="40879-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="40879-118">-Задача</span><span class="sxs-lookup"><span data-stu-id="40879-118">-Task</span></span>
<span data-ttu-id="40879-119">Указывает **PSCloudTask** , на который этот командлет обновляет службу пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="40879-119">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="40879-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40879-120">-DefaultProfile</span></span>
<span data-ttu-id="40879-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40879-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40879-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40879-122">CommonParameters</span></span>
<span data-ttu-id="40879-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40879-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40879-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40879-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40879-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40879-125">INPUTS</span></span>

### <span data-ttu-id="40879-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="40879-126">BatchAccountContext</span></span>
<span data-ttu-id="40879-127">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="40879-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="40879-128">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="40879-128">PSCloudTask</span></span>
<span data-ttu-id="40879-129">Параметр "задача" принимает значение типа "PSCloudTask" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="40879-129">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="40879-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40879-130">OUTPUTS</span></span>

## <span data-ttu-id="40879-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="40879-131">NOTES</span></span>

## <span data-ttu-id="40879-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40879-132">RELATED LINKS</span></span>

[<span data-ttu-id="40879-133">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="40879-133">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="40879-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="40879-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="40879-135">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="40879-135">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="40879-136">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="40879-136">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="40879-137">Остановить-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="40879-137">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="40879-138">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="40879-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


