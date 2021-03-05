---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 26a280ef567ed09ff14cf143048aadceeeed29e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991724"
---
# <span data-ttu-id="ecc9e-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ecc9e-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="ecc9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecc9e-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc9e-103">Обновляет свойства пула.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="ecc9e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ecc9e-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecc9e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecc9e-105">DESCRIPTION</span></span>
<span data-ttu-id="ecc9e-106">**Cmdlet Set-AzBatchPool** обновляет свойства пула в службе Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="ecc9e-107">Используйте Get-AzBatchPool для получения объекта **PSCloudPool.**</span><span class="sxs-lookup"><span data-stu-id="ecc9e-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="ecc9e-108">Измените свойства этого объекта, а затем с помощью текущего cmdlet зафиксировать изменения в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="ecc9e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ecc9e-109">EXAMPLES</span></span>

### <span data-ttu-id="ecc9e-110">Пример 1. Обновление пула</span><span class="sxs-lookup"><span data-stu-id="ecc9e-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="ecc9e-111">Первая команда получает пул с помощью **Get-AzBatchPool,** а затем сохраняет его в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-111">The first command gets a pool by using **Get-AzBatchPool**, and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="ecc9e-112">Следующие три команды изменяют спецификацию задачи начала для $Pool объекта.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="ecc9e-113">Конечная команда обновляет пакетную службу в соответствие с локальным объектом в $Pool.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="ecc9e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecc9e-114">PARAMETERS</span></span>

### <span data-ttu-id="ecc9e-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ecc9e-115">-BatchContext</span></span>
<span data-ttu-id="ecc9e-116">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ecc9e-117">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ecc9e-118">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ecc9e-119">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ecc9e-120">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ecc9e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc9e-121">-DefaultProfile</span></span>
<span data-ttu-id="ecc9e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecc9e-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="ecc9e-123">-Pool</span></span>
<span data-ttu-id="ecc9e-124">Определяет **psCloudPool,** для которого этот cmdlet обновляет пакетную службу.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecc9e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc9e-125">CommonParameters</span></span>
<span data-ttu-id="ecc9e-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc9e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc9e-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecc9e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc9e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ecc9e-128">INPUTS</span></span>

### <span data-ttu-id="ecc9e-129">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="ecc9e-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="ecc9e-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ecc9e-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ecc9e-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ecc9e-131">OUTPUTS</span></span>

### <span data-ttu-id="ecc9e-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="ecc9e-132">System.Void</span></span>

## <span data-ttu-id="ecc9e-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ecc9e-133">NOTES</span></span>

## <span data-ttu-id="ecc9e-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecc9e-134">RELATED LINKS</span></span>

[<span data-ttu-id="ecc9e-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ecc9e-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="ecc9e-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ecc9e-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ecc9e-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ecc9e-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="ecc9e-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ecc9e-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="ecc9e-139">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="ecc9e-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
