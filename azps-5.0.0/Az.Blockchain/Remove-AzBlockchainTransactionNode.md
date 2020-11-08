---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249101"
---
# <span data-ttu-id="d0850-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="d0850-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="d0850-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0850-102">SYNOPSIS</span></span>
<span data-ttu-id="d0850-103">Удалите узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="d0850-103">Delete the transaction node.</span></span>

## <span data-ttu-id="d0850-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0850-104">SYNTAX</span></span>

### <span data-ttu-id="d0850-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d0850-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d0850-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d0850-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d0850-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0850-107">DESCRIPTION</span></span>
<span data-ttu-id="d0850-108">Удалите узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="d0850-108">Delete the transaction node.</span></span>

## <span data-ttu-id="d0850-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0850-109">EXAMPLES</span></span>

### <span data-ttu-id="d0850-110">Пример 1: Удаление узла транзакции</span><span class="sxs-lookup"><span data-stu-id="d0850-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="d0850-111">Эта команда удаляет узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="d0850-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="d0850-112">Пример 2: Удаление узла транзакции</span><span class="sxs-lookup"><span data-stu-id="d0850-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="d0850-113">Эта команда удаляет узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="d0850-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="d0850-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0850-114">PARAMETERS</span></span>

### <span data-ttu-id="d0850-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0850-115">-AsJob</span></span>
<span data-ttu-id="d0850-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d0850-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d0850-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="d0850-117">-BlockchainMemberName</span></span>
<span data-ttu-id="d0850-118">Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="d0850-118">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0850-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0850-119">-DefaultProfile</span></span>
<span data-ttu-id="d0850-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0850-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0850-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0850-121">-InputObject</span></span>
<span data-ttu-id="d0850-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d0850-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0850-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d0850-123">-Name</span></span>
<span data-ttu-id="d0850-124">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="d0850-124">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0850-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="d0850-125">-NoWait</span></span>
<span data-ttu-id="d0850-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="d0850-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d0850-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0850-127">-PassThru</span></span>
<span data-ttu-id="d0850-128">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d0850-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d0850-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0850-129">-ResourceGroupName</span></span>
<span data-ttu-id="d0850-130">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="d0850-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d0850-131">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d0850-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0850-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0850-132">-SubscriptionId</span></span>
<span data-ttu-id="d0850-133">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d0850-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d0850-134">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d0850-134">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0850-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0850-135">-Confirm</span></span>
<span data-ttu-id="d0850-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d0850-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0850-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0850-137">-WhatIf</span></span>
<span data-ttu-id="d0850-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0850-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0850-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0850-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0850-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0850-140">CommonParameters</span></span>
<span data-ttu-id="d0850-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0850-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0850-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0850-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0850-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0850-143">INPUTS</span></span>

### <span data-ttu-id="d0850-144">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="d0850-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="d0850-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0850-145">OUTPUTS</span></span>

### <span data-ttu-id="d0850-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0850-146">System.Boolean</span></span>

## <span data-ttu-id="d0850-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0850-147">NOTES</span></span>

<span data-ttu-id="d0850-148">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d0850-148">ALIASES</span></span>

<span data-ttu-id="d0850-149">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d0850-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d0850-150">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d0850-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d0850-151">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d0850-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d0850-152">INPUTOBJECT <IBlockchainIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d0850-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d0850-153">`[BlockchainMemberName <String>]`: Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="d0850-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="d0850-154">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d0850-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d0850-155">`[Location <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="d0850-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="d0850-156">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="d0850-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="d0850-157">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="d0850-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d0850-158">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d0850-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d0850-159">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d0850-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="d0850-160">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d0850-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="d0850-161">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="d0850-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="d0850-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0850-162">RELATED LINKS</span></span>

