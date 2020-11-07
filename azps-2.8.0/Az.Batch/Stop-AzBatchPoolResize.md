---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 9e970251671297a6fa4a0019bb663c9e34cbe4d7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913138"
---
# <span data-ttu-id="a007f-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="a007f-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="a007f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a007f-102">SYNOPSIS</span></span>
<span data-ttu-id="a007f-103">Останавливает операцию изменения размера пула.</span><span class="sxs-lookup"><span data-stu-id="a007f-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="a007f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a007f-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a007f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a007f-105">DESCRIPTION</span></span>
<span data-ttu-id="a007f-106">Командлет **Stop-AzBatchPoolResize** останавливает пакетную операцию по изменению размера пакета Azure для пула.</span><span class="sxs-lookup"><span data-stu-id="a007f-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="a007f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a007f-107">EXAMPLES</span></span>

### <span data-ttu-id="a007f-108">Пример 1: прекращение изменения размера пула</span><span class="sxs-lookup"><span data-stu-id="a007f-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="a007f-109">Эта команда останавливает операцию изменения размера в пуле с ИДЕНТИФИКАТОРом ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="a007f-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="a007f-110">Используйте командлет Get-AzBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="a007f-110">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a007f-111">Пример 2: прекращение изменения размера пула с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="a007f-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="a007f-112">Эта команда останавливает изменение размера пула с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="a007f-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="a007f-113">Команда получает пул с ИД ContosoPool06 с помощью командлета Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="a007f-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="a007f-114">Команда передает этот объект пула в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="a007f-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="a007f-115">Команда останавливает операцию изменения размера в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="a007f-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="a007f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a007f-116">PARAMETERS</span></span>

### <span data-ttu-id="a007f-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a007f-117">-BatchContext</span></span>
<span data-ttu-id="a007f-118">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="a007f-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a007f-119">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="a007f-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a007f-120">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="a007f-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a007f-121">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="a007f-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a007f-122">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a007f-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a007f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a007f-123">-DefaultProfile</span></span>
<span data-ttu-id="a007f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a007f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a007f-125">-ID</span><span class="sxs-lookup"><span data-stu-id="a007f-125">-Id</span></span>
<span data-ttu-id="a007f-126">Указывает идентификатор пула, для которого этот командлет останавливает операцию изменения размера.</span><span class="sxs-lookup"><span data-stu-id="a007f-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a007f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a007f-127">CommonParameters</span></span>
<span data-ttu-id="a007f-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a007f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a007f-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a007f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a007f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a007f-130">INPUTS</span></span>

### <span data-ttu-id="a007f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a007f-131">System.String</span></span>

### <span data-ttu-id="a007f-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a007f-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a007f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a007f-133">OUTPUTS</span></span>

### <span data-ttu-id="a007f-134">System. void</span><span class="sxs-lookup"><span data-stu-id="a007f-134">System.Void</span></span>

## <span data-ttu-id="a007f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a007f-135">NOTES</span></span>

## <span data-ttu-id="a007f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a007f-136">RELATED LINKS</span></span>

[<span data-ttu-id="a007f-137">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a007f-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a007f-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="a007f-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="a007f-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="a007f-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="a007f-140">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="a007f-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


