---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 2f46b13570ef1f538658dae6d02000848822c150
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953891"
---
# <span data-ttu-id="14d24-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="14d24-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="14d24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14d24-102">SYNOPSIS</span></span>
<span data-ttu-id="14d24-103">Создает IP-тег.</span><span class="sxs-lookup"><span data-stu-id="14d24-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="14d24-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="14d24-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14d24-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14d24-105">DESCRIPTION</span></span>
<span data-ttu-id="14d24-106">Командлет **New-AzPublicIpTag** создает IP-тег.</span><span class="sxs-lookup"><span data-stu-id="14d24-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="14d24-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="14d24-107">EXAMPLES</span></span>

### <span data-ttu-id="14d24-108">Пример 1. Создание нового IP-тега</span><span class="sxs-lookup"><span data-stu-id="14d24-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="14d24-109">Эта команда создает новый IP-тег с тегом FirstPartyUsage и тегом "/Sql".</span><span class="sxs-lookup"><span data-stu-id="14d24-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="14d24-110">Этот тег используется при создании publicIpAddress с конкретными тегами для выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14d24-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="14d24-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14d24-111">PARAMETERS</span></span>

### <span data-ttu-id="14d24-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d24-112">-DefaultProfile</span></span>
<span data-ttu-id="14d24-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14d24-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14d24-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="14d24-114">-IpTagType</span></span>
<span data-ttu-id="14d24-115">Пример типа IPTag:FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="14d24-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d24-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="14d24-116">-Tag</span></span>
<span data-ttu-id="14d24-117">Пример значения IpTag:/Sql</span><span class="sxs-lookup"><span data-stu-id="14d24-117">IpTag value Example:/Sql</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d24-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14d24-118">-Confirm</span></span>
<span data-ttu-id="14d24-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14d24-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14d24-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14d24-120">-WhatIf</span></span>
<span data-ttu-id="14d24-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14d24-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14d24-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="14d24-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14d24-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d24-123">CommonParameters</span></span>
<span data-ttu-id="14d24-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14d24-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d24-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14d24-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d24-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14d24-126">INPUTS</span></span>

### <span data-ttu-id="14d24-127">System.String</span><span class="sxs-lookup"><span data-stu-id="14d24-127">System.String</span></span>

## <span data-ttu-id="14d24-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="14d24-128">OUTPUTS</span></span>

### <span data-ttu-id="14d24-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="14d24-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="14d24-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="14d24-130">NOTES</span></span>

## <span data-ttu-id="14d24-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14d24-131">RELATED LINKS</span></span>
