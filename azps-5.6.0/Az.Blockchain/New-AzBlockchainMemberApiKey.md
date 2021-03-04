---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 77b4d7800d556fc43aee4e47ebc243d006a0f484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954883"
---
# <span data-ttu-id="47892-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="47892-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="47892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47892-102">SYNOPSIS</span></span>
<span data-ttu-id="47892-103">Повторно сгенерировать ключи API для участника aPI.</span><span class="sxs-lookup"><span data-stu-id="47892-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="47892-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47892-104">SYNTAX</span></span>

### <span data-ttu-id="47892-105">RegenerateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47892-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="47892-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="47892-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47892-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47892-107">DESCRIPTION</span></span>
<span data-ttu-id="47892-108">Повторно сгенерировать ключи API для участника aPI.</span><span class="sxs-lookup"><span data-stu-id="47892-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="47892-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47892-109">EXAMPLES</span></span>

### <span data-ttu-id="47892-110">Пример 1. Повторное сгенерировать клавиши API для участника группы с использованием имени</span><span class="sxs-lookup"><span data-stu-id="47892-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="47892-111">Эта команда повторно сгенерирует ключи API для участника, используя имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47892-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="47892-112">Пример 2. Повторное сгенерировать клавиши API для участника группы с использованием idenity</span><span class="sxs-lookup"><span data-stu-id="47892-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="47892-113">Эта команда повторно сгенерирует клавиши API для участника группы с использованием удостоверения.</span><span class="sxs-lookup"><span data-stu-id="47892-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="47892-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47892-114">PARAMETERS</span></span>

### <span data-ttu-id="47892-115">-ДолжныеИмяЯ</span><span class="sxs-lookup"><span data-stu-id="47892-115">-BlockchainMemberName</span></span>
<span data-ttu-id="47892-116">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="47892-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47892-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47892-117">-DefaultProfile</span></span>
<span data-ttu-id="47892-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47892-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47892-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47892-119">-InputObject</span></span>
<span data-ttu-id="47892-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="47892-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47892-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="47892-121">-KeyName</span></span>
<span data-ttu-id="47892-122">Возвращает или задает имя ключа API.</span><span class="sxs-lookup"><span data-stu-id="47892-122">Gets or sets the API key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47892-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47892-123">-ResourceGroupName</span></span>
<span data-ttu-id="47892-124">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="47892-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="47892-125">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="47892-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47892-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47892-126">-SubscriptionId</span></span>
<span data-ttu-id="47892-127">Возвращает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="47892-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="47892-128">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="47892-128">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47892-129">-Value</span><span class="sxs-lookup"><span data-stu-id="47892-129">-Value</span></span>
<span data-ttu-id="47892-130">Возвращает или задает значение ключа API.</span><span class="sxs-lookup"><span data-stu-id="47892-130">Gets or sets the API key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47892-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47892-131">-Confirm</span></span>
<span data-ttu-id="47892-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47892-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47892-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47892-133">-WhatIf</span></span>
<span data-ttu-id="47892-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47892-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47892-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="47892-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47892-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47892-136">CommonParameters</span></span>
<span data-ttu-id="47892-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47892-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47892-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47892-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47892-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47892-139">INPUTS</span></span>

### <span data-ttu-id="47892-140">Microsoft.Azure.PowerShell.Cmdlets.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="47892-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="47892-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47892-141">OUTPUTS</span></span>

### <span data-ttu-id="47892-142">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="47892-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="47892-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47892-143">NOTES</span></span>

<span data-ttu-id="47892-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="47892-144">ALIASES</span></span>

<span data-ttu-id="47892-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="47892-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47892-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="47892-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47892-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47892-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47892-148">INPUTOBJECT <IBlockchainIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="47892-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47892-149">`[BlockchainMemberName <String>]`: Имя участника.</span><span class="sxs-lookup"><span data-stu-id="47892-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="47892-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="47892-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47892-151">`[Location <String>]`: имя расположения.</span><span class="sxs-lookup"><span data-stu-id="47892-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="47892-152">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="47892-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="47892-153">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="47892-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="47892-154">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="47892-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="47892-155">`[SubscriptionId <String>]`: получает идентификатор подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="47892-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="47892-156">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="47892-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="47892-157">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="47892-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="47892-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47892-158">RELATED LINKS</span></span>

