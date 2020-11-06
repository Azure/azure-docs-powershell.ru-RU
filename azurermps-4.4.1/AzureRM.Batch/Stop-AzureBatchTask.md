---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: ac63bbdb95551ff5ff08661a92f0924d5853ade5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566752"
---
# <span data-ttu-id="e823d-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="e823d-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="e823d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e823d-102">SYNOPSIS</span></span>
<span data-ttu-id="e823d-103">Останавливает пакетную задачу.</span><span class="sxs-lookup"><span data-stu-id="e823d-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e823d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e823d-104">SYNTAX</span></span>

### <span data-ttu-id="e823d-105">Номер</span><span class="sxs-lookup"><span data-stu-id="e823d-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e823d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e823d-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e823d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e823d-107">DESCRIPTION</span></span>
<span data-ttu-id="e823d-108">Командлет **Stop-AzureBatchTask** останавливает пакетную задачу Azure.</span><span class="sxs-lookup"><span data-stu-id="e823d-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="e823d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e823d-109">EXAMPLES</span></span>

### <span data-ttu-id="e823d-110">Пример 1: удаление пакетной задачи по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="e823d-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="e823d-111">Эта команда останавливает задачу с ИДЕНТИФИКАТОРом Task23 в задаче с ИД задания 000001.</span><span class="sxs-lookup"><span data-stu-id="e823d-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e823d-112">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e823d-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="e823d-113">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="e823d-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="e823d-114">Пример 2: остановка пакетной задачи с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="e823d-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="e823d-115">Эта команда возвращает пакетную задачу с ИДЕНТИФИКАТОРом Task26 в задании с ИД задания 000001 с помощью командлета Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="e823d-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="e823d-116">Команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="e823d-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e823d-117">Команда останавливает эту задачу.</span><span class="sxs-lookup"><span data-stu-id="e823d-117">The command stops that task.</span></span>

## <span data-ttu-id="e823d-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e823d-118">PARAMETERS</span></span>

### <span data-ttu-id="e823d-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e823d-119">-BatchContext</span></span>
<span data-ttu-id="e823d-120">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="e823d-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e823d-121">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="e823d-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="e823d-122">-ID</span><span class="sxs-lookup"><span data-stu-id="e823d-122">-Id</span></span>
<span data-ttu-id="e823d-123">Указывает идентификатор задачи, которую завершает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e823d-123">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e823d-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="e823d-124">-JobId</span></span>
<span data-ttu-id="e823d-125">Указывает идентификатор задания, содержащего задачу.</span><span class="sxs-lookup"><span data-stu-id="e823d-125">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e823d-126">-Задача</span><span class="sxs-lookup"><span data-stu-id="e823d-126">-Task</span></span>
<span data-ttu-id="e823d-127">Указывает задачу, которую завершает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e823d-127">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="e823d-128">Чтобы получить объект **PSCloudTask** , используйте командлет Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="e823d-128">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e823d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e823d-129">-DefaultProfile</span></span>
<span data-ttu-id="e823d-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e823d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e823d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e823d-131">CommonParameters</span></span>
<span data-ttu-id="e823d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e823d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e823d-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e823d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e823d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e823d-134">INPUTS</span></span>

### <span data-ttu-id="e823d-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e823d-135">BatchAccountContext</span></span>
<span data-ttu-id="e823d-136">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e823d-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="e823d-137">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="e823d-137">PSCloudTask</span></span>
<span data-ttu-id="e823d-138">Параметр "задача" принимает значение типа "PSCloudTask" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e823d-138">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="e823d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e823d-139">OUTPUTS</span></span>

## <span data-ttu-id="e823d-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="e823d-140">NOTES</span></span>

## <span data-ttu-id="e823d-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e823d-141">RELATED LINKS</span></span>

[<span data-ttu-id="e823d-142">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="e823d-142">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="e823d-143">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="e823d-143">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="e823d-144">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="e823d-144">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="e823d-145">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="e823d-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


