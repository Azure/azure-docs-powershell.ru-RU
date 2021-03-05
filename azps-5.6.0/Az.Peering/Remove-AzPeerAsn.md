---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: a5b50fd4d57fc7036196decdb7b967e2867b21f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989327"
---
# <span data-ttu-id="89fcc-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="89fcc-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="89fcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="89fcc-103">Удалить одноранговой asn</span><span class="sxs-lookup"><span data-stu-id="89fcc-103">Remove Peer Asn</span></span>

## <span data-ttu-id="89fcc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89fcc-104">SYNTAX</span></span>

### <span data-ttu-id="89fcc-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89fcc-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89fcc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="89fcc-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89fcc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="89fcc-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89fcc-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89fcc-108">DESCRIPTION</span></span>
<span data-ttu-id="89fcc-109">Удалите одноранговую подписку из подписки.</span><span class="sxs-lookup"><span data-stu-id="89fcc-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="89fcc-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89fcc-110">EXAMPLES</span></span>

### <span data-ttu-id="89fcc-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="89fcc-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="89fcc-112">Удаляет одноранговую оценку</span><span class="sxs-lookup"><span data-stu-id="89fcc-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="89fcc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89fcc-113">PARAMETERS</span></span>

### <span data-ttu-id="89fcc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89fcc-114">-AsJob</span></span>
<span data-ttu-id="89fcc-115">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="89fcc-115">Run in the background.</span></span>

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

### <span data-ttu-id="89fcc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89fcc-116">-DefaultProfile</span></span>
<span data-ttu-id="89fcc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89fcc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89fcc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="89fcc-118">-Force</span></span>
<span data-ttu-id="89fcc-119">{{ Fill Force Description }}</span><span class="sxs-lookup"><span data-stu-id="89fcc-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="89fcc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89fcc-120">-InputObject</span></span>
<span data-ttu-id="89fcc-121">Объект PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="89fcc-121">The PeerAsn object.</span></span>

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

### <span data-ttu-id="89fcc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="89fcc-122">-Name</span></span>
<span data-ttu-id="89fcc-123">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="89fcc-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="89fcc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89fcc-124">-PassThru</span></span>
<span data-ttu-id="89fcc-125">Возврат к истинам, если они завершены</span><span class="sxs-lookup"><span data-stu-id="89fcc-125">Return true if complete</span></span>

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

### <span data-ttu-id="89fcc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89fcc-126">-ResourceId</span></span>
<span data-ttu-id="89fcc-127">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="89fcc-127">The resource id string name.</span></span>

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

### <span data-ttu-id="89fcc-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89fcc-128">-Confirm</span></span>
<span data-ttu-id="89fcc-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89fcc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89fcc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89fcc-130">-WhatIf</span></span>
<span data-ttu-id="89fcc-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89fcc-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89fcc-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="89fcc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89fcc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89fcc-133">CommonParameters</span></span>
<span data-ttu-id="89fcc-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89fcc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89fcc-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89fcc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89fcc-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89fcc-136">INPUTS</span></span>

### <span data-ttu-id="89fcc-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="89fcc-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="89fcc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="89fcc-138">System.String</span></span>

## <span data-ttu-id="89fcc-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89fcc-139">OUTPUTS</span></span>

### <span data-ttu-id="89fcc-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89fcc-140">System.Boolean</span></span>

## <span data-ttu-id="89fcc-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89fcc-141">NOTES</span></span>

## <span data-ttu-id="89fcc-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89fcc-142">RELATED LINKS</span></span>
