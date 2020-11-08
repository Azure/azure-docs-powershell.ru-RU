---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: f811f73b50f88a256de62069a287d113607e7ee1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074475"
---
# <span data-ttu-id="8b922-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="8b922-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="8b922-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b922-102">SYNOPSIS</span></span>
<span data-ttu-id="8b922-103">Создание нового однорангового ASN</span><span class="sxs-lookup"><span data-stu-id="8b922-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="8b922-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b922-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -Email <String[]> -Phone <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b922-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b922-105">DESCRIPTION</span></span>
<span data-ttu-id="8b922-106">Создает новый объект PeerAsn для подписки.</span><span class="sxs-lookup"><span data-stu-id="8b922-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="8b922-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b922-107">EXAMPLES</span></span>

### <span data-ttu-id="8b922-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b922-108">Example 1</span></span>
```powershell
PS C:> New-AzPeerAsn -Name Contoso65050 -PeerName Contoso -PeerAsn 65050 -Emails noc@contoso.com -Phone "888-888-8889"

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="8b922-109">Создание нового PeerAsn</span><span class="sxs-lookup"><span data-stu-id="8b922-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="8b922-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b922-110">PARAMETERS</span></span>

### <span data-ttu-id="8b922-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b922-111">-AsJob</span></span>
<span data-ttu-id="8b922-112">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="8b922-112">Run in the background.</span></span>

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

### <span data-ttu-id="8b922-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b922-113">-DefaultProfile</span></span>
<span data-ttu-id="8b922-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b922-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b922-115">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="8b922-115">-Email</span></span>
<span data-ttu-id="8b922-116">Отправить по электронной почте</span><span class="sxs-lookup"><span data-stu-id="8b922-116">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b922-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8b922-117">-Name</span></span>
<span data-ttu-id="8b922-118">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="8b922-118">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b922-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="8b922-119">-PeerAsn</span></span>
<span data-ttu-id="8b922-120">Идентификатор однорангового ресурса ASN. Используйте Get-AzPeerAsn для получения идентификатора.</span><span class="sxs-lookup"><span data-stu-id="8b922-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b922-121">-Одноранговое</span><span class="sxs-lookup"><span data-stu-id="8b922-121">-PeerName</span></span>
<span data-ttu-id="8b922-122">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="8b922-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b922-123">-Phone</span><span class="sxs-lookup"><span data-stu-id="8b922-123">-Phone</span></span>
<span data-ttu-id="8b922-124">Кнопка</span><span class="sxs-lookup"><span data-stu-id="8b922-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b922-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b922-125">-Confirm</span></span>
<span data-ttu-id="8b922-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b922-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b922-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b922-127">-WhatIf</span></span>
<span data-ttu-id="8b922-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b922-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b922-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b922-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b922-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b922-130">CommonParameters</span></span>
<span data-ttu-id="8b922-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b922-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b922-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b922-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b922-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b922-133">INPUTS</span></span>

### <span data-ttu-id="8b922-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="8b922-134">None</span></span>

## <span data-ttu-id="8b922-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b922-135">OUTPUTS</span></span>

### <span data-ttu-id="8b922-136">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeerAsn)</span><span class="sxs-lookup"><span data-stu-id="8b922-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="8b922-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b922-137">NOTES</span></span>

## <span data-ttu-id="8b922-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b922-138">RELATED LINKS</span></span>
