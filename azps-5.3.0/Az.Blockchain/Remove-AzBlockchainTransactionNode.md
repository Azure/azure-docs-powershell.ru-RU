---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509470"
---
# <span data-ttu-id="49f92-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="49f92-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="49f92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49f92-102">SYNOPSIS</span></span>
<span data-ttu-id="49f92-103">Удалите узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="49f92-103">Delete the transaction node.</span></span>

## <span data-ttu-id="49f92-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49f92-104">SYNTAX</span></span>

### <span data-ttu-id="49f92-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49f92-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="49f92-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49f92-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="49f92-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49f92-107">DESCRIPTION</span></span>
<span data-ttu-id="49f92-108">Удалите узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="49f92-108">Delete the transaction node.</span></span>

## <span data-ttu-id="49f92-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49f92-109">EXAMPLES</span></span>

### <span data-ttu-id="49f92-110">Пример 1. Удаление узла транзакции</span><span class="sxs-lookup"><span data-stu-id="49f92-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="49f92-111">Эта команда удаляет узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="49f92-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="49f92-112">Пример 2. Удаление узла транзакции</span><span class="sxs-lookup"><span data-stu-id="49f92-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="49f92-113">Эта команда удаляет узел транзакции.</span><span class="sxs-lookup"><span data-stu-id="49f92-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="49f92-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49f92-114">PARAMETERS</span></span>

### <span data-ttu-id="49f92-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49f92-115">-AsJob</span></span>
<span data-ttu-id="49f92-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="49f92-116">Run the command as a job</span></span>

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

### <span data-ttu-id="49f92-117">-ДолжныеИмяЯ</span><span class="sxs-lookup"><span data-stu-id="49f92-117">-BlockchainMemberName</span></span>
<span data-ttu-id="49f92-118">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="49f92-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="49f92-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f92-119">-DefaultProfile</span></span>
<span data-ttu-id="49f92-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49f92-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49f92-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49f92-121">-InputObject</span></span>
<span data-ttu-id="49f92-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="49f92-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="49f92-123">-Name</span><span class="sxs-lookup"><span data-stu-id="49f92-123">-Name</span></span>
<span data-ttu-id="49f92-124">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="49f92-124">Transaction node name.</span></span>

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

### <span data-ttu-id="49f92-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="49f92-125">-NoWait</span></span>
<span data-ttu-id="49f92-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="49f92-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="49f92-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49f92-127">-PassThru</span></span>
<span data-ttu-id="49f92-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="49f92-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="49f92-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f92-129">-ResourceGroupName</span></span>
<span data-ttu-id="49f92-130">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="49f92-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="49f92-131">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="49f92-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="49f92-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49f92-132">-SubscriptionId</span></span>
<span data-ttu-id="49f92-133">Возвращает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="49f92-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="49f92-134">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="49f92-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="49f92-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49f92-135">-Confirm</span></span>
<span data-ttu-id="49f92-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49f92-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49f92-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49f92-137">-WhatIf</span></span>
<span data-ttu-id="49f92-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49f92-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49f92-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="49f92-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49f92-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f92-140">CommonParameters</span></span>
<span data-ttu-id="49f92-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49f92-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f92-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49f92-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f92-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49f92-143">INPUTS</span></span>

### <span data-ttu-id="49f92-144">Microsoft.Azure.PowerShell.Cmdlets.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="49f92-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="49f92-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49f92-145">OUTPUTS</span></span>

### <span data-ttu-id="49f92-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49f92-146">System.Boolean</span></span>

## <span data-ttu-id="49f92-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49f92-147">NOTES</span></span>

<span data-ttu-id="49f92-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="49f92-148">ALIASES</span></span>

<span data-ttu-id="49f92-149">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="49f92-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49f92-150">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="49f92-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49f92-151">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49f92-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49f92-152">INPUTOBJECT <IBlockchainIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="49f92-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49f92-153">`[BlockchainMemberName <String>]`: Имя участника.</span><span class="sxs-lookup"><span data-stu-id="49f92-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="49f92-154">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="49f92-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49f92-155">`[Location <String>]`: имя расположения.</span><span class="sxs-lookup"><span data-stu-id="49f92-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="49f92-156">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="49f92-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="49f92-157">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="49f92-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="49f92-158">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="49f92-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="49f92-159">`[SubscriptionId <String>]`: получает идентификатор подписки, однозначно определяя подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="49f92-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="49f92-160">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="49f92-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="49f92-161">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="49f92-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="49f92-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49f92-162">RELATED LINKS</span></span>

