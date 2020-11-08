---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246367"
---
# <span data-ttu-id="51d65-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="51d65-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="51d65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51d65-102">SYNOPSIS</span></span>
<span data-ttu-id="51d65-103">Удаление однорангового ASN</span><span class="sxs-lookup"><span data-stu-id="51d65-103">Remove Peer Asn</span></span>

## <span data-ttu-id="51d65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51d65-104">SYNTAX</span></span>

### <span data-ttu-id="51d65-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="51d65-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51d65-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="51d65-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51d65-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="51d65-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51d65-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51d65-108">DESCRIPTION</span></span>
<span data-ttu-id="51d65-109">Удаление PeerAsn из подписки.</span><span class="sxs-lookup"><span data-stu-id="51d65-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="51d65-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51d65-110">EXAMPLES</span></span>

### <span data-ttu-id="51d65-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="51d65-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="51d65-112">Удаляет одноранговый ASN</span><span class="sxs-lookup"><span data-stu-id="51d65-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="51d65-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51d65-113">PARAMETERS</span></span>

### <span data-ttu-id="51d65-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51d65-114">-AsJob</span></span>
<span data-ttu-id="51d65-115">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="51d65-115">Run in the background.</span></span>

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

### <span data-ttu-id="51d65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51d65-116">-DefaultProfile</span></span>
<span data-ttu-id="51d65-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51d65-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51d65-118">-Force</span><span class="sxs-lookup"><span data-stu-id="51d65-118">-Force</span></span>
<span data-ttu-id="51d65-119">{Определение принудительной заливки}}</span><span class="sxs-lookup"><span data-stu-id="51d65-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="51d65-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51d65-120">-InputObject</span></span>
<span data-ttu-id="51d65-121">Объект PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="51d65-121">The PeerAsn object.</span></span>

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

### <span data-ttu-id="51d65-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="51d65-122">-Name</span></span>
<span data-ttu-id="51d65-123">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="51d65-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="51d65-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51d65-124">-PassThru</span></span>
<span data-ttu-id="51d65-125">Возвращает значение истина, если завершено</span><span class="sxs-lookup"><span data-stu-id="51d65-125">Return true if complete</span></span>

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

### <span data-ttu-id="51d65-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51d65-126">-ResourceId</span></span>
<span data-ttu-id="51d65-127">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="51d65-127">The resource id string name.</span></span>

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

### <span data-ttu-id="51d65-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51d65-128">-Confirm</span></span>
<span data-ttu-id="51d65-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="51d65-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51d65-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51d65-130">-WhatIf</span></span>
<span data-ttu-id="51d65-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="51d65-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51d65-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="51d65-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51d65-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d65-133">CommonParameters</span></span>
<span data-ttu-id="51d65-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51d65-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d65-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51d65-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d65-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51d65-136">INPUTS</span></span>

### <span data-ttu-id="51d65-137">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeerAsn)</span><span class="sxs-lookup"><span data-stu-id="51d65-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="51d65-138">System. String</span><span class="sxs-lookup"><span data-stu-id="51d65-138">System.String</span></span>

## <span data-ttu-id="51d65-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51d65-139">OUTPUTS</span></span>

### <span data-ttu-id="51d65-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51d65-140">System.Boolean</span></span>

## <span data-ttu-id="51d65-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="51d65-141">NOTES</span></span>

## <span data-ttu-id="51d65-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51d65-142">RELATED LINKS</span></span>
