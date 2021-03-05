---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: 11f3a729c6818a7794a8b42a4b21a658530cc60d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989456"
---
# <span data-ttu-id="7e561-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="7e561-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="7e561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e561-102">SYNOPSIS</span></span>
<span data-ttu-id="7e561-103">Создание нового одноранговых asN</span><span class="sxs-lookup"><span data-stu-id="7e561-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="7e561-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7e561-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e561-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e561-105">DESCRIPTION</span></span>
<span data-ttu-id="7e561-106">Создает объект PeerAsn для подписки.</span><span class="sxs-lookup"><span data-stu-id="7e561-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="7e561-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7e561-107">EXAMPLES</span></span>

### <span data-ttu-id="7e561-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e561-108">Example 1</span></span>
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

<span data-ttu-id="7e561-109">Создание нового peerAsn</span><span class="sxs-lookup"><span data-stu-id="7e561-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="7e561-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e561-110">PARAMETERS</span></span>

### <span data-ttu-id="7e561-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e561-111">-AsJob</span></span>
<span data-ttu-id="7e561-112">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="7e561-112">Run in the background.</span></span>

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

### <span data-ttu-id="7e561-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="7e561-113">-ContactDetail</span></span>
<span data-ttu-id="7e561-114">Адреса электронной почты, используемые для связи, если проблемы обычно заданы в Центре сетевых операций</span><span class="sxs-lookup"><span data-stu-id="7e561-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="7e561-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e561-115">-DefaultProfile</span></span>
<span data-ttu-id="7e561-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e561-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e561-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7e561-117">-Name</span></span>
<span data-ttu-id="7e561-118">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="7e561-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="7e561-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="7e561-119">-PeerAsn</span></span>
<span data-ttu-id="7e561-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span><span class="sxs-lookup"><span data-stu-id="7e561-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="7e561-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="7e561-121">-PeerName</span></span>
<span data-ttu-id="7e561-122">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="7e561-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="7e561-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e561-123">-Confirm</span></span>
<span data-ttu-id="7e561-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7e561-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e561-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e561-125">-WhatIf</span></span>
<span data-ttu-id="7e561-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e561-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e561-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7e561-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e561-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e561-128">CommonParameters</span></span>
<span data-ttu-id="7e561-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e561-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e561-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e561-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e561-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e561-131">INPUTS</span></span>

### <span data-ttu-id="7e561-132">Нет</span><span class="sxs-lookup"><span data-stu-id="7e561-132">None</span></span>

## <span data-ttu-id="7e561-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e561-133">OUTPUTS</span></span>

### <span data-ttu-id="7e561-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="7e561-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="7e561-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7e561-135">NOTES</span></span>

## <span data-ttu-id="7e561-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e561-136">RELATED LINKS</span></span>
