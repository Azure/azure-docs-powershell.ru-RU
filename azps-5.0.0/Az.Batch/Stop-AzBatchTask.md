---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 8b84028bc9da854b5aa749867a8759b71d9f7b63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317294"
---
# <span data-ttu-id="88be3-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88be3-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="88be3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88be3-102">SYNOPSIS</span></span>
<span data-ttu-id="88be3-103">Останавливает пакетную задачу.</span><span class="sxs-lookup"><span data-stu-id="88be3-103">Stops a Batch task.</span></span>

## <span data-ttu-id="88be3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88be3-104">SYNTAX</span></span>

### <span data-ttu-id="88be3-105">Номер</span><span class="sxs-lookup"><span data-stu-id="88be3-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88be3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="88be3-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88be3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88be3-107">DESCRIPTION</span></span>
<span data-ttu-id="88be3-108">Командлет **Stop-AzBatchTask** останавливает пакетную задачу Azure.</span><span class="sxs-lookup"><span data-stu-id="88be3-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="88be3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88be3-109">EXAMPLES</span></span>

### <span data-ttu-id="88be3-110">Пример 1: удаление пакетной задачи по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="88be3-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="88be3-111">Эта команда останавливает задачу с ИДЕНТИФИКАТОРом Task23 в задаче с ИД задания 000001.</span><span class="sxs-lookup"><span data-stu-id="88be3-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="88be3-112">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="88be3-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="88be3-113">Используйте командлет Get-AzBatchAccountKey для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="88be3-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="88be3-114">Пример 2: остановка пакетной задачи с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="88be3-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="88be3-115">Эта команда возвращает пакетную задачу с ИДЕНТИФИКАТОРом Task26 в задании с ИД задания 000001 с помощью командлета Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="88be3-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="88be3-116">Команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="88be3-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="88be3-117">Команда останавливает эту задачу.</span><span class="sxs-lookup"><span data-stu-id="88be3-117">The command stops that task.</span></span>

## <span data-ttu-id="88be3-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88be3-118">PARAMETERS</span></span>

### <span data-ttu-id="88be3-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="88be3-119">-BatchContext</span></span>
<span data-ttu-id="88be3-120">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="88be3-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="88be3-121">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="88be3-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="88be3-122">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="88be3-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="88be3-123">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="88be3-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="88be3-124">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="88be3-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="88be3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88be3-125">-DefaultProfile</span></span>
<span data-ttu-id="88be3-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88be3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88be3-127">-ID</span><span class="sxs-lookup"><span data-stu-id="88be3-127">-Id</span></span>
<span data-ttu-id="88be3-128">Указывает идентификатор задачи, которую завершает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="88be3-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="88be3-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="88be3-129">-JobId</span></span>
<span data-ttu-id="88be3-130">Указывает идентификатор задания, содержащего задачу.</span><span class="sxs-lookup"><span data-stu-id="88be3-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="88be3-131">-Задача</span><span class="sxs-lookup"><span data-stu-id="88be3-131">-Task</span></span>
<span data-ttu-id="88be3-132">Указывает задачу, которую завершает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="88be3-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="88be3-133">Чтобы получить объект **PSCloudTask** , используйте командлет Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="88be3-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="88be3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88be3-134">CommonParameters</span></span>
<span data-ttu-id="88be3-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88be3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88be3-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88be3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88be3-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88be3-137">INPUTS</span></span>

### <span data-ttu-id="88be3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="88be3-138">System.String</span></span>

### <span data-ttu-id="88be3-139">Microsoft.Azure.Commands.BatCH. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="88be3-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="88be3-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="88be3-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="88be3-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88be3-141">OUTPUTS</span></span>

### <span data-ttu-id="88be3-142">System. void</span><span class="sxs-lookup"><span data-stu-id="88be3-142">System.Void</span></span>

## <span data-ttu-id="88be3-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="88be3-143">NOTES</span></span>

## <span data-ttu-id="88be3-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88be3-144">RELATED LINKS</span></span>

[<span data-ttu-id="88be3-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88be3-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="88be3-146">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88be3-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="88be3-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="88be3-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="88be3-148">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="88be3-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
