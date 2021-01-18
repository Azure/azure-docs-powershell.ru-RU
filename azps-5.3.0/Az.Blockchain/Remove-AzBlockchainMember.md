---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519751"
---
# <span data-ttu-id="b9327-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="b9327-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="b9327-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9327-102">SYNOPSIS</span></span>
<span data-ttu-id="b9327-103">Удалите участника-участника.</span><span class="sxs-lookup"><span data-stu-id="b9327-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="b9327-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b9327-104">SYNTAX</span></span>

### <span data-ttu-id="b9327-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9327-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b9327-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b9327-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b9327-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9327-107">DESCRIPTION</span></span>
<span data-ttu-id="b9327-108">Удалите участника-участника.</span><span class="sxs-lookup"><span data-stu-id="b9327-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="b9327-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b9327-109">EXAMPLES</span></span>

### <span data-ttu-id="b9327-110">Пример 1. Удаление участника-участника</span><span class="sxs-lookup"><span data-stu-id="b9327-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="b9327-111">Эта команда удаляет участника-участника.</span><span class="sxs-lookup"><span data-stu-id="b9327-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="b9327-112">Пример 2. Удаление участника группы</span><span class="sxs-lookup"><span data-stu-id="b9327-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="b9327-113">Эта команда удаляет участника-участника.</span><span class="sxs-lookup"><span data-stu-id="b9327-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="b9327-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9327-114">PARAMETERS</span></span>

### <span data-ttu-id="b9327-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9327-115">-AsJob</span></span>
<span data-ttu-id="b9327-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="b9327-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b9327-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9327-117">-DefaultProfile</span></span>
<span data-ttu-id="b9327-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9327-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9327-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9327-119">-InputObject</span></span>
<span data-ttu-id="b9327-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b9327-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b9327-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b9327-121">-Name</span></span>
<span data-ttu-id="b9327-122">Имя участника Группы</span><span class="sxs-lookup"><span data-stu-id="b9327-122">Blockchain member name</span></span>

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

### <span data-ttu-id="b9327-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b9327-123">-NoWait</span></span>
<span data-ttu-id="b9327-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="b9327-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b9327-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9327-125">-PassThru</span></span>
<span data-ttu-id="b9327-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="b9327-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b9327-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9327-127">-ResourceGroupName</span></span>
<span data-ttu-id="b9327-128">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="b9327-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b9327-129">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="b9327-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b9327-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9327-130">-SubscriptionId</span></span>
<span data-ttu-id="b9327-131">Возвращает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b9327-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b9327-132">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b9327-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b9327-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9327-133">-Confirm</span></span>
<span data-ttu-id="b9327-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9327-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9327-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9327-135">-WhatIf</span></span>
<span data-ttu-id="b9327-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9327-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9327-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b9327-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9327-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9327-138">CommonParameters</span></span>
<span data-ttu-id="b9327-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9327-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9327-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9327-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9327-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9327-141">INPUTS</span></span>

### <span data-ttu-id="b9327-142">Microsoft.Azure.PowerShell.Cmdlets.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="b9327-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="b9327-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9327-143">OUTPUTS</span></span>

### <span data-ttu-id="b9327-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b9327-144">System.Boolean</span></span>

## <span data-ttu-id="b9327-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b9327-145">NOTES</span></span>

<span data-ttu-id="b9327-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b9327-146">ALIASES</span></span>

<span data-ttu-id="b9327-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b9327-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9327-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b9327-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9327-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b9327-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9327-150">INPUTOBJECT <IBlockchainIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="b9327-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b9327-151">`[BlockchainMemberName <String>]`: Имя участника.</span><span class="sxs-lookup"><span data-stu-id="b9327-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="b9327-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="b9327-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b9327-153">`[Location <String>]`: имя расположения.</span><span class="sxs-lookup"><span data-stu-id="b9327-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="b9327-154">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="b9327-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="b9327-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="b9327-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b9327-156">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="b9327-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b9327-157">`[SubscriptionId <String>]`: получает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b9327-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="b9327-158">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b9327-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="b9327-159">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="b9327-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="b9327-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9327-160">RELATED LINKS</span></span>

