---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: 81398d4ab62db1b8dca573dfd6beccde3be63700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904582"
---
# <span data-ttu-id="4010a-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="4010a-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="4010a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4010a-102">SYNOPSIS</span></span>
<span data-ttu-id="4010a-103">Обновление контактных данных</span><span class="sxs-lookup"><span data-stu-id="4010a-103">Update Contact Information</span></span>

## <span data-ttu-id="4010a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4010a-104">SYNTAX</span></span>

### <span data-ttu-id="4010a-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4010a-105">ByName (Default)</span></span>
```
Set-AzPeerAsn [-Name] <String> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4010a-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="4010a-106">Default</span></span>
```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4010a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4010a-107">DESCRIPTION</span></span>
<span data-ttu-id="4010a-108">Позволяет обновлять контактные данные PeerAsn подписки.</span><span class="sxs-lookup"><span data-stu-id="4010a-108">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="4010a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4010a-109">EXAMPLES</span></span>

### <span data-ttu-id="4010a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4010a-110">Example 1</span></span>
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

<span data-ttu-id="4010a-111">Добавляет адрес электронной почты для однорангового узла ASN</span><span class="sxs-lookup"><span data-stu-id="4010a-111">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="4010a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4010a-112">PARAMETERS</span></span>

### <span data-ttu-id="4010a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4010a-113">-AsJob</span></span>
<span data-ttu-id="4010a-114">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="4010a-114">Run in the background.</span></span>

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

### <span data-ttu-id="4010a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4010a-115">-DefaultProfile</span></span>
<span data-ttu-id="4010a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4010a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4010a-117">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="4010a-117">-Email</span></span>
<span data-ttu-id="4010a-118">Отправить по электронной почте</span><span class="sxs-lookup"><span data-stu-id="4010a-118">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4010a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4010a-119">-InputObject</span></span>
<span data-ttu-id="4010a-120">{{Fill InputObject описание}}</span><span class="sxs-lookup"><span data-stu-id="4010a-120">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="4010a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4010a-121">-Name</span></span>
<span data-ttu-id="4010a-122">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="4010a-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="4010a-123">-Phone</span><span class="sxs-lookup"><span data-stu-id="4010a-123">-Phone</span></span>
<span data-ttu-id="4010a-124">Кнопка</span><span class="sxs-lookup"><span data-stu-id="4010a-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4010a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4010a-125">-Confirm</span></span>
<span data-ttu-id="4010a-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4010a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4010a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4010a-127">-WhatIf</span></span>
<span data-ttu-id="4010a-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4010a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4010a-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4010a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4010a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4010a-130">CommonParameters</span></span>
<span data-ttu-id="4010a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4010a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4010a-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4010a-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4010a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4010a-133">INPUTS</span></span>

### <span data-ttu-id="4010a-134">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeerAsn)</span><span class="sxs-lookup"><span data-stu-id="4010a-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="4010a-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4010a-135">OUTPUTS</span></span>

### <span data-ttu-id="4010a-136">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeerAsn)</span><span class="sxs-lookup"><span data-stu-id="4010a-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="4010a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="4010a-137">NOTES</span></span>

## <span data-ttu-id="4010a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4010a-138">RELATED LINKS</span></span>
