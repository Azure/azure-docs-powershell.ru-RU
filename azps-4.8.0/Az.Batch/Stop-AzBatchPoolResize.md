---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 229877db7a3077a4b1951a06914c842e63384ba6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235089"
---
# <span data-ttu-id="bdd2c-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="bdd2c-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="bdd2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bdd2c-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd2c-103">Останавливает операцию изменения размера пула.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="bdd2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bdd2c-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdd2c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdd2c-105">DESCRIPTION</span></span>
<span data-ttu-id="bdd2c-106">Командлет **Stop-AzBatchPoolResize** останавливает пакетную операцию по изменению размера пакета Azure для пула.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="bdd2c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bdd2c-107">EXAMPLES</span></span>

### <span data-ttu-id="bdd2c-108">Пример 1: прекращение изменения размера пула</span><span class="sxs-lookup"><span data-stu-id="bdd2c-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="bdd2c-109">Эта команда останавливает операцию изменения размера в пуле с ИДЕНТИФИКАТОРом ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="bdd2c-110">Используйте командлет Get-AzBatchAccountKey для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="bdd2c-111">Пример 2: прекращение изменения размера пула с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="bdd2c-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="bdd2c-112">Эта команда останавливает изменение размера пула с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="bdd2c-113">Команда получает пул с ИД ContosoPool06 с помощью командлета Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="bdd2c-114">Команда передает этот объект пула в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="bdd2c-115">Команда останавливает операцию изменения размера в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="bdd2c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bdd2c-116">PARAMETERS</span></span>

### <span data-ttu-id="bdd2c-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bdd2c-117">-BatchContext</span></span>
<span data-ttu-id="bdd2c-118">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bdd2c-119">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bdd2c-120">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bdd2c-121">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bdd2c-122">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bdd2c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd2c-123">-DefaultProfile</span></span>
<span data-ttu-id="bdd2c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdd2c-125">-ID</span><span class="sxs-lookup"><span data-stu-id="bdd2c-125">-Id</span></span>
<span data-ttu-id="bdd2c-126">Указывает идентификатор пула, для которого этот командлет останавливает операцию изменения размера.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="bdd2c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd2c-127">CommonParameters</span></span>
<span data-ttu-id="bdd2c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd2c-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdd2c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd2c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bdd2c-130">INPUTS</span></span>

### <span data-ttu-id="bdd2c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bdd2c-131">System.String</span></span>

### <span data-ttu-id="bdd2c-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bdd2c-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bdd2c-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdd2c-133">OUTPUTS</span></span>

### <span data-ttu-id="bdd2c-134">System. void</span><span class="sxs-lookup"><span data-stu-id="bdd2c-134">System.Void</span></span>

## <span data-ttu-id="bdd2c-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="bdd2c-135">NOTES</span></span>

## <span data-ttu-id="bdd2c-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdd2c-136">RELATED LINKS</span></span>

[<span data-ttu-id="bdd2c-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="bdd2c-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bdd2c-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="bdd2c-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="bdd2c-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="bdd2c-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="bdd2c-140">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="bdd2c-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
