---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234836"
---
# <span data-ttu-id="e4a65-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="e4a65-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="e4a65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4a65-102">SYNOPSIS</span></span>
<span data-ttu-id="e4a65-103">Создание нового однорангового ASN</span><span class="sxs-lookup"><span data-stu-id="e4a65-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="e4a65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4a65-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4a65-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4a65-105">DESCRIPTION</span></span>
<span data-ttu-id="e4a65-106">Создает новый объект PeerAsn для подписки.</span><span class="sxs-lookup"><span data-stu-id="e4a65-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="e4a65-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4a65-107">EXAMPLES</span></span>

### <span data-ttu-id="e4a65-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e4a65-108">Example 1</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="e4a65-109">Создание нового PeerAsn</span><span class="sxs-lookup"><span data-stu-id="e4a65-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="e4a65-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4a65-110">PARAMETERS</span></span>

### <span data-ttu-id="e4a65-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4a65-111">-AsJob</span></span>
<span data-ttu-id="e4a65-112">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="e4a65-112">Run in the background.</span></span>

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

### <span data-ttu-id="e4a65-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="e4a65-113">-ContactDetail</span></span>
<span data-ttu-id="e4a65-114">Адреса электронной почты, которые используются для связи, если arrise обычно является центром сетевых операций</span><span class="sxs-lookup"><span data-stu-id="e4a65-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4a65-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4a65-115">-DefaultProfile</span></span>
<span data-ttu-id="e4a65-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4a65-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4a65-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e4a65-117">-Name</span></span>
<span data-ttu-id="e4a65-118">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e4a65-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e4a65-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="e4a65-119">-PeerAsn</span></span>
<span data-ttu-id="e4a65-120">Идентификатор однорангового ресурса ASN. Используйте Get-AzPeerAsn для получения идентификатора.</span><span class="sxs-lookup"><span data-stu-id="e4a65-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="e4a65-121">-Одноранговое</span><span class="sxs-lookup"><span data-stu-id="e4a65-121">-PeerName</span></span>
<span data-ttu-id="e4a65-122">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e4a65-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e4a65-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4a65-123">-Confirm</span></span>
<span data-ttu-id="e4a65-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e4a65-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4a65-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4a65-125">-WhatIf</span></span>
<span data-ttu-id="e4a65-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e4a65-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4a65-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e4a65-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4a65-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4a65-128">CommonParameters</span></span>
<span data-ttu-id="e4a65-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4a65-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4a65-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4a65-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4a65-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4a65-131">INPUTS</span></span>

### <span data-ttu-id="e4a65-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="e4a65-132">None</span></span>

## <span data-ttu-id="e4a65-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4a65-133">OUTPUTS</span></span>

### <span data-ttu-id="e4a65-134">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeerAsn)</span><span class="sxs-lookup"><span data-stu-id="e4a65-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="e4a65-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4a65-135">NOTES</span></span>

## <span data-ttu-id="e4a65-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4a65-136">RELATED LINKS</span></span>