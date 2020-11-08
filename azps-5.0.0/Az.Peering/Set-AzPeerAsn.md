---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246877"
---
# <span data-ttu-id="202b0-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="202b0-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="202b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="202b0-102">SYNOPSIS</span></span>
<span data-ttu-id="202b0-103">Обновление контактных данных</span><span class="sxs-lookup"><span data-stu-id="202b0-103">Update Contact Information</span></span>

## <span data-ttu-id="202b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="202b0-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="202b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="202b0-105">DESCRIPTION</span></span>
<span data-ttu-id="202b0-106">Позволяет обновлять контактные данные PeerAsn подписки.</span><span class="sxs-lookup"><span data-stu-id="202b0-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="202b0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="202b0-107">EXAMPLES</span></span>

### <span data-ttu-id="202b0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="202b0-108">Example 1</span></span>
```powershell
#Get the Peer ASN object
PS C:> Get-AzPeerAsn -PeerName Contoso | Set-AzPeerAsn -Email noc1@contoso.com

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="202b0-109">Добавляет адрес электронной почты для однорангового узла ASN</span><span class="sxs-lookup"><span data-stu-id="202b0-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="202b0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="202b0-110">PARAMETERS</span></span>

### <span data-ttu-id="202b0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="202b0-111">-AsJob</span></span>
<span data-ttu-id="202b0-112">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="202b0-112">Run in the background.</span></span>

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

### <span data-ttu-id="202b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="202b0-113">-DefaultProfile</span></span>
<span data-ttu-id="202b0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="202b0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="202b0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="202b0-115">-InputObject</span></span>
<span data-ttu-id="202b0-116">{{Fill InputObject описание}}</span><span class="sxs-lookup"><span data-stu-id="202b0-116">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="202b0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="202b0-117">-Confirm</span></span>
<span data-ttu-id="202b0-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="202b0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="202b0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="202b0-119">-WhatIf</span></span>
<span data-ttu-id="202b0-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="202b0-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="202b0-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="202b0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="202b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="202b0-122">CommonParameters</span></span>
<span data-ttu-id="202b0-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="202b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="202b0-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="202b0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="202b0-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="202b0-125">INPUTS</span></span>

### <span data-ttu-id="202b0-126">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeerAsn)</span><span class="sxs-lookup"><span data-stu-id="202b0-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="202b0-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="202b0-127">OUTPUTS</span></span>

### <span data-ttu-id="202b0-128">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeerAsn)</span><span class="sxs-lookup"><span data-stu-id="202b0-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="202b0-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="202b0-129">NOTES</span></span>

## <span data-ttu-id="202b0-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="202b0-130">RELATED LINKS</span></span>
