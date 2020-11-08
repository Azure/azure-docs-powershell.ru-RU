---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077901"
---
# <span data-ttu-id="df56d-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="df56d-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="df56d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df56d-102">SYNOPSIS</span></span>
<span data-ttu-id="df56d-103">Список ключей API для элемента blockchain.</span><span class="sxs-lookup"><span data-stu-id="df56d-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="df56d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df56d-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="df56d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df56d-105">DESCRIPTION</span></span>
<span data-ttu-id="df56d-106">Список ключей API для элемента blockchain.</span><span class="sxs-lookup"><span data-stu-id="df56d-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="df56d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df56d-107">EXAMPLES</span></span>

### <span data-ttu-id="df56d-108">Пример 1: список ключей API blockchain</span><span class="sxs-lookup"><span data-stu-id="df56d-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="df56d-109">Эта команда перечисляет ключи API для элемента blockchain.</span><span class="sxs-lookup"><span data-stu-id="df56d-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="df56d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df56d-110">PARAMETERS</span></span>

### <span data-ttu-id="df56d-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="df56d-111">-BlockchainMemberName</span></span>
<span data-ttu-id="df56d-112">Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="df56d-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="df56d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df56d-113">-DefaultProfile</span></span>
<span data-ttu-id="df56d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df56d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df56d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df56d-115">-ResourceGroupName</span></span>
<span data-ttu-id="df56d-116">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="df56d-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="df56d-117">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="df56d-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="df56d-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df56d-118">-SubscriptionId</span></span>
<span data-ttu-id="df56d-119">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="df56d-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="df56d-120">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="df56d-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="df56d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df56d-121">-Confirm</span></span>
<span data-ttu-id="df56d-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="df56d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df56d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df56d-123">-WhatIf</span></span>
<span data-ttu-id="df56d-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="df56d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df56d-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="df56d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df56d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df56d-126">CommonParameters</span></span>
<span data-ttu-id="df56d-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df56d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df56d-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df56d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df56d-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df56d-129">INPUTS</span></span>

## <span data-ttu-id="df56d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df56d-130">OUTPUTS</span></span>

### <span data-ttu-id="df56d-131">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="df56d-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="df56d-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="df56d-132">NOTES</span></span>

<span data-ttu-id="df56d-133">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="df56d-133">ALIASES</span></span>

## <span data-ttu-id="df56d-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df56d-134">RELATED LINKS</span></span>

