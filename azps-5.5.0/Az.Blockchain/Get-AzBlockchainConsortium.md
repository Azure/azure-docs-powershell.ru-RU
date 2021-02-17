---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216036"
---
# <span data-ttu-id="9e576-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="9e576-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="9e576-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e576-102">SYNOPSIS</span></span>
<span data-ttu-id="9e576-103">Список доступных для подписки консорциумов.</span><span class="sxs-lookup"><span data-stu-id="9e576-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="9e576-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9e576-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9e576-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e576-105">DESCRIPTION</span></span>
<span data-ttu-id="9e576-106">Список доступных для подписки консорциумов.</span><span class="sxs-lookup"><span data-stu-id="9e576-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="9e576-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9e576-107">EXAMPLES</span></span>

### <span data-ttu-id="9e576-108">Пример 1. Получить Консорциумы.</span><span class="sxs-lookup"><span data-stu-id="9e576-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="9e576-109">Эта команда содержит список unis в рамках подписки на определенное место.</span><span class="sxs-lookup"><span data-stu-id="9e576-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="9e576-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e576-110">PARAMETERS</span></span>

### <span data-ttu-id="9e576-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e576-111">-DefaultProfile</span></span>
<span data-ttu-id="9e576-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e576-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e576-113">-Location</span><span class="sxs-lookup"><span data-stu-id="9e576-113">-Location</span></span>
<span data-ttu-id="9e576-114">Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="9e576-114">Location Name.</span></span>

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

### <span data-ttu-id="9e576-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e576-115">-SubscriptionId</span></span>
<span data-ttu-id="9e576-116">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9e576-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9e576-117">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="9e576-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9e576-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e576-118">-Confirm</span></span>
<span data-ttu-id="9e576-119">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9e576-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e576-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e576-120">-WhatIf</span></span>
<span data-ttu-id="9e576-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e576-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e576-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9e576-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e576-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e576-123">CommonParameters</span></span>
<span data-ttu-id="9e576-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e576-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e576-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e576-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e576-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e576-126">INPUTS</span></span>

## <span data-ttu-id="9e576-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e576-127">OUTPUTS</span></span>

### <span data-ttu-id="9e576-128">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IConsortium</span><span class="sxs-lookup"><span data-stu-id="9e576-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="9e576-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9e576-129">NOTES</span></span>

<span data-ttu-id="9e576-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9e576-130">ALIASES</span></span>

## <span data-ttu-id="9e576-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e576-131">RELATED LINKS</span></span>

