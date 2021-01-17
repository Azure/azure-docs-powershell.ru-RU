---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 52fea755708645173a5f0f3429591a384ec63b01
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416759"
---
# <span data-ttu-id="4e7db-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="4e7db-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="4e7db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e7db-102">SYNOPSIS</span></span>
<span data-ttu-id="4e7db-103">Удаляет учетную запись пользователя из узла пакетных вычислений.</span><span class="sxs-lookup"><span data-stu-id="4e7db-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="4e7db-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e7db-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e7db-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e7db-105">DESCRIPTION</span></span>
<span data-ttu-id="4e7db-106">При **этом учетная** запись пользователя удаляется из узла обработки пакетных вычислений Azure.</span><span class="sxs-lookup"><span data-stu-id="4e7db-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="4e7db-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e7db-107">EXAMPLES</span></span>

### <span data-ttu-id="4e7db-108">Пример 1. Удаление пользователя из узла вычислений без подтверждения</span><span class="sxs-lookup"><span data-stu-id="4e7db-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="4e7db-109">Эта команда удаляет пользователя с именем User14 из узла вычислений с именем ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="4e7db-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="4e7db-110">Узел вычислений находится в пуле с именем Pool01.</span><span class="sxs-lookup"><span data-stu-id="4e7db-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="4e7db-111">Эта команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="4e7db-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="4e7db-112">Таким образом, команда не будет запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4e7db-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4e7db-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e7db-113">PARAMETERS</span></span>

### <span data-ttu-id="4e7db-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4e7db-114">-BatchContext</span></span>
<span data-ttu-id="4e7db-115">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="4e7db-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4e7db-116">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4e7db-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4e7db-117">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="4e7db-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4e7db-118">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4e7db-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4e7db-119">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4e7db-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4e7db-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="4e7db-120">-ComputeNodeId</span></span>
<span data-ttu-id="4e7db-121">Определяет код узла вычислений, на котором этот cmdlet удаляет учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="4e7db-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e7db-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e7db-122">-DefaultProfile</span></span>
<span data-ttu-id="4e7db-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e7db-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e7db-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4e7db-124">-Name</span></span>
<span data-ttu-id="4e7db-125">Указывает имя учетной записи пользователя, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4e7db-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="4e7db-126">Поддиавные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="4e7db-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e7db-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="4e7db-127">-PoolId</span></span>
<span data-ttu-id="4e7db-128">Определяет ИД пула, который содержит узел вычислений, на котором нужно удалить учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="4e7db-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="4e7db-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e7db-129">-Confirm</span></span>
<span data-ttu-id="4e7db-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4e7db-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e7db-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e7db-131">-WhatIf</span></span>
<span data-ttu-id="4e7db-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e7db-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e7db-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4e7db-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e7db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e7db-134">CommonParameters</span></span>
<span data-ttu-id="4e7db-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e7db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e7db-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e7db-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e7db-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e7db-137">INPUTS</span></span>

### <span data-ttu-id="4e7db-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4e7db-138">System.String</span></span>

### <span data-ttu-id="4e7db-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4e7db-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4e7db-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e7db-140">OUTPUTS</span></span>

### <span data-ttu-id="4e7db-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="4e7db-141">System.Void</span></span>

## <span data-ttu-id="4e7db-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e7db-142">NOTES</span></span>

## <span data-ttu-id="4e7db-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e7db-143">RELATED LINKS</span></span>

[<span data-ttu-id="4e7db-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="4e7db-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="4e7db-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4e7db-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4e7db-146">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="4e7db-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
