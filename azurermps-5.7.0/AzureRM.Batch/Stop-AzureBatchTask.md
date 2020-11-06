---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: 979c136f1bdbd216cebe367060ebdc5d8360ea24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559291"
---
# <span data-ttu-id="c5bed-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c5bed-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="c5bed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5bed-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bed-103">Останавливает пакетную задачу.</span><span class="sxs-lookup"><span data-stu-id="c5bed-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5bed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5bed-104">SYNTAX</span></span>

### <span data-ttu-id="c5bed-105">Номер</span><span class="sxs-lookup"><span data-stu-id="c5bed-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5bed-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c5bed-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5bed-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5bed-107">DESCRIPTION</span></span>
<span data-ttu-id="c5bed-108">Командлет **Stop-AzureBatchTask** останавливает пакетную задачу Azure.</span><span class="sxs-lookup"><span data-stu-id="c5bed-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="c5bed-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5bed-109">EXAMPLES</span></span>

### <span data-ttu-id="c5bed-110">Пример 1: удаление пакетной задачи по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="c5bed-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="c5bed-111">Эта команда останавливает задачу с ИДЕНТИФИКАТОРом Task23 в задаче с ИД задания 000001.</span><span class="sxs-lookup"><span data-stu-id="c5bed-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="c5bed-112">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c5bed-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="c5bed-113">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="c5bed-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c5bed-114">Пример 2: остановка пакетной задачи с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="c5bed-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="c5bed-115">Эта команда возвращает пакетную задачу с ИДЕНТИФИКАТОРом Task26 в задании с ИД задания 000001 с помощью командлета Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="c5bed-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="c5bed-116">Команда передает эту задачу текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="c5bed-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c5bed-117">Команда останавливает эту задачу.</span><span class="sxs-lookup"><span data-stu-id="c5bed-117">The command stops that task.</span></span>

## <span data-ttu-id="c5bed-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5bed-118">PARAMETERS</span></span>

### <span data-ttu-id="c5bed-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c5bed-119">-BatchContext</span></span>
<span data-ttu-id="c5bed-120">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="c5bed-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c5bed-121">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="c5bed-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c5bed-122">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="c5bed-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c5bed-123">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="c5bed-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c5bed-124">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c5bed-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c5bed-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5bed-125">-DefaultProfile</span></span>
<span data-ttu-id="c5bed-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5bed-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5bed-127">-ID</span><span class="sxs-lookup"><span data-stu-id="c5bed-127">-Id</span></span>
<span data-ttu-id="c5bed-128">Указывает идентификатор задачи, которую завершает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c5bed-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bed-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="c5bed-129">-JobId</span></span>
<span data-ttu-id="c5bed-130">Указывает идентификатор задания, содержащего задачу.</span><span class="sxs-lookup"><span data-stu-id="c5bed-130">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bed-131">-Задача</span><span class="sxs-lookup"><span data-stu-id="c5bed-131">-Task</span></span>
<span data-ttu-id="c5bed-132">Указывает задачу, которую завершает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c5bed-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="c5bed-133">Чтобы получить объект **PSCloudTask** , используйте командлет Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="c5bed-133">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bed-134">CommonParameters</span></span>
<span data-ttu-id="c5bed-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5bed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bed-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5bed-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bed-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5bed-137">INPUTS</span></span>

### <span data-ttu-id="c5bed-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c5bed-138">BatchAccountContext</span></span>
<span data-ttu-id="c5bed-139">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c5bed-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c5bed-140">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="c5bed-140">PSCloudTask</span></span>
<span data-ttu-id="c5bed-141">Параметр "задача" принимает значение типа "PSCloudTask" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c5bed-141">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="c5bed-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5bed-142">OUTPUTS</span></span>

## <span data-ttu-id="c5bed-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5bed-143">NOTES</span></span>

## <span data-ttu-id="c5bed-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5bed-144">RELATED LINKS</span></span>

[<span data-ttu-id="c5bed-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c5bed-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="c5bed-146">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c5bed-146">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="c5bed-147">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c5bed-147">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="c5bed-148">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="c5bed-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


