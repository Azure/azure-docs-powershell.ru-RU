---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 1104eed4d60405226cdc6dad351ae418b84142e2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079177"
---
# <span data-ttu-id="1772d-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1772d-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="1772d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1772d-102">SYNOPSIS</span></span>
<span data-ttu-id="1772d-103">Обновляет пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="1772d-103">Updates a Batch job.</span></span>

## <span data-ttu-id="1772d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1772d-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1772d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1772d-105">DESCRIPTION</span></span>
<span data-ttu-id="1772d-106">Командлет **Set-AzBatchJob** обновляет пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="1772d-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="1772d-107">Используйте командлет Get-AzBatchJob, чтобы получить объект **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="1772d-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="1772d-108">Измените свойства объекта, а затем используйте текущий командлет для фиксации изменений в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="1772d-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="1772d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1772d-109">EXAMPLES</span></span>

### <span data-ttu-id="1772d-110">Пример 1: обновление задания</span><span class="sxs-lookup"><span data-stu-id="1772d-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="1772d-111">Первая команда получает задание с помощью **Get-AzBatchJob** , а затем сохраняет его в переменной $job.</span><span class="sxs-lookup"><span data-stu-id="1772d-111">The first command gets a job by using **Get-AzBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="1772d-112">Вторая команда изменяет спецификацию приоритета для объекта $Job.</span><span class="sxs-lookup"><span data-stu-id="1772d-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="1772d-113">Последняя команда обновляет пакетную службу таким образом, чтобы она соответствовала локальному объекту в $Job.</span><span class="sxs-lookup"><span data-stu-id="1772d-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="1772d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1772d-114">PARAMETERS</span></span>

### <span data-ttu-id="1772d-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1772d-115">-BatchContext</span></span>
<span data-ttu-id="1772d-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="1772d-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1772d-117">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="1772d-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1772d-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="1772d-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1772d-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="1772d-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1772d-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1772d-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1772d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1772d-121">-DefaultProfile</span></span>
<span data-ttu-id="1772d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1772d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1772d-123">-Job</span><span class="sxs-lookup"><span data-stu-id="1772d-123">-Job</span></span>
<span data-ttu-id="1772d-124">Указывает **PSCloudJob** , на который этот командлет обновляет службу пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="1772d-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="1772d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1772d-125">CommonParameters</span></span>
<span data-ttu-id="1772d-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1772d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1772d-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1772d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1772d-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1772d-128">INPUTS</span></span>

### <span data-ttu-id="1772d-129">Microsoft.Azure.Commands.BatCH. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="1772d-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="1772d-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1772d-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1772d-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1772d-131">OUTPUTS</span></span>

### <span data-ttu-id="1772d-132">System. void</span><span class="sxs-lookup"><span data-stu-id="1772d-132">System.Void</span></span>

## <span data-ttu-id="1772d-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="1772d-133">NOTES</span></span>

## <span data-ttu-id="1772d-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1772d-134">RELATED LINKS</span></span>

[<span data-ttu-id="1772d-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1772d-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="1772d-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1772d-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="1772d-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1772d-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="1772d-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1772d-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1772d-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1772d-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="1772d-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1772d-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="1772d-141">Остановить-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1772d-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="1772d-142">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="1772d-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)