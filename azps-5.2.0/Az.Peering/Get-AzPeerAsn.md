---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400143"
---
# <span data-ttu-id="8be96-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="8be96-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="8be96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8be96-102">SYNOPSIS</span></span>
<span data-ttu-id="8be96-103">Получает объект PeerAsn из ARM.</span><span class="sxs-lookup"><span data-stu-id="8be96-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="8be96-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8be96-104">SYNTAX</span></span>

### <span data-ttu-id="8be96-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8be96-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8be96-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8be96-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8be96-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8be96-107">DESCRIPTION</span></span>
<span data-ttu-id="8be96-108">Возвращает peerAsn для подписки.</span><span class="sxs-lookup"><span data-stu-id="8be96-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="8be96-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8be96-109">EXAMPLES</span></span>

### <span data-ttu-id="8be96-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8be96-110">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -Name Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="8be96-111">Получает одноранговую оценку</span><span class="sxs-lookup"><span data-stu-id="8be96-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="8be96-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8be96-112">PARAMETERS</span></span>

### <span data-ttu-id="8be96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be96-113">-DefaultProfile</span></span>
<span data-ttu-id="8be96-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8be96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8be96-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8be96-115">-Name</span></span>
<span data-ttu-id="8be96-116">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="8be96-116">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be96-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8be96-117">-ResourceId</span></span>
<span data-ttu-id="8be96-118">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="8be96-118">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8be96-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be96-119">CommonParameters</span></span>
<span data-ttu-id="8be96-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be96-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be96-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8be96-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be96-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8be96-122">INPUTS</span></span>

### <span data-ttu-id="8be96-123">System.String</span><span class="sxs-lookup"><span data-stu-id="8be96-123">System.String</span></span>

## <span data-ttu-id="8be96-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8be96-124">OUTPUTS</span></span>

### <span data-ttu-id="8be96-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="8be96-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="8be96-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8be96-126">NOTES</span></span>

## <span data-ttu-id="8be96-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8be96-127">RELATED LINKS</span></span>
