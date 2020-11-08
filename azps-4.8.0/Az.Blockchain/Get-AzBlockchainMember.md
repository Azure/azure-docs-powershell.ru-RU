---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079162"
---
# <span data-ttu-id="898e0-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="898e0-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="898e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="898e0-102">SYNOPSIS</span></span>
<span data-ttu-id="898e0-103">Получение сведений о члене blockchain.</span><span class="sxs-lookup"><span data-stu-id="898e0-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="898e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="898e0-104">SYNTAX</span></span>

### <span data-ttu-id="898e0-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="898e0-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="898e0-106">Получить</span><span class="sxs-lookup"><span data-stu-id="898e0-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="898e0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="898e0-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="898e0-108">Список</span><span class="sxs-lookup"><span data-stu-id="898e0-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="898e0-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="898e0-109">DESCRIPTION</span></span>
<span data-ttu-id="898e0-110">Получение сведений о члене blockchain.</span><span class="sxs-lookup"><span data-stu-id="898e0-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="898e0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="898e0-111">EXAMPLES</span></span>

### <span data-ttu-id="898e0-112">Пример 1: список участников blockchain</span><span class="sxs-lookup"><span data-stu-id="898e0-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="898e0-113">Эта команда перечисляет пользователей blockchain в подписке.</span><span class="sxs-lookup"><span data-stu-id="898e0-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="898e0-114">Пример 2: List blockchain Members</span><span class="sxs-lookup"><span data-stu-id="898e0-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="898e0-115">Эта команда перечисляет пользователей blockchain в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="898e0-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="898e0-116">Пример 3: получение blockchain участника</span><span class="sxs-lookup"><span data-stu-id="898e0-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="898e0-117">Эта команда получает пользователя blockchain в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="898e0-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="898e0-118">Пример 4: получение blockchain участника</span><span class="sxs-lookup"><span data-stu-id="898e0-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="898e0-119">Эта команда получает пользователя blockchain в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="898e0-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="898e0-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="898e0-120">PARAMETERS</span></span>

### <span data-ttu-id="898e0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="898e0-121">-DefaultProfile</span></span>
<span data-ttu-id="898e0-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="898e0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="898e0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="898e0-123">-InputObject</span></span>
<span data-ttu-id="898e0-124">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="898e0-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="898e0-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="898e0-125">-Name</span></span>
<span data-ttu-id="898e0-126">Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="898e0-126">Blockchain member name.</span></span>

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

### <span data-ttu-id="898e0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="898e0-127">-ResourceGroupName</span></span>
<span data-ttu-id="898e0-128">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="898e0-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="898e0-129">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="898e0-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="898e0-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="898e0-130">-SubscriptionId</span></span>
<span data-ttu-id="898e0-131">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="898e0-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="898e0-132">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="898e0-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="898e0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="898e0-133">CommonParameters</span></span>
<span data-ttu-id="898e0-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="898e0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="898e0-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="898e0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="898e0-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="898e0-136">INPUTS</span></span>

### <span data-ttu-id="898e0-137">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="898e0-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="898e0-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="898e0-138">OUTPUTS</span></span>

### <span data-ttu-id="898e0-139">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="898e0-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="898e0-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="898e0-140">NOTES</span></span>

<span data-ttu-id="898e0-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="898e0-141">ALIASES</span></span>

<span data-ttu-id="898e0-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="898e0-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="898e0-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="898e0-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="898e0-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="898e0-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="898e0-145">INPUTOBJECT <IBlockchainIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="898e0-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="898e0-146">`[BlockchainMemberName <String>]`: Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="898e0-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="898e0-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="898e0-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="898e0-148">`[Location <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="898e0-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="898e0-149">`[OperationId <String>]`: ИД операции.</span><span class="sxs-lookup"><span data-stu-id="898e0-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="898e0-150">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="898e0-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="898e0-151">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="898e0-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="898e0-152">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="898e0-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="898e0-153">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="898e0-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="898e0-154">`[TransactionNodeName <String>]`: Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="898e0-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="898e0-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="898e0-155">RELATED LINKS</span></span>

