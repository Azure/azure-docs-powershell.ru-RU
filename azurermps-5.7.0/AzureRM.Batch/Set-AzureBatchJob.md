---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: a878002c509fd2a895f61a97af1bef2afebc3691
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568240"
---
# <span data-ttu-id="4216f-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4216f-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="4216f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4216f-102">SYNOPSIS</span></span>
<span data-ttu-id="4216f-103">Обновляет пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="4216f-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4216f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4216f-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4216f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4216f-105">DESCRIPTION</span></span>
<span data-ttu-id="4216f-106">Командлет **Set-AzureBatchJob** обновляет пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="4216f-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="4216f-107">Используйте командлет Get-AzureBatchJob, чтобы получить объект **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="4216f-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="4216f-108">Измените свойства объекта, а затем используйте текущий командлет для фиксации изменений в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="4216f-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="4216f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4216f-109">EXAMPLES</span></span>

### <span data-ttu-id="4216f-110">Пример 1: обновление задания</span><span class="sxs-lookup"><span data-stu-id="4216f-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="4216f-111">Первая команда получает пул с помощью **Get-AzureBatchJob** , а затем сохраняет его в переменной $job.</span><span class="sxs-lookup"><span data-stu-id="4216f-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="4216f-112">Вторая команда изменяет спецификацию приоритета для объекта $Job.</span><span class="sxs-lookup"><span data-stu-id="4216f-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="4216f-113">Последняя команда обновляет пакетную службу таким образом, чтобы она соответствовала локальному объекту в $Job.</span><span class="sxs-lookup"><span data-stu-id="4216f-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="4216f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4216f-114">PARAMETERS</span></span>

### <span data-ttu-id="4216f-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4216f-115">-BatchContext</span></span>
<span data-ttu-id="4216f-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="4216f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4216f-117">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="4216f-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4216f-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="4216f-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4216f-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="4216f-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4216f-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4216f-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4216f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4216f-121">-DefaultProfile</span></span>
<span data-ttu-id="4216f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4216f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4216f-123">-Job</span><span class="sxs-lookup"><span data-stu-id="4216f-123">-Job</span></span>
<span data-ttu-id="4216f-124">Указывает **PSCloudJob** , на который этот командлет обновляет службу пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="4216f-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4216f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4216f-125">CommonParameters</span></span>
<span data-ttu-id="4216f-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4216f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4216f-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4216f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4216f-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4216f-128">INPUTS</span></span>

### <span data-ttu-id="4216f-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4216f-129">BatchAccountContext</span></span>
<span data-ttu-id="4216f-130">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4216f-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="4216f-131">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="4216f-131">PSCloudJob</span></span>
<span data-ttu-id="4216f-132">Параметр "задание" принимает значение типа "PSCloudJob" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4216f-132">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="4216f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4216f-133">OUTPUTS</span></span>

## <span data-ttu-id="4216f-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="4216f-134">NOTES</span></span>

## <span data-ttu-id="4216f-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4216f-135">RELATED LINKS</span></span>

[<span data-ttu-id="4216f-136">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4216f-136">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="4216f-137">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4216f-137">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="4216f-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4216f-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="4216f-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4216f-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="4216f-140">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4216f-140">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="4216f-141">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4216f-141">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="4216f-142">Остановить-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="4216f-142">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="4216f-143">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="4216f-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


