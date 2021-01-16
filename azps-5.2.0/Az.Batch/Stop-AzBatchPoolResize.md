---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 229877db7a3077a4b1951a06914c842e63384ba6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409092"
---
# <span data-ttu-id="eecfa-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="eecfa-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="eecfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eecfa-102">SYNOPSIS</span></span>
<span data-ttu-id="eecfa-103">Остановка операции по окнам пула.</span><span class="sxs-lookup"><span data-stu-id="eecfa-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="eecfa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eecfa-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eecfa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eecfa-105">DESCRIPTION</span></span>
<span data-ttu-id="eecfa-106">Для остановки операции обработки пула пакетов Azure операция **stop-AzBatchPoolResize** прекращается.</span><span class="sxs-lookup"><span data-stu-id="eecfa-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="eecfa-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eecfa-107">EXAMPLES</span></span>

### <span data-ttu-id="eecfa-108">Пример 1. Остановка resizing a pool</span><span class="sxs-lookup"><span data-stu-id="eecfa-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="eecfa-109">Эта команда останавливает операцию resize пула с ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="eecfa-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="eecfa-110">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="eecfa-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="eecfa-111">Пример 2. Остановка повторного использования пула с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="eecfa-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="eecfa-112">Эта команда прекращает размер пула с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="eecfa-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="eecfa-113">Команда получает пул с ИД ContosoPool06 с помощью Get-AzBatchPool командлета.</span><span class="sxs-lookup"><span data-stu-id="eecfa-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="eecfa-114">Эта команда передает объект пула текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="eecfa-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="eecfa-115">Команда останавливает операцию по окнованию пула.</span><span class="sxs-lookup"><span data-stu-id="eecfa-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="eecfa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eecfa-116">PARAMETERS</span></span>

### <span data-ttu-id="eecfa-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="eecfa-117">-BatchContext</span></span>
<span data-ttu-id="eecfa-118">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="eecfa-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eecfa-119">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="eecfa-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="eecfa-120">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="eecfa-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="eecfa-121">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eecfa-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="eecfa-122">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="eecfa-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="eecfa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eecfa-123">-DefaultProfile</span></span>
<span data-ttu-id="eecfa-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eecfa-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eecfa-125">-Id</span><span class="sxs-lookup"><span data-stu-id="eecfa-125">-Id</span></span>
<span data-ttu-id="eecfa-126">Определяет код пула, для которого этот cmdlet останавливает операцию.</span><span class="sxs-lookup"><span data-stu-id="eecfa-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="eecfa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eecfa-127">CommonParameters</span></span>
<span data-ttu-id="eecfa-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eecfa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eecfa-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eecfa-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eecfa-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eecfa-130">INPUTS</span></span>

### <span data-ttu-id="eecfa-131">System.String</span><span class="sxs-lookup"><span data-stu-id="eecfa-131">System.String</span></span>

### <span data-ttu-id="eecfa-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eecfa-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="eecfa-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eecfa-133">OUTPUTS</span></span>

### <span data-ttu-id="eecfa-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="eecfa-134">System.Void</span></span>

## <span data-ttu-id="eecfa-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eecfa-135">NOTES</span></span>

## <span data-ttu-id="eecfa-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eecfa-136">RELATED LINKS</span></span>

[<span data-ttu-id="eecfa-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="eecfa-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="eecfa-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="eecfa-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="eecfa-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="eecfa-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="eecfa-140">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="eecfa-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)