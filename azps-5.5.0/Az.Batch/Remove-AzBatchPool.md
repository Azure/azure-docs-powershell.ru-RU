---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 575c2e8a7e510f3c8b3808b4ed6ce9169cd4f21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233596"
---
# <span data-ttu-id="0906e-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="0906e-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="0906e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0906e-102">SYNOPSIS</span></span>
<span data-ttu-id="0906e-103">Удаляет указанный пакетный пул.</span><span class="sxs-lookup"><span data-stu-id="0906e-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="0906e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0906e-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0906e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0906e-105">DESCRIPTION</span></span>
<span data-ttu-id="0906e-106">С **использованием cmdlet Remove-AzBatchPool** удаляется указанный пул пакетов Azure.</span><span class="sxs-lookup"><span data-stu-id="0906e-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="0906e-107">Вам будет предложено подтвердить запрос, если вы не используете параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="0906e-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="0906e-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0906e-108">EXAMPLES</span></span>

### <span data-ttu-id="0906e-109">Пример 1. Удаление пакетного пула по ИД пула</span><span class="sxs-lookup"><span data-stu-id="0906e-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="0906e-110">Эта команда удаляет пул с помощью ID MyPool.</span><span class="sxs-lookup"><span data-stu-id="0906e-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="0906e-111">Перед удалением пользователю будет предложено подтвердить операцию.</span><span class="sxs-lookup"><span data-stu-id="0906e-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="0906e-112">Пример 2. Принудительное удаление всех пакетных пулов</span><span class="sxs-lookup"><span data-stu-id="0906e-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="0906e-113">Эта команда удаляет все пакетные пулы.</span><span class="sxs-lookup"><span data-stu-id="0906e-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="0906e-114">Так как параметр *Force* присутствует, запрос подтверждения подавляется.</span><span class="sxs-lookup"><span data-stu-id="0906e-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="0906e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0906e-115">PARAMETERS</span></span>

### <span data-ttu-id="0906e-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0906e-116">-BatchContext</span></span>
<span data-ttu-id="0906e-117">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="0906e-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0906e-118">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0906e-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0906e-119">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="0906e-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0906e-120">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0906e-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0906e-121">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0906e-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0906e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0906e-122">-DefaultProfile</span></span>
<span data-ttu-id="0906e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0906e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0906e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0906e-124">-Force</span></span>
<span data-ttu-id="0906e-125">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0906e-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0906e-126">-Id</span><span class="sxs-lookup"><span data-stu-id="0906e-126">-Id</span></span>
<span data-ttu-id="0906e-127">Определяет ИД пула, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="0906e-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="0906e-128">Поддиавные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="0906e-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="0906e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0906e-129">-Confirm</span></span>
<span data-ttu-id="0906e-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0906e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0906e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0906e-131">-WhatIf</span></span>
<span data-ttu-id="0906e-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0906e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0906e-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0906e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0906e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0906e-134">CommonParameters</span></span>
<span data-ttu-id="0906e-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0906e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0906e-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0906e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0906e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0906e-137">INPUTS</span></span>

### <span data-ttu-id="0906e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0906e-138">System.String</span></span>

### <span data-ttu-id="0906e-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0906e-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0906e-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0906e-140">OUTPUTS</span></span>

### <span data-ttu-id="0906e-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="0906e-141">System.Void</span></span>

## <span data-ttu-id="0906e-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0906e-142">NOTES</span></span>

## <span data-ttu-id="0906e-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0906e-143">RELATED LINKS</span></span>

[<span data-ttu-id="0906e-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0906e-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0906e-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="0906e-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="0906e-146">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="0906e-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="0906e-147">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="0906e-147">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
