---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: c0f1dc4972e3b71dce74bffb7a72e782774a2734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556807"
---
# <span data-ttu-id="c21e3-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c21e3-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="c21e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c21e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c21e3-103">Обновляет свойства пула.</span><span class="sxs-lookup"><span data-stu-id="c21e3-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c21e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c21e3-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c21e3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c21e3-105">DESCRIPTION</span></span>
<span data-ttu-id="c21e3-106">Командлет **Set-AzureBatchPool** обновляет свойства пула в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="c21e3-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="c21e3-107">Используйте командлет Get-AzureBatchPool, чтобы получить объект **PSCloudPool** .</span><span class="sxs-lookup"><span data-stu-id="c21e3-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="c21e3-108">Измените свойства объекта, а затем используйте текущий командлет для фиксации изменений в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="c21e3-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="c21e3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c21e3-109">EXAMPLES</span></span>

### <span data-ttu-id="c21e3-110">Пример 1: Обновление пула</span><span class="sxs-lookup"><span data-stu-id="c21e3-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="c21e3-111">Первая команда получает пул с помощью **Get-AzureBatchPool** , а затем сохраняет его в переменной $pool.</span><span class="sxs-lookup"><span data-stu-id="c21e3-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="c21e3-112">Следующие три команды изменяют спецификацию Start Task для объекта $Pool.</span><span class="sxs-lookup"><span data-stu-id="c21e3-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="c21e3-113">Последняя команда обновляет пакетную службу таким образом, чтобы она соответствовала локальному объекту в $Pool.</span><span class="sxs-lookup"><span data-stu-id="c21e3-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="c21e3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c21e3-114">PARAMETERS</span></span>

### <span data-ttu-id="c21e3-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c21e3-115">-BatchContext</span></span>
<span data-ttu-id="c21e3-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="c21e3-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c21e3-117">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="c21e3-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c21e3-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="c21e3-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c21e3-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="c21e3-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c21e3-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c21e3-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c21e3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c21e3-121">-DefaultProfile</span></span>
<span data-ttu-id="c21e3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c21e3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c21e3-123">-Пул</span><span class="sxs-lookup"><span data-stu-id="c21e3-123">-Pool</span></span>
<span data-ttu-id="c21e3-124">Указывает **PSCloudPool** , на который этот командлет обновляет службу пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="c21e3-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="c21e3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c21e3-125">CommonParameters</span></span>
<span data-ttu-id="c21e3-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c21e3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c21e3-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c21e3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c21e3-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c21e3-128">INPUTS</span></span>

### <span data-ttu-id="c21e3-129">Microsoft.Azure.Commands.BatCH. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="c21e3-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>
<span data-ttu-id="c21e3-130">Параметры: Pool (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c21e3-130">Parameters: Pool (ByValue)</span></span>

### <span data-ttu-id="c21e3-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c21e3-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c21e3-132">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c21e3-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c21e3-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c21e3-133">OUTPUTS</span></span>

### <span data-ttu-id="c21e3-134">System. void</span><span class="sxs-lookup"><span data-stu-id="c21e3-134">System.Void</span></span>

## <span data-ttu-id="c21e3-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="c21e3-135">NOTES</span></span>

## <span data-ttu-id="c21e3-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c21e3-136">RELATED LINKS</span></span>

[<span data-ttu-id="c21e3-137">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c21e3-137">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="c21e3-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c21e3-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c21e3-139">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c21e3-139">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="c21e3-140">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c21e3-140">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="c21e3-141">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="c21e3-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


