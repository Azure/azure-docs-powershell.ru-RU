---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079156"
---
# <span data-ttu-id="044f2-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="044f2-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="044f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="044f2-102">SYNOPSIS</span></span>
<span data-ttu-id="044f2-103">Удаление blockchain участника.</span><span class="sxs-lookup"><span data-stu-id="044f2-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="044f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="044f2-104">SYNTAX</span></span>

### <span data-ttu-id="044f2-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="044f2-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="044f2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="044f2-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="044f2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="044f2-107">DESCRIPTION</span></span>
<span data-ttu-id="044f2-108">Удаление blockchain участника.</span><span class="sxs-lookup"><span data-stu-id="044f2-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="044f2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="044f2-109">EXAMPLES</span></span>

### <span data-ttu-id="044f2-110">Пример 1: удаление blockchain участника</span><span class="sxs-lookup"><span data-stu-id="044f2-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="044f2-111">Эта команда удаляет blockchain участника.</span><span class="sxs-lookup"><span data-stu-id="044f2-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="044f2-112">Пример 2: удаление blockchain участника</span><span class="sxs-lookup"><span data-stu-id="044f2-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="044f2-113">Эта команда удаляет blockchain участника.</span><span class="sxs-lookup"><span data-stu-id="044f2-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="044f2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="044f2-114">PARAMETERS</span></span>

### <span data-ttu-id="044f2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="044f2-115">-AsJob</span></span>
<span data-ttu-id="044f2-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="044f2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="044f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="044f2-117">-DefaultProfile</span></span>
<span data-ttu-id="044f2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="044f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="044f2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="044f2-119">-InputObject</span></span>
<span data-ttu-id="044f2-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="044f2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="044f2-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="044f2-121">-Name</span></span>
<span data-ttu-id="044f2-122">Имя участника Blockchain</span><span class="sxs-lookup"><span data-stu-id="044f2-122">Blockchain member name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044f2-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="044f2-123">-NoWait</span></span>
<span data-ttu-id="044f2-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="044f2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="044f2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="044f2-125">-PassThru</span></span>
<span data-ttu-id="044f2-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="044f2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="044f2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="044f2-127">-ResourceGroupName</span></span>
<span data-ttu-id="044f2-128">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="044f2-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="044f2-129">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="044f2-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="044f2-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="044f2-130">-SubscriptionId</span></span>
<span data-ttu-id="044f2-131">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="044f2-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="044f2-132">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="044f2-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="044f2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="044f2-133">-Confirm</span></span>
<span data-ttu-id="044f2-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="044f2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="044f2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="044f2-135">-WhatIf</span></span>
<span data-ttu-id="044f2-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="044f2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="044f2-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="044f2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="044f2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044f2-138">CommonParameters</span></span>
<span data-ttu-id="044f2-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="044f2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044f2-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="044f2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044f2-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="044f2-141">INPUTS</span></span>

### <span data-ttu-id="044f2-142">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="044f2-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="044f2-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="044f2-143">OUTPUTS</span></span>

### <span data-ttu-id="044f2-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="044f2-144">System.Boolean</span></span>

## <span data-ttu-id="044f2-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="044f2-145">NOTES</span></span>

<span data-ttu-id="044f2-146">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="044f2-146">ALIASES</span></span>

<span data-ttu-id="044f2-147">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="044f2-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="044f2-148">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="044f2-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="044f2-149">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="044f2-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="044f2-150">INPUTOBJECT <IBlockchainIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="044f2-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="044f2-151">`[BlockchainMemberName <String>]`: Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="044f2-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="044f2-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="044f2-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="044f2-153">`[Location <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="044f2-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="044f2-154">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="044f2-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="044f2-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="044f2-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="044f2-156">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="044f2-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="044f2-157">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="044f2-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="044f2-158">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="044f2-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="044f2-159">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="044f2-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="044f2-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="044f2-160">RELATED LINKS</span></span>

