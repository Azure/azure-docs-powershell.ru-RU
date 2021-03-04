---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 339c3a537e84ff63a6eac0a6f1f63669ce4567ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959827"
---
# <span data-ttu-id="bec3c-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="bec3c-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="bec3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bec3c-102">SYNOPSIS</span></span>
<span data-ttu-id="bec3c-103">Останавливает операцию по окнам пула.</span><span class="sxs-lookup"><span data-stu-id="bec3c-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="bec3c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bec3c-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bec3c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bec3c-105">DESCRIPTION</span></span>
<span data-ttu-id="bec3c-106">Для остановки операции обработки пула пакетных пакетов Azure операция **stop-AzBatchPoolResize** прекращается.</span><span class="sxs-lookup"><span data-stu-id="bec3c-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="bec3c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bec3c-107">EXAMPLES</span></span>

### <span data-ttu-id="bec3c-108">Пример 1. Остановка resizing a pool</span><span class="sxs-lookup"><span data-stu-id="bec3c-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="bec3c-109">Эта команда останавливает операцию resize пула с ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="bec3c-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="bec3c-110">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="bec3c-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="bec3c-111">Пример 2. Остановка повторного использования пула с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="bec3c-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="bec3c-112">Эта команда прекращает размер пула с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="bec3c-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="bec3c-113">Команда получает пул с ИД ContosoPool06 с помощью Get-AzBatchPool командлета.</span><span class="sxs-lookup"><span data-stu-id="bec3c-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="bec3c-114">Эта команда передает объект пула текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="bec3c-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="bec3c-115">Команда останавливает операцию по окнованию пула.</span><span class="sxs-lookup"><span data-stu-id="bec3c-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="bec3c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bec3c-116">PARAMETERS</span></span>

### <span data-ttu-id="bec3c-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bec3c-117">-BatchContext</span></span>
<span data-ttu-id="bec3c-118">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="bec3c-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bec3c-119">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bec3c-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bec3c-120">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="bec3c-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bec3c-121">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bec3c-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bec3c-122">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bec3c-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bec3c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec3c-123">-DefaultProfile</span></span>
<span data-ttu-id="bec3c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bec3c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bec3c-125">-Id</span><span class="sxs-lookup"><span data-stu-id="bec3c-125">-Id</span></span>
<span data-ttu-id="bec3c-126">Определяет код пула, для которого этот cmdlet останавливает операцию.</span><span class="sxs-lookup"><span data-stu-id="bec3c-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="bec3c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec3c-127">CommonParameters</span></span>
<span data-ttu-id="bec3c-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec3c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec3c-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bec3c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec3c-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bec3c-130">INPUTS</span></span>

### <span data-ttu-id="bec3c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bec3c-131">System.String</span></span>

### <span data-ttu-id="bec3c-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bec3c-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bec3c-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bec3c-133">OUTPUTS</span></span>

### <span data-ttu-id="bec3c-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="bec3c-134">System.Void</span></span>

## <span data-ttu-id="bec3c-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bec3c-135">NOTES</span></span>

## <span data-ttu-id="bec3c-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bec3c-136">RELATED LINKS</span></span>

[<span data-ttu-id="bec3c-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="bec3c-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bec3c-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="bec3c-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="bec3c-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="bec3c-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="bec3c-140">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="bec3c-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
