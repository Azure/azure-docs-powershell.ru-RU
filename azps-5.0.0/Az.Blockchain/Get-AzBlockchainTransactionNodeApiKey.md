---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 401073a8d97affaec866486b19113373c001ae58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249546"
---
# <span data-ttu-id="ae172-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="ae172-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="ae172-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae172-102">SYNOPSIS</span></span>
<span data-ttu-id="ae172-103">Перечислите ключи API для узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="ae172-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="ae172-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae172-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ae172-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae172-105">DESCRIPTION</span></span>
<span data-ttu-id="ae172-106">Перечислите ключи API для узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="ae172-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="ae172-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae172-107">EXAMPLES</span></span>

### <span data-ttu-id="ae172-108">Пример 1: список ключей API для узла транзакции</span><span class="sxs-lookup"><span data-stu-id="ae172-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="ae172-109">Эта команда перечисляет ключи API для узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="ae172-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="ae172-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae172-110">PARAMETERS</span></span>

### <span data-ttu-id="ae172-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="ae172-111">-BlockchainMemberName</span></span>
<span data-ttu-id="ae172-112">Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="ae172-112">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae172-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae172-113">-DefaultProfile</span></span>
<span data-ttu-id="ae172-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae172-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae172-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae172-115">-ResourceGroupName</span></span>
<span data-ttu-id="ae172-116">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="ae172-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ae172-117">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="ae172-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae172-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae172-118">-SubscriptionId</span></span>
<span data-ttu-id="ae172-119">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ae172-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ae172-120">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ae172-120">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae172-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="ae172-121">-TransactionNodeName</span></span>
<span data-ttu-id="ae172-122">Имя узла транзакции.</span><span class="sxs-lookup"><span data-stu-id="ae172-122">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae172-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae172-123">-Confirm</span></span>
<span data-ttu-id="ae172-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ae172-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae172-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae172-125">-WhatIf</span></span>
<span data-ttu-id="ae172-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ae172-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae172-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ae172-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae172-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae172-128">CommonParameters</span></span>
<span data-ttu-id="ae172-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae172-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae172-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae172-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae172-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae172-131">INPUTS</span></span>

## <span data-ttu-id="ae172-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae172-132">OUTPUTS</span></span>

### <span data-ttu-id="ae172-133">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="ae172-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="ae172-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae172-134">NOTES</span></span>

<span data-ttu-id="ae172-135">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="ae172-135">ALIASES</span></span>

## <span data-ttu-id="ae172-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae172-136">RELATED LINKS</span></span>

