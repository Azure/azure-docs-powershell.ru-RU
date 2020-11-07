---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: bae5f2b075f8d4f2fa579b38bdccf160cd46caad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732122"
---
# <span data-ttu-id="23712-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="23712-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="23712-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23712-102">SYNOPSIS</span></span>
<span data-ttu-id="23712-103">Обновляет свойства задачи.</span><span class="sxs-lookup"><span data-stu-id="23712-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23712-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23712-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23712-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23712-105">DESCRIPTION</span></span>
<span data-ttu-id="23712-106">Командлет **Set-AzureBatchTask** обновляет свойства задачи в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="23712-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="23712-107">Используйте командлет Get-AzureBatchTask, чтобы получить объект **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="23712-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="23712-108">Измените свойства объекта, а затем используйте текущий командлет для фиксации изменений в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="23712-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="23712-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23712-109">EXAMPLES</span></span>

### <span data-ttu-id="23712-110">Пример 1: обновление задачи</span><span class="sxs-lookup"><span data-stu-id="23712-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="23712-111">Первая команда получает задачу с помощью **Get-AzureBatchTask** , а затем сохраняет ее в переменной $Task.</span><span class="sxs-lookup"><span data-stu-id="23712-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="23712-112">Следующие две команды изменяют ограничения задачи в $Task.</span><span class="sxs-lookup"><span data-stu-id="23712-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="23712-113">Последняя команда обновляет пакетную службу таким образом, чтобы она соответствовала локальному объекту в $Task.</span><span class="sxs-lookup"><span data-stu-id="23712-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="23712-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23712-114">PARAMETERS</span></span>

### <span data-ttu-id="23712-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="23712-115">-BatchContext</span></span>
<span data-ttu-id="23712-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="23712-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="23712-117">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="23712-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="23712-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="23712-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="23712-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="23712-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="23712-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="23712-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="23712-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23712-121">-DefaultProfile</span></span>
<span data-ttu-id="23712-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23712-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23712-123">-Задача</span><span class="sxs-lookup"><span data-stu-id="23712-123">-Task</span></span>
<span data-ttu-id="23712-124">Указывает **PSCloudTask** , на который этот командлет обновляет службу пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="23712-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="23712-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23712-125">CommonParameters</span></span>
<span data-ttu-id="23712-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23712-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23712-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23712-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23712-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23712-128">INPUTS</span></span>

### <span data-ttu-id="23712-129">Microsoft.Azure.Commands.BatCH. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="23712-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="23712-130">Параметры: Task (ByValue)</span><span class="sxs-lookup"><span data-stu-id="23712-130">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="23712-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="23712-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="23712-132">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="23712-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="23712-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23712-133">OUTPUTS</span></span>

### <span data-ttu-id="23712-134">System. void</span><span class="sxs-lookup"><span data-stu-id="23712-134">System.Void</span></span>

## <span data-ttu-id="23712-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="23712-135">NOTES</span></span>

## <span data-ttu-id="23712-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23712-136">RELATED LINKS</span></span>

[<span data-ttu-id="23712-137">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="23712-137">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="23712-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="23712-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="23712-139">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="23712-139">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="23712-140">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="23712-140">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="23712-141">Остановить-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="23712-141">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="23712-142">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="23712-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


