---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 86e977c3d538c9eeb5f26da7d70db1726adf119b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731826"
---
# <span data-ttu-id="2514c-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2514c-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="2514c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2514c-102">SYNOPSIS</span></span>
<span data-ttu-id="2514c-103">Обновляет пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="2514c-103">Updates a Batch job.</span></span>

## <span data-ttu-id="2514c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2514c-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2514c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2514c-105">DESCRIPTION</span></span>
<span data-ttu-id="2514c-106">Командлет **Set-AzBatchJob** обновляет пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="2514c-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="2514c-107">Используйте командлет Get-AzBatchJob, чтобы получить объект **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="2514c-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="2514c-108">Измените свойства объекта, а затем используйте текущий командлет для фиксации изменений в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="2514c-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="2514c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2514c-109">EXAMPLES</span></span>

### <span data-ttu-id="2514c-110">Пример 1: обновление задания</span><span class="sxs-lookup"><span data-stu-id="2514c-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="2514c-111">Первая команда получает задание с помощью **Get-AzBatchJob** , а затем сохраняет его в переменной $job.</span><span class="sxs-lookup"><span data-stu-id="2514c-111">The first command gets a job by using **Get-AzBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="2514c-112">Вторая команда изменяет спецификацию приоритета для объекта $Job.</span><span class="sxs-lookup"><span data-stu-id="2514c-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="2514c-113">Последняя команда обновляет пакетную службу таким образом, чтобы она соответствовала локальному объекту в $Job.</span><span class="sxs-lookup"><span data-stu-id="2514c-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="2514c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2514c-114">PARAMETERS</span></span>

### <span data-ttu-id="2514c-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2514c-115">-BatchContext</span></span>
<span data-ttu-id="2514c-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="2514c-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2514c-117">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="2514c-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2514c-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="2514c-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2514c-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="2514c-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2514c-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2514c-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2514c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2514c-121">-DefaultProfile</span></span>
<span data-ttu-id="2514c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2514c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2514c-123">-Job</span><span class="sxs-lookup"><span data-stu-id="2514c-123">-Job</span></span>
<span data-ttu-id="2514c-124">Указывает **PSCloudJob** , на который этот командлет обновляет службу пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="2514c-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="2514c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2514c-125">CommonParameters</span></span>
<span data-ttu-id="2514c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2514c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2514c-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2514c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2514c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2514c-128">INPUTS</span></span>

### <span data-ttu-id="2514c-129">Microsoft.Azure.Commands.BatCH. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="2514c-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="2514c-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2514c-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2514c-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2514c-131">OUTPUTS</span></span>

### <span data-ttu-id="2514c-132">System. void</span><span class="sxs-lookup"><span data-stu-id="2514c-132">System.Void</span></span>

## <span data-ttu-id="2514c-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="2514c-133">NOTES</span></span>

## <span data-ttu-id="2514c-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2514c-134">RELATED LINKS</span></span>

[<span data-ttu-id="2514c-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2514c-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="2514c-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2514c-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="2514c-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2514c-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="2514c-138">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2514c-138">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2514c-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2514c-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="2514c-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2514c-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="2514c-141">Остановить-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2514c-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="2514c-142">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="2514c-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


