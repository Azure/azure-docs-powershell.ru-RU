---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316745"
---
# <span data-ttu-id="d4087-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="d4087-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="d4087-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4087-102">SYNOPSIS</span></span>
<span data-ttu-id="d4087-103">Повторно создайте ключи API для элемента blockchain.</span><span class="sxs-lookup"><span data-stu-id="d4087-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="d4087-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4087-104">SYNTAX</span></span>

### <span data-ttu-id="d4087-105">RegenerateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4087-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d4087-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d4087-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d4087-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4087-107">DESCRIPTION</span></span>
<span data-ttu-id="d4087-108">Повторно создайте ключи API для элемента blockchain.</span><span class="sxs-lookup"><span data-stu-id="d4087-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="d4087-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4087-109">EXAMPLES</span></span>

### <span data-ttu-id="d4087-110">Пример 1: повторное создание ключей API для элемента blockchain с помощью Name</span><span class="sxs-lookup"><span data-stu-id="d4087-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="d4087-111">Эта команда повторно создает ключи API для элемента blockchain с помощью имени, группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4087-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="d4087-112">Пример 2: повторное создание ключей API для элемента blockchain с помощью idenity</span><span class="sxs-lookup"><span data-stu-id="d4087-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="d4087-113">Эта команда повторно создает ключи API для элемента blockchain с помощью удостоверения.</span><span class="sxs-lookup"><span data-stu-id="d4087-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="d4087-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4087-114">PARAMETERS</span></span>

### <span data-ttu-id="d4087-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="d4087-115">-BlockchainMemberName</span></span>
<span data-ttu-id="d4087-116">Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="d4087-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="d4087-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4087-117">-DefaultProfile</span></span>
<span data-ttu-id="d4087-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4087-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4087-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4087-119">-InputObject</span></span>
<span data-ttu-id="d4087-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d4087-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d4087-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d4087-121">-KeyName</span></span>
<span data-ttu-id="d4087-122">Возвращает или задает имя ключа API.</span><span class="sxs-lookup"><span data-stu-id="d4087-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="d4087-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4087-123">-ResourceGroupName</span></span>
<span data-ttu-id="d4087-124">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="d4087-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d4087-125">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d4087-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d4087-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4087-126">-SubscriptionId</span></span>
<span data-ttu-id="d4087-127">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d4087-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d4087-128">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d4087-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d4087-129">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="d4087-129">-Value</span></span>
<span data-ttu-id="d4087-130">Возвращает или задает значение ключа API.</span><span class="sxs-lookup"><span data-stu-id="d4087-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="d4087-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4087-131">-Confirm</span></span>
<span data-ttu-id="d4087-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d4087-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4087-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4087-133">-WhatIf</span></span>
<span data-ttu-id="d4087-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d4087-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4087-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d4087-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4087-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4087-136">CommonParameters</span></span>
<span data-ttu-id="d4087-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4087-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4087-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4087-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4087-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4087-139">INPUTS</span></span>

### <span data-ttu-id="d4087-140">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="d4087-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="d4087-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4087-141">OUTPUTS</span></span>

### <span data-ttu-id="d4087-142">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="d4087-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="d4087-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4087-143">NOTES</span></span>

<span data-ttu-id="d4087-144">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d4087-144">ALIASES</span></span>

<span data-ttu-id="d4087-145">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d4087-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4087-146">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d4087-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4087-147">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d4087-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4087-148">INPUTOBJECT <IBlockchainIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d4087-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4087-149">`[BlockchainMemberName <String>]`: Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="d4087-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="d4087-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d4087-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4087-151">`[Location <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="d4087-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="d4087-152">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="d4087-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="d4087-153">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="d4087-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d4087-154">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d4087-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d4087-155">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d4087-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="d4087-156">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d4087-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="d4087-157">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="d4087-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="d4087-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4087-158">RELATED LINKS</span></span>

