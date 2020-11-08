---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249558"
---
# <span data-ttu-id="7d31e-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="7d31e-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="7d31e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d31e-102">SYNOPSIS</span></span>
<span data-ttu-id="7d31e-103">Получение сведений о члене blockchain.</span><span class="sxs-lookup"><span data-stu-id="7d31e-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="7d31e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d31e-104">SYNTAX</span></span>

### <span data-ttu-id="7d31e-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d31e-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7d31e-106">Получить</span><span class="sxs-lookup"><span data-stu-id="7d31e-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7d31e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7d31e-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7d31e-108">Список</span><span class="sxs-lookup"><span data-stu-id="7d31e-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d31e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d31e-109">DESCRIPTION</span></span>
<span data-ttu-id="7d31e-110">Получение сведений о члене blockchain.</span><span class="sxs-lookup"><span data-stu-id="7d31e-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="7d31e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d31e-111">EXAMPLES</span></span>

### <span data-ttu-id="7d31e-112">Пример 1: список участников blockchain</span><span class="sxs-lookup"><span data-stu-id="7d31e-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="7d31e-113">Эта команда перечисляет пользователей blockchain в подписке.</span><span class="sxs-lookup"><span data-stu-id="7d31e-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="7d31e-114">Пример 2: List blockchain Members</span><span class="sxs-lookup"><span data-stu-id="7d31e-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="7d31e-115">Эта команда перечисляет пользователей blockchain в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d31e-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="7d31e-116">Пример 3: получение blockchain участника</span><span class="sxs-lookup"><span data-stu-id="7d31e-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="7d31e-117">Эта команда получает пользователя blockchain в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d31e-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="7d31e-118">Пример 4: получение blockchain участника</span><span class="sxs-lookup"><span data-stu-id="7d31e-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="7d31e-119">Эта команда получает пользователя blockchain в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d31e-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="7d31e-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d31e-120">PARAMETERS</span></span>

### <span data-ttu-id="7d31e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d31e-121">-DefaultProfile</span></span>
<span data-ttu-id="7d31e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d31e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d31e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d31e-123">-InputObject</span></span>
<span data-ttu-id="7d31e-124">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="7d31e-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d31e-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d31e-125">-Name</span></span>
<span data-ttu-id="7d31e-126">Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="7d31e-126">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d31e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d31e-127">-ResourceGroupName</span></span>
<span data-ttu-id="7d31e-128">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="7d31e-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7d31e-129">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="7d31e-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d31e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d31e-130">-SubscriptionId</span></span>
<span data-ttu-id="7d31e-131">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7d31e-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7d31e-132">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="7d31e-132">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d31e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d31e-133">CommonParameters</span></span>
<span data-ttu-id="7d31e-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d31e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d31e-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d31e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d31e-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d31e-136">INPUTS</span></span>

### <span data-ttu-id="7d31e-137">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="7d31e-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="7d31e-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d31e-138">OUTPUTS</span></span>

### <span data-ttu-id="7d31e-139">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="7d31e-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="7d31e-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d31e-140">NOTES</span></span>

<span data-ttu-id="7d31e-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="7d31e-141">ALIASES</span></span>

<span data-ttu-id="7d31e-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="7d31e-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7d31e-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7d31e-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7d31e-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7d31e-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7d31e-145">INPUTOBJECT <IBlockchainIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="7d31e-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7d31e-146">`[BlockchainMemberName <String>]`: Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="7d31e-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="7d31e-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="7d31e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7d31e-148">`[Location <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="7d31e-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="7d31e-149">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="7d31e-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="7d31e-150">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="7d31e-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7d31e-151">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="7d31e-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7d31e-152">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7d31e-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="7d31e-153">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="7d31e-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="7d31e-154">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="7d31e-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="7d31e-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d31e-155">RELATED LINKS</span></span>

