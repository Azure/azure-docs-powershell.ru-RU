---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: d1ff0baeff3bf4b5747ff1d024b0de6e5184688a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072760"
---
# <span data-ttu-id="d9ba5-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="d9ba5-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="d9ba5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ba5-103">Удаление однорангового ASN</span><span class="sxs-lookup"><span data-stu-id="d9ba5-103">Remove Peer Asn</span></span>

## <span data-ttu-id="d9ba5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9ba5-104">SYNTAX</span></span>

### <span data-ttu-id="d9ba5-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d9ba5-105">Default (Default)</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ba5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d9ba5-106">ByName</span></span>
```
Remove-AzPeerAsn [-Name] <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9ba5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9ba5-107">DESCRIPTION</span></span>
<span data-ttu-id="d9ba5-108">Удаление PeerAsn из подписки.</span><span class="sxs-lookup"><span data-stu-id="d9ba5-108">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="d9ba5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9ba5-109">EXAMPLES</span></span>

### <span data-ttu-id="d9ba5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d9ba5-110">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="d9ba5-111">Удаляет одноранговый ASN</span><span class="sxs-lookup"><span data-stu-id="d9ba5-111">Removes the Peer Asn</span></span>

## <span data-ttu-id="d9ba5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9ba5-112">PARAMETERS</span></span>

### <span data-ttu-id="d9ba5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9ba5-113">-AsJob</span></span>
<span data-ttu-id="d9ba5-114">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="d9ba5-114">Run in the background.</span></span>

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

### <span data-ttu-id="d9ba5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ba5-115">-DefaultProfile</span></span>
<span data-ttu-id="d9ba5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ba5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9ba5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d9ba5-117">-Force</span></span>
<span data-ttu-id="d9ba5-118">{Определение принудительной заливки}}</span><span class="sxs-lookup"><span data-stu-id="d9ba5-118">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="d9ba5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9ba5-119">-InputObject</span></span>
<span data-ttu-id="d9ba5-120">Объект PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="d9ba5-120">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ba5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d9ba5-121">-Name</span></span>
<span data-ttu-id="d9ba5-122">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="d9ba5-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ba5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9ba5-123">-PassThru</span></span>
<span data-ttu-id="d9ba5-124">Возвращает значение истина, если завершено</span><span class="sxs-lookup"><span data-stu-id="d9ba5-124">Return true if complete</span></span>

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

### <span data-ttu-id="d9ba5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9ba5-125">-Confirm</span></span>
<span data-ttu-id="d9ba5-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d9ba5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9ba5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9ba5-127">-WhatIf</span></span>
<span data-ttu-id="d9ba5-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d9ba5-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9ba5-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d9ba5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9ba5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ba5-130">CommonParameters</span></span>
<span data-ttu-id="d9ba5-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9ba5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ba5-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9ba5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ba5-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9ba5-133">INPUTS</span></span>

### <span data-ttu-id="d9ba5-134">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeerAsn)</span><span class="sxs-lookup"><span data-stu-id="d9ba5-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="d9ba5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9ba5-135">OUTPUTS</span></span>

### <span data-ttu-id="d9ba5-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9ba5-136">System.Boolean</span></span>

## <span data-ttu-id="d9ba5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9ba5-137">NOTES</span></span>

## <span data-ttu-id="d9ba5-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9ba5-138">RELATED LINKS</span></span>
