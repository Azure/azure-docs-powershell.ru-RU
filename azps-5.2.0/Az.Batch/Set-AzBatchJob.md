---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 1104eed4d60405226cdc6dad351ae418b84142e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393620"
---
# <span data-ttu-id="a3e95-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3e95-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="a3e95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3e95-102">SYNOPSIS</span></span>
<span data-ttu-id="a3e95-103">Обновляет задание пакета.</span><span class="sxs-lookup"><span data-stu-id="a3e95-103">Updates a Batch job.</span></span>

## <span data-ttu-id="a3e95-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a3e95-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3e95-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3e95-105">DESCRIPTION</span></span>
<span data-ttu-id="a3e95-106">Для обновления задания пакета Azure обновляется cmdlet **Set-AzBatchJob.**</span><span class="sxs-lookup"><span data-stu-id="a3e95-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="a3e95-107">Используйте Get-AzBatchJob для получения объекта **PSCloudJob.**</span><span class="sxs-lookup"><span data-stu-id="a3e95-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="a3e95-108">Измените свойства этого объекта, а затем с помощью текущего cmdlet зафиксировать изменения в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="a3e95-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="a3e95-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a3e95-109">EXAMPLES</span></span>

### <span data-ttu-id="a3e95-110">Пример 1. Обновление задания</span><span class="sxs-lookup"><span data-stu-id="a3e95-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="a3e95-111">Первая команда получает задание с помощью **Get-AzBatchJob,** а затем сохраняет ее в $Job переменной.</span><span class="sxs-lookup"><span data-stu-id="a3e95-111">The first command gets a job by using **Get-AzBatchJob**, and then stores it in the $Job variable.</span></span>
<span data-ttu-id="a3e95-112">Вторая команда изменяет спецификацию приоритета объекта $Job.</span><span class="sxs-lookup"><span data-stu-id="a3e95-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="a3e95-113">Конечная команда обновляет пакетную службу в соответствие с локальным объектом в $Job.</span><span class="sxs-lookup"><span data-stu-id="a3e95-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="a3e95-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3e95-114">PARAMETERS</span></span>

### <span data-ttu-id="a3e95-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a3e95-115">-BatchContext</span></span>
<span data-ttu-id="a3e95-116">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="a3e95-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a3e95-117">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a3e95-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a3e95-118">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="a3e95-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a3e95-119">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a3e95-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a3e95-120">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a3e95-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a3e95-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3e95-121">-DefaultProfile</span></span>
<span data-ttu-id="a3e95-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3e95-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3e95-123">-Job</span><span class="sxs-lookup"><span data-stu-id="a3e95-123">-Job</span></span>
<span data-ttu-id="a3e95-124">Указывает **PSCloudJob,** для которого этот cmdlet обновляет пакетную службу.</span><span class="sxs-lookup"><span data-stu-id="a3e95-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="a3e95-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e95-125">CommonParameters</span></span>
<span data-ttu-id="a3e95-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3e95-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3e95-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3e95-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e95-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3e95-128">INPUTS</span></span>

### <span data-ttu-id="a3e95-129">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="a3e95-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="a3e95-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a3e95-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a3e95-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3e95-131">OUTPUTS</span></span>

### <span data-ttu-id="a3e95-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="a3e95-132">System.Void</span></span>

## <span data-ttu-id="a3e95-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a3e95-133">NOTES</span></span>

## <span data-ttu-id="a3e95-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3e95-134">RELATED LINKS</span></span>

[<span data-ttu-id="a3e95-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3e95-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="a3e95-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3e95-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="a3e95-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3e95-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="a3e95-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a3e95-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a3e95-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3e95-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="a3e95-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3e95-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="a3e95-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3e95-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="a3e95-142">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="a3e95-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
