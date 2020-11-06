---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: eb15991e0bf7aefd60b53dbb02785a1b2004cb22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569704"
---
# <span data-ttu-id="f4b4f-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4b4f-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="f4b4f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b4f-103">Обновляет пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="f4b4f-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4b4f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4b4f-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4b4f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4b4f-105">DESCRIPTION</span></span>
<span data-ttu-id="f4b4f-106">Командлет **Set-AzureBatchJob** обновляет пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b4f-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="f4b4f-107">Используйте командлет Get-AzureBatchJob, чтобы получить объект **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="f4b4f-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="f4b4f-108">Измените свойства объекта, а затем используйте текущий командлет для фиксации изменений в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="f4b4f-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="f4b4f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4b4f-109">EXAMPLES</span></span>

### <span data-ttu-id="f4b4f-110">Пример 1: обновление задания</span><span class="sxs-lookup"><span data-stu-id="f4b4f-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="f4b4f-111">Первая команда получает пул с помощью **Get-AzureBatchJob** , а затем сохраняет его в переменной $job.</span><span class="sxs-lookup"><span data-stu-id="f4b4f-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="f4b4f-112">Вторая команда изменяет спецификацию приоритета для объекта $Job.</span><span class="sxs-lookup"><span data-stu-id="f4b4f-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="f4b4f-113">Последняя команда обновляет пакетную службу таким образом, чтобы она соответствовала локальному объекту в $Job.</span><span class="sxs-lookup"><span data-stu-id="f4b4f-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="f4b4f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4b4f-114">PARAMETERS</span></span>

### <span data-ttu-id="f4b4f-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f4b4f-115">-BatchContext</span></span>
<span data-ttu-id="f4b4f-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="f4b4f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f4b4f-117">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="f4b4f-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="f4b4f-118">-Job</span><span class="sxs-lookup"><span data-stu-id="f4b4f-118">-Job</span></span>
<span data-ttu-id="f4b4f-119">Указывает **PSCloudJob** , на который этот командлет обновляет службу пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="f4b4f-119">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b4f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b4f-120">-DefaultProfile</span></span>
<span data-ttu-id="f4b4f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b4f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4b4f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b4f-122">CommonParameters</span></span>
<span data-ttu-id="f4b4f-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4b4f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b4f-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4b4f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b4f-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4b4f-125">INPUTS</span></span>

### <span data-ttu-id="f4b4f-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f4b4f-126">BatchAccountContext</span></span>
<span data-ttu-id="f4b4f-127">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f4b4f-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="f4b4f-128">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="f4b4f-128">PSCloudJob</span></span>
<span data-ttu-id="f4b4f-129">Параметр "задание" принимает значение типа "PSCloudJob" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f4b4f-129">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="f4b4f-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4b4f-130">OUTPUTS</span></span>

## <span data-ttu-id="f4b4f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4b4f-131">NOTES</span></span>

## <span data-ttu-id="f4b4f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4b4f-132">RELATED LINKS</span></span>

[<span data-ttu-id="f4b4f-133">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4b4f-133">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="f4b4f-134">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4b4f-134">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="f4b4f-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4b4f-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="f4b4f-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f4b4f-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f4b4f-137">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4b4f-137">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="f4b4f-138">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4b4f-138">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="f4b4f-139">Остановить-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4b4f-139">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="f4b4f-140">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="f4b4f-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


