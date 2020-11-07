---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 8db1f11cfd434beb52eb32e4b175b2dab67ecbdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733175"
---
# <span data-ttu-id="47cae-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="47cae-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="47cae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47cae-102">SYNOPSIS</span></span>
<span data-ttu-id="47cae-103">Останавливает операцию изменения размера пула.</span><span class="sxs-lookup"><span data-stu-id="47cae-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47cae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47cae-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47cae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47cae-105">DESCRIPTION</span></span>
<span data-ttu-id="47cae-106">Командлет **Stop-AzureBatchPoolResize** останавливает пакетную операцию по изменению размера пакета Azure для пула.</span><span class="sxs-lookup"><span data-stu-id="47cae-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="47cae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47cae-107">EXAMPLES</span></span>

### <span data-ttu-id="47cae-108">Пример 1: прекращение изменения размера пула</span><span class="sxs-lookup"><span data-stu-id="47cae-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="47cae-109">Эта команда останавливает операцию изменения размера в пуле с ИДЕНТИФИКАТОРом ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="47cae-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="47cae-110">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="47cae-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="47cae-111">Пример 2: прекращение изменения размера пула с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="47cae-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="47cae-112">Эта команда останавливает изменение размера пула с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="47cae-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="47cae-113">Команда получает пул с ИД ContosoPool06 с помощью командлета Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="47cae-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="47cae-114">Команда передает этот объект пула в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="47cae-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="47cae-115">Команда останавливает операцию изменения размера в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="47cae-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="47cae-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47cae-116">PARAMETERS</span></span>

### <span data-ttu-id="47cae-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="47cae-117">-BatchContext</span></span>
<span data-ttu-id="47cae-118">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="47cae-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="47cae-119">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="47cae-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="47cae-120">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="47cae-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="47cae-121">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="47cae-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="47cae-122">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="47cae-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="47cae-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47cae-123">-DefaultProfile</span></span>
<span data-ttu-id="47cae-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47cae-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47cae-125">-ID</span><span class="sxs-lookup"><span data-stu-id="47cae-125">-Id</span></span>
<span data-ttu-id="47cae-126">Указывает идентификатор пула, для которого этот командлет останавливает операцию изменения размера.</span><span class="sxs-lookup"><span data-stu-id="47cae-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="47cae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47cae-127">CommonParameters</span></span>
<span data-ttu-id="47cae-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47cae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47cae-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47cae-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47cae-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47cae-130">INPUTS</span></span>

### <span data-ttu-id="47cae-131">System. String</span><span class="sxs-lookup"><span data-stu-id="47cae-131">System.String</span></span>

### <span data-ttu-id="47cae-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="47cae-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="47cae-133">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="47cae-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="47cae-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47cae-134">OUTPUTS</span></span>

### <span data-ttu-id="47cae-135">System. void</span><span class="sxs-lookup"><span data-stu-id="47cae-135">System.Void</span></span>

## <span data-ttu-id="47cae-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="47cae-136">NOTES</span></span>

## <span data-ttu-id="47cae-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47cae-137">RELATED LINKS</span></span>

[<span data-ttu-id="47cae-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="47cae-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="47cae-139">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="47cae-139">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="47cae-140">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="47cae-140">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="47cae-141">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="47cae-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


