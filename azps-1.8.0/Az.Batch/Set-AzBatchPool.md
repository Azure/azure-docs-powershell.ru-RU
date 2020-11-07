---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 7ab0d9f64b14f6fbdd572f69ecb081114d78891d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913106"
---
# <span data-ttu-id="d38d6-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="d38d6-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="d38d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d38d6-102">SYNOPSIS</span></span>
<span data-ttu-id="d38d6-103">Обновляет свойства пула.</span><span class="sxs-lookup"><span data-stu-id="d38d6-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="d38d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d38d6-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d38d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d38d6-105">DESCRIPTION</span></span>
<span data-ttu-id="d38d6-106">Командлет **Set-AzBatchPool** обновляет свойства пула в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="d38d6-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="d38d6-107">Используйте командлет Get-AzBatchPool, чтобы получить объект **PSCloudPool** .</span><span class="sxs-lookup"><span data-stu-id="d38d6-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="d38d6-108">Измените свойства объекта, а затем используйте текущий командлет для фиксации изменений в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="d38d6-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="d38d6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d38d6-109">EXAMPLES</span></span>

### <span data-ttu-id="d38d6-110">Пример 1: Обновление пула</span><span class="sxs-lookup"><span data-stu-id="d38d6-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="d38d6-111">Первая команда получает пул с помощью **Get-AzBatchPool** , а затем сохраняет его в переменной $pool.</span><span class="sxs-lookup"><span data-stu-id="d38d6-111">The first command gets a pool by using **Get-AzBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="d38d6-112">Следующие три команды изменяют спецификацию Start Task для объекта $Pool.</span><span class="sxs-lookup"><span data-stu-id="d38d6-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="d38d6-113">Последняя команда обновляет пакетную службу таким образом, чтобы она соответствовала локальному объекту в $Pool.</span><span class="sxs-lookup"><span data-stu-id="d38d6-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="d38d6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d38d6-114">PARAMETERS</span></span>

### <span data-ttu-id="d38d6-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d38d6-115">-BatchContext</span></span>
<span data-ttu-id="d38d6-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="d38d6-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d38d6-117">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="d38d6-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d38d6-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="d38d6-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d38d6-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="d38d6-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d38d6-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d38d6-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d38d6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d38d6-121">-DefaultProfile</span></span>
<span data-ttu-id="d38d6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d38d6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d38d6-123">-Пул</span><span class="sxs-lookup"><span data-stu-id="d38d6-123">-Pool</span></span>
<span data-ttu-id="d38d6-124">Указывает **PSCloudPool** , на который этот командлет обновляет службу пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="d38d6-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="d38d6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d38d6-125">CommonParameters</span></span>
<span data-ttu-id="d38d6-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d38d6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d38d6-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d38d6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d38d6-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d38d6-128">INPUTS</span></span>

### <span data-ttu-id="d38d6-129">Microsoft.Azure.Commands.BatCH. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="d38d6-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="d38d6-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d38d6-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d38d6-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d38d6-131">OUTPUTS</span></span>

### <span data-ttu-id="d38d6-132">System. void</span><span class="sxs-lookup"><span data-stu-id="d38d6-132">System.Void</span></span>

## <span data-ttu-id="d38d6-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d38d6-133">NOTES</span></span>

## <span data-ttu-id="d38d6-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d38d6-134">RELATED LINKS</span></span>

[<span data-ttu-id="d38d6-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="d38d6-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="d38d6-136">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d38d6-136">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d38d6-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="d38d6-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="d38d6-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="d38d6-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="d38d6-139">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="d38d6-139">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


