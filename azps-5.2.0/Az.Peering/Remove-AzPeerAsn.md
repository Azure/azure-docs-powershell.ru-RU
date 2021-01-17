---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411319"
---
# <span data-ttu-id="7752a-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="7752a-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="7752a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7752a-102">SYNOPSIS</span></span>
<span data-ttu-id="7752a-103">Удалить одноранговой asn</span><span class="sxs-lookup"><span data-stu-id="7752a-103">Remove Peer Asn</span></span>

## <span data-ttu-id="7752a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7752a-104">SYNTAX</span></span>

### <span data-ttu-id="7752a-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7752a-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7752a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7752a-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7752a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7752a-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7752a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7752a-108">DESCRIPTION</span></span>
<span data-ttu-id="7752a-109">Удалите одноранговую подписку из подписки.</span><span class="sxs-lookup"><span data-stu-id="7752a-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="7752a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7752a-110">EXAMPLES</span></span>

### <span data-ttu-id="7752a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7752a-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="7752a-112">Удаляет одноранговую оценку</span><span class="sxs-lookup"><span data-stu-id="7752a-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="7752a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7752a-113">PARAMETERS</span></span>

### <span data-ttu-id="7752a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7752a-114">-AsJob</span></span>
<span data-ttu-id="7752a-115">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="7752a-115">Run in the background.</span></span>

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

### <span data-ttu-id="7752a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7752a-116">-DefaultProfile</span></span>
<span data-ttu-id="7752a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7752a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7752a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7752a-118">-Force</span></span>
<span data-ttu-id="7752a-119">{{ Fill Force Description }}</span><span class="sxs-lookup"><span data-stu-id="7752a-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="7752a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7752a-120">-InputObject</span></span>
<span data-ttu-id="7752a-121">Объект PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="7752a-121">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7752a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7752a-122">-Name</span></span>
<span data-ttu-id="7752a-123">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="7752a-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7752a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7752a-124">-PassThru</span></span>
<span data-ttu-id="7752a-125">Возврат к истинам, если они завершены</span><span class="sxs-lookup"><span data-stu-id="7752a-125">Return true if complete</span></span>

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

### <span data-ttu-id="7752a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7752a-126">-ResourceId</span></span>
<span data-ttu-id="7752a-127">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="7752a-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7752a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7752a-128">-Confirm</span></span>
<span data-ttu-id="7752a-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7752a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7752a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7752a-130">-WhatIf</span></span>
<span data-ttu-id="7752a-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7752a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7752a-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7752a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7752a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7752a-133">CommonParameters</span></span>
<span data-ttu-id="7752a-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7752a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7752a-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7752a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7752a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7752a-136">INPUTS</span></span>

### <span data-ttu-id="7752a-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="7752a-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="7752a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7752a-138">System.String</span></span>

## <span data-ttu-id="7752a-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7752a-139">OUTPUTS</span></span>

### <span data-ttu-id="7752a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7752a-140">System.Boolean</span></span>

## <span data-ttu-id="7752a-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7752a-141">NOTES</span></span>

## <span data-ttu-id="7752a-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7752a-142">RELATED LINKS</span></span>
