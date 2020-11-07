---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e2588e1516b8b0ee41e260b27ea40ed72a199613
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904630"
---
# <span data-ttu-id="ca8e9-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="ca8e9-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="ca8e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca8e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8e9-103">Получает объект PeerAsn из ARM.</span><span class="sxs-lookup"><span data-stu-id="ca8e9-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="ca8e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca8e9-104">SYNTAX</span></span>

```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca8e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca8e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ca8e9-106">Возвращает PeerAsn для подписки.</span><span class="sxs-lookup"><span data-stu-id="ca8e9-106">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="ca8e9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca8e9-107">EXAMPLES</span></span>

### <span data-ttu-id="ca8e9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ca8e9-108">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -PeerName Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="ca8e9-109">Возвращает PeerAsn</span><span class="sxs-lookup"><span data-stu-id="ca8e9-109">Gets the PeerAsn</span></span>

## <span data-ttu-id="ca8e9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca8e9-110">PARAMETERS</span></span>

### <span data-ttu-id="ca8e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8e9-111">-DefaultProfile</span></span>
<span data-ttu-id="ca8e9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca8e9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca8e9-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca8e9-113">-Name</span></span>
<span data-ttu-id="ca8e9-114">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="ca8e9-114">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8e9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8e9-115">CommonParameters</span></span>
<span data-ttu-id="ca8e9-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca8e9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8e9-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca8e9-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8e9-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca8e9-118">INPUTS</span></span>

### <span data-ttu-id="ca8e9-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="ca8e9-119">None</span></span>

## <span data-ttu-id="ca8e9-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca8e9-120">OUTPUTS</span></span>

### <span data-ttu-id="ca8e9-121">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeerAsn)</span><span class="sxs-lookup"><span data-stu-id="ca8e9-121">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="ca8e9-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca8e9-122">NOTES</span></span>

## <span data-ttu-id="ca8e9-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca8e9-123">RELATED LINKS</span></span>
