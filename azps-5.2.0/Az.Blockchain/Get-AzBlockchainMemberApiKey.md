---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393804"
---
# <span data-ttu-id="e7503-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="e7503-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="e7503-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7503-102">SYNOPSIS</span></span>
<span data-ttu-id="e7503-103">Содержит перечень ключей API для участника группы.</span><span class="sxs-lookup"><span data-stu-id="e7503-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="e7503-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e7503-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e7503-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7503-105">DESCRIPTION</span></span>
<span data-ttu-id="e7503-106">Содержит перечень ключей API для участника группы.</span><span class="sxs-lookup"><span data-stu-id="e7503-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="e7503-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e7503-107">EXAMPLES</span></span>

### <span data-ttu-id="e7503-108">Пример 1. List и клавиши API</span><span class="sxs-lookup"><span data-stu-id="e7503-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="e7503-109">Эта команда содержит клавиши API для участника, который является участником группы.</span><span class="sxs-lookup"><span data-stu-id="e7503-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="e7503-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7503-110">PARAMETERS</span></span>

### <span data-ttu-id="e7503-111">-ЛесОИмяноИмя</span><span class="sxs-lookup"><span data-stu-id="e7503-111">-BlockchainMemberName</span></span>
<span data-ttu-id="e7503-112">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="e7503-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="e7503-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7503-113">-DefaultProfile</span></span>
<span data-ttu-id="e7503-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7503-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7503-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7503-115">-ResourceGroupName</span></span>
<span data-ttu-id="e7503-116">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="e7503-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e7503-117">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="e7503-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e7503-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7503-118">-SubscriptionId</span></span>
<span data-ttu-id="e7503-119">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e7503-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e7503-120">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="e7503-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e7503-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7503-121">-Confirm</span></span>
<span data-ttu-id="e7503-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e7503-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7503-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7503-123">-WhatIf</span></span>
<span data-ttu-id="e7503-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7503-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7503-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e7503-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7503-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7503-126">CommonParameters</span></span>
<span data-ttu-id="e7503-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7503-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7503-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7503-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7503-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7503-129">INPUTS</span></span>

## <span data-ttu-id="e7503-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e7503-130">OUTPUTS</span></span>

### <span data-ttu-id="e7503-131">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="e7503-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="e7503-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e7503-132">NOTES</span></span>

<span data-ttu-id="e7503-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e7503-133">ALIASES</span></span>

## <span data-ttu-id="e7503-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7503-134">RELATED LINKS</span></span>

