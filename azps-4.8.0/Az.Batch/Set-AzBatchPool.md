---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 423f249a7971883cbe47d8f499fdd780980362f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079175"
---
# <span data-ttu-id="5dcba-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5dcba-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="5dcba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5dcba-102">SYNOPSIS</span></span>
<span data-ttu-id="5dcba-103">Обновляет свойства пула.</span><span class="sxs-lookup"><span data-stu-id="5dcba-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="5dcba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5dcba-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dcba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dcba-105">DESCRIPTION</span></span>
<span data-ttu-id="5dcba-106">Командлет **Set-AzBatchPool** обновляет свойства пула в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="5dcba-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="5dcba-107">Используйте командлет Get-AzBatchPool, чтобы получить объект **PSCloudPool** .</span><span class="sxs-lookup"><span data-stu-id="5dcba-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="5dcba-108">Измените свойства объекта, а затем используйте текущий командлет для фиксации изменений в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="5dcba-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="5dcba-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5dcba-109">EXAMPLES</span></span>

### <span data-ttu-id="5dcba-110">Пример 1: Обновление пула</span><span class="sxs-lookup"><span data-stu-id="5dcba-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="5dcba-111">Первая команда получает пул с помощью **Get-AzBatchPool** , а затем сохраняет его в переменной $pool.</span><span class="sxs-lookup"><span data-stu-id="5dcba-111">The first command gets a pool by using **Get-AzBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="5dcba-112">Следующие три команды изменяют спецификацию Start Task для объекта $Pool.</span><span class="sxs-lookup"><span data-stu-id="5dcba-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="5dcba-113">Последняя команда обновляет пакетную службу таким образом, чтобы она соответствовала локальному объекту в $Pool.</span><span class="sxs-lookup"><span data-stu-id="5dcba-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="5dcba-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5dcba-114">PARAMETERS</span></span>

### <span data-ttu-id="5dcba-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5dcba-115">-BatchContext</span></span>
<span data-ttu-id="5dcba-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="5dcba-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5dcba-117">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="5dcba-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5dcba-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="5dcba-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5dcba-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="5dcba-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5dcba-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5dcba-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5dcba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dcba-121">-DefaultProfile</span></span>
<span data-ttu-id="5dcba-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5dcba-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dcba-123">-Пул</span><span class="sxs-lookup"><span data-stu-id="5dcba-123">-Pool</span></span>
<span data-ttu-id="5dcba-124">Указывает **PSCloudPool** , на который этот командлет обновляет службу пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="5dcba-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="5dcba-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dcba-125">CommonParameters</span></span>
<span data-ttu-id="5dcba-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5dcba-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dcba-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5dcba-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dcba-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5dcba-128">INPUTS</span></span>

### <span data-ttu-id="5dcba-129">Microsoft.Azure.Commands.BatCH. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="5dcba-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="5dcba-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5dcba-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5dcba-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dcba-131">OUTPUTS</span></span>

### <span data-ttu-id="5dcba-132">System. void</span><span class="sxs-lookup"><span data-stu-id="5dcba-132">System.Void</span></span>

## <span data-ttu-id="5dcba-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="5dcba-133">NOTES</span></span>

## <span data-ttu-id="5dcba-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5dcba-134">RELATED LINKS</span></span>

[<span data-ttu-id="5dcba-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5dcba-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="5dcba-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5dcba-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5dcba-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5dcba-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="5dcba-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5dcba-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="5dcba-139">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="5dcba-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
