---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: 3de49353a19afbce6ed8996fc5dd7cdeccca1627
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992914"
---
# <span data-ttu-id="8377d-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="8377d-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="8377d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8377d-102">SYNOPSIS</span></span>
<span data-ttu-id="8377d-103">Удалите узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="8377d-103">Delete the transaction node.</span></span>

## <span data-ttu-id="8377d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8377d-104">SYNTAX</span></span>

### <span data-ttu-id="8377d-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8377d-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8377d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8377d-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8377d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8377d-107">DESCRIPTION</span></span>
<span data-ttu-id="8377d-108">Удалите узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="8377d-108">Delete the transaction node.</span></span>

## <span data-ttu-id="8377d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8377d-109">EXAMPLES</span></span>

### <span data-ttu-id="8377d-110">Пример 1. Удаление узла транзакции</span><span class="sxs-lookup"><span data-stu-id="8377d-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="8377d-111">Эта команда удаляет узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="8377d-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="8377d-112">Пример 2. Удаление узла транзакции</span><span class="sxs-lookup"><span data-stu-id="8377d-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="8377d-113">Эта команда удаляет узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="8377d-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="8377d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8377d-114">PARAMETERS</span></span>

### <span data-ttu-id="8377d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8377d-115">-AsJob</span></span>
<span data-ttu-id="8377d-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="8377d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8377d-117">-ЛесОИмяноИмя</span><span class="sxs-lookup"><span data-stu-id="8377d-117">-BlockchainMemberName</span></span>
<span data-ttu-id="8377d-118">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="8377d-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="8377d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8377d-119">-DefaultProfile</span></span>
<span data-ttu-id="8377d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8377d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8377d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8377d-121">-InputObject</span></span>
<span data-ttu-id="8377d-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="8377d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8377d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8377d-123">-Name</span></span>
<span data-ttu-id="8377d-124">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="8377d-124">Transaction node name.</span></span>

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

### <span data-ttu-id="8377d-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8377d-125">-NoWait</span></span>
<span data-ttu-id="8377d-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="8377d-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8377d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8377d-127">-PassThru</span></span>
<span data-ttu-id="8377d-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="8377d-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8377d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8377d-129">-ResourceGroupName</span></span>
<span data-ttu-id="8377d-130">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="8377d-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8377d-131">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="8377d-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8377d-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8377d-132">-SubscriptionId</span></span>
<span data-ttu-id="8377d-133">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8377d-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8377d-134">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="8377d-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8377d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8377d-135">-Confirm</span></span>
<span data-ttu-id="8377d-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8377d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8377d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8377d-137">-WhatIf</span></span>
<span data-ttu-id="8377d-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8377d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8377d-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8377d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8377d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8377d-140">CommonParameters</span></span>
<span data-ttu-id="8377d-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8377d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8377d-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8377d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8377d-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8377d-143">INPUTS</span></span>

### <span data-ttu-id="8377d-144">Microsoft.Azure.PowerShell.Cmdlets.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="8377d-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="8377d-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8377d-145">OUTPUTS</span></span>

### <span data-ttu-id="8377d-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8377d-146">System.Boolean</span></span>

## <span data-ttu-id="8377d-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8377d-147">NOTES</span></span>

<span data-ttu-id="8377d-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8377d-148">ALIASES</span></span>

<span data-ttu-id="8377d-149">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="8377d-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8377d-150">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="8377d-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8377d-151">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8377d-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8377d-152">INPUTOBJECT <IBlockchainIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="8377d-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8377d-153">`[BlockchainMemberName <String>]`: Имя участника.</span><span class="sxs-lookup"><span data-stu-id="8377d-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="8377d-154">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="8377d-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8377d-155">`[Location <String>]`: имя расположения.</span><span class="sxs-lookup"><span data-stu-id="8377d-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="8377d-156">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="8377d-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="8377d-157">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="8377d-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8377d-158">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="8377d-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8377d-159">`[SubscriptionId <String>]`: получает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8377d-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="8377d-160">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="8377d-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="8377d-161">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="8377d-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="8377d-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8377d-162">RELATED LINKS</span></span>

