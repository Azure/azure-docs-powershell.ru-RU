---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 153e566df3e2ab6f758d139719af1e812e0476ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559292"
---
# <span data-ttu-id="93fef-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="93fef-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="93fef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93fef-102">SYNOPSIS</span></span>
<span data-ttu-id="93fef-103">Останавливает операцию изменения размера пула.</span><span class="sxs-lookup"><span data-stu-id="93fef-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93fef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93fef-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93fef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93fef-105">DESCRIPTION</span></span>
<span data-ttu-id="93fef-106">Командлет **Stop-AzureBatchPoolResize** останавливает пакетную операцию по изменению размера пакета Azure для пула.</span><span class="sxs-lookup"><span data-stu-id="93fef-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="93fef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93fef-107">EXAMPLES</span></span>

### <span data-ttu-id="93fef-108">Пример 1: прекращение изменения размера пула</span><span class="sxs-lookup"><span data-stu-id="93fef-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="93fef-109">Эта команда останавливает операцию изменения размера в пуле с ИДЕНТИФИКАТОРом ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="93fef-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="93fef-110">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="93fef-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="93fef-111">Пример 2: прекращение изменения размера пула с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="93fef-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="93fef-112">Эта команда останавливает изменение размера пула с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="93fef-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="93fef-113">Команда получает пул с ИД ContosoPool06 с помощью командлета Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="93fef-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="93fef-114">Команда передает этот объект пула в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="93fef-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="93fef-115">Команда останавливает операцию изменения размера в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="93fef-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="93fef-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93fef-116">PARAMETERS</span></span>

### <span data-ttu-id="93fef-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="93fef-117">-BatchContext</span></span>
<span data-ttu-id="93fef-118">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="93fef-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="93fef-119">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="93fef-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="93fef-120">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="93fef-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="93fef-121">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="93fef-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="93fef-122">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="93fef-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="93fef-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93fef-123">-DefaultProfile</span></span>
<span data-ttu-id="93fef-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93fef-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93fef-125">-ID</span><span class="sxs-lookup"><span data-stu-id="93fef-125">-Id</span></span>
<span data-ttu-id="93fef-126">Указывает идентификатор пула, для которого этот командлет останавливает операцию изменения размера.</span><span class="sxs-lookup"><span data-stu-id="93fef-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93fef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93fef-127">CommonParameters</span></span>
<span data-ttu-id="93fef-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93fef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93fef-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93fef-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93fef-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93fef-130">INPUTS</span></span>

### <span data-ttu-id="93fef-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="93fef-131">BatchAccountContext</span></span>
<span data-ttu-id="93fef-132">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="93fef-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="93fef-133">Подстрок</span><span class="sxs-lookup"><span data-stu-id="93fef-133">String</span></span>
<span data-ttu-id="93fef-134">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="93fef-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="93fef-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93fef-135">OUTPUTS</span></span>

## <span data-ttu-id="93fef-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="93fef-136">NOTES</span></span>

## <span data-ttu-id="93fef-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93fef-137">RELATED LINKS</span></span>

[<span data-ttu-id="93fef-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="93fef-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="93fef-139">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="93fef-139">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="93fef-140">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="93fef-140">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="93fef-141">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="93fef-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


