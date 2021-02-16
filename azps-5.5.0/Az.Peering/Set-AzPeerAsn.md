---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225521"
---
# <span data-ttu-id="bbbbb-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="bbbbb-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="bbbbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbbbb-102">SYNOPSIS</span></span>
<span data-ttu-id="bbbbb-103">Обновление контактных данных</span><span class="sxs-lookup"><span data-stu-id="bbbbb-103">Update Contact Information</span></span>

## <span data-ttu-id="bbbbb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bbbbb-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbbbb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbbbb-105">DESCRIPTION</span></span>
<span data-ttu-id="bbbbb-106">Позволяет обновлять контактные данные одноранговых пользователей в подписке.</span><span class="sxs-lookup"><span data-stu-id="bbbbb-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="bbbbb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bbbbb-107">EXAMPLES</span></span>

### <span data-ttu-id="bbbbb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bbbbb-108">Example 1</span></span>
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

<span data-ttu-id="bbbbb-109">Добавляет адрес электронной почты к одноранговой учетной записи</span><span class="sxs-lookup"><span data-stu-id="bbbbb-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="bbbbb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbbbb-110">PARAMETERS</span></span>

### <span data-ttu-id="bbbbb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbbbb-111">-AsJob</span></span>
<span data-ttu-id="bbbbb-112">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="bbbbb-112">Run in the background.</span></span>

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

### <span data-ttu-id="bbbbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbbbb-113">-DefaultProfile</span></span>
<span data-ttu-id="bbbbb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbbbb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbbbb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbbbb-115">-InputObject</span></span>
<span data-ttu-id="bbbbb-116">{{ Заполнить описание inputObject }}</span><span class="sxs-lookup"><span data-stu-id="bbbbb-116">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="bbbbb-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbbbb-117">-Confirm</span></span>
<span data-ttu-id="bbbbb-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bbbbb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbbbb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbbbb-119">-WhatIf</span></span>
<span data-ttu-id="bbbbb-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbbbb-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bbbbb-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bbbbb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbbbb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbbbb-122">CommonParameters</span></span>
<span data-ttu-id="bbbbb-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbbbb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbbbb-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbbbb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbbbb-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbbbb-125">INPUTS</span></span>

### <span data-ttu-id="bbbbb-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="bbbbb-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="bbbbb-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bbbbb-127">OUTPUTS</span></span>

### <span data-ttu-id="bbbbb-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="bbbbb-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="bbbbb-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bbbbb-129">NOTES</span></span>

## <span data-ttu-id="bbbbb-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbbbb-130">RELATED LINKS</span></span>
