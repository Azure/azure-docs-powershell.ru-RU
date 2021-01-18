---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 575c2e8a7e510f3c8b3808b4ed6ce9169cd4f21f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509590"
---
# <span data-ttu-id="4fea9-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="4fea9-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="4fea9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fea9-102">SYNOPSIS</span></span>
<span data-ttu-id="4fea9-103">Удаляет указанный пакетный пул.</span><span class="sxs-lookup"><span data-stu-id="4fea9-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="4fea9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4fea9-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fea9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fea9-105">DESCRIPTION</span></span>
<span data-ttu-id="4fea9-106">С **использованием cmdlet Remove-AzBatchPool** удаляется указанный пул пакетов Azure.</span><span class="sxs-lookup"><span data-stu-id="4fea9-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="4fea9-107">Вам будет предложено подтвердить запрос, если вы не используете параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="4fea9-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="4fea9-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4fea9-108">EXAMPLES</span></span>

### <span data-ttu-id="4fea9-109">Пример 1. Удаление пакетного пула по ИД пула</span><span class="sxs-lookup"><span data-stu-id="4fea9-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="4fea9-110">Эта команда удаляет пул с помощью ID MyPool.</span><span class="sxs-lookup"><span data-stu-id="4fea9-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="4fea9-111">Перед удалением пользователю будет предложено подтвердить операцию.</span><span class="sxs-lookup"><span data-stu-id="4fea9-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="4fea9-112">Пример 2. Принудительное удаление всех пакетных пулов</span><span class="sxs-lookup"><span data-stu-id="4fea9-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="4fea9-113">Эта команда удаляет все пакетные пулы.</span><span class="sxs-lookup"><span data-stu-id="4fea9-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="4fea9-114">Так как параметр *Force* присутствует, запрос подтверждения подавляется.</span><span class="sxs-lookup"><span data-stu-id="4fea9-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="4fea9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fea9-115">PARAMETERS</span></span>

### <span data-ttu-id="4fea9-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4fea9-116">-BatchContext</span></span>
<span data-ttu-id="4fea9-117">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="4fea9-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4fea9-118">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4fea9-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4fea9-119">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="4fea9-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4fea9-120">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4fea9-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4fea9-121">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4fea9-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4fea9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fea9-122">-DefaultProfile</span></span>
<span data-ttu-id="4fea9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4fea9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fea9-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4fea9-124">-Force</span></span>
<span data-ttu-id="4fea9-125">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4fea9-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fea9-126">-Id</span><span class="sxs-lookup"><span data-stu-id="4fea9-126">-Id</span></span>
<span data-ttu-id="4fea9-127">Определяет ИД пула, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4fea9-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="4fea9-128">Поддиавные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="4fea9-128">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fea9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fea9-129">-Confirm</span></span>
<span data-ttu-id="4fea9-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fea9-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fea9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fea9-131">-WhatIf</span></span>
<span data-ttu-id="4fea9-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fea9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fea9-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4fea9-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fea9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fea9-134">CommonParameters</span></span>
<span data-ttu-id="4fea9-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fea9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fea9-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fea9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fea9-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fea9-137">INPUTS</span></span>

### <span data-ttu-id="4fea9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4fea9-138">System.String</span></span>

### <span data-ttu-id="4fea9-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4fea9-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4fea9-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4fea9-140">OUTPUTS</span></span>

### <span data-ttu-id="4fea9-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="4fea9-141">System.Void</span></span>

## <span data-ttu-id="4fea9-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4fea9-142">NOTES</span></span>

## <span data-ttu-id="4fea9-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fea9-143">RELATED LINKS</span></span>

[<span data-ttu-id="4fea9-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4fea9-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4fea9-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="4fea9-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="4fea9-146">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="4fea9-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="4fea9-147">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="4fea9-147">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
