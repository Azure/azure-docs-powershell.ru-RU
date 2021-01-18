---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 5d7d73b3c7f49babc9e80929dab7b3fa2adad20a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505506"
---
# <span data-ttu-id="db6a7-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="db6a7-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="db6a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db6a7-102">SYNOPSIS</span></span>
<span data-ttu-id="db6a7-103">Создает IP-тег.</span><span class="sxs-lookup"><span data-stu-id="db6a7-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="db6a7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="db6a7-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db6a7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db6a7-105">DESCRIPTION</span></span>
<span data-ttu-id="db6a7-106">Командлет **New-AzPublicIpTag** создает IP-тег.</span><span class="sxs-lookup"><span data-stu-id="db6a7-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="db6a7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="db6a7-107">EXAMPLES</span></span>

### <span data-ttu-id="db6a7-108">Пример 1. Создание нового IP-тега</span><span class="sxs-lookup"><span data-stu-id="db6a7-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="db6a7-109">Эта команда создает новый IP-тег с тегом FirstPartyUsage и тегом "/Sql".</span><span class="sxs-lookup"><span data-stu-id="db6a7-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="db6a7-110">Этот тег используется при создании publicIpAddress с конкретными тегами для выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db6a7-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="db6a7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db6a7-111">PARAMETERS</span></span>

### <span data-ttu-id="db6a7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6a7-112">-DefaultProfile</span></span>
<span data-ttu-id="db6a7-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db6a7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db6a7-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="db6a7-114">-IpTagType</span></span>
<span data-ttu-id="db6a7-115">Пример типа IPTag:FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="db6a7-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="db6a7-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="db6a7-116">-Tag</span></span>
<span data-ttu-id="db6a7-117">Пример значения IpTag:/Sql</span><span class="sxs-lookup"><span data-stu-id="db6a7-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="db6a7-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db6a7-118">-Confirm</span></span>
<span data-ttu-id="db6a7-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db6a7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db6a7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db6a7-120">-WhatIf</span></span>
<span data-ttu-id="db6a7-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db6a7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db6a7-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="db6a7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db6a7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6a7-123">CommonParameters</span></span>
<span data-ttu-id="db6a7-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6a7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6a7-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db6a7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6a7-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db6a7-126">INPUTS</span></span>

### <span data-ttu-id="db6a7-127">System.String</span><span class="sxs-lookup"><span data-stu-id="db6a7-127">System.String</span></span>

## <span data-ttu-id="db6a7-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db6a7-128">OUTPUTS</span></span>

### <span data-ttu-id="db6a7-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="db6a7-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="db6a7-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="db6a7-130">NOTES</span></span>

## <span data-ttu-id="db6a7-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db6a7-131">RELATED LINKS</span></span>
