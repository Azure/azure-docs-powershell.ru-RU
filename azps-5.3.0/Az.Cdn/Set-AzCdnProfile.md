---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 341d46e5dd4ceefaf8baa76a71de462559115a5d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509337"
---
# <span data-ttu-id="c8769-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8769-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="c8769-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8769-102">SYNOPSIS</span></span>
<span data-ttu-id="c8769-103">Обновляет профиль сети CDN.</span><span class="sxs-lookup"><span data-stu-id="c8769-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="c8769-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c8769-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8769-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8769-105">DESCRIPTION</span></span>
<span data-ttu-id="c8769-106">**Настройка Set-AzCdnProfile** обновляет профиль сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="c8769-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="c8769-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c8769-107">EXAMPLES</span></span>

## <span data-ttu-id="c8769-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8769-108">PARAMETERS</span></span>

### <span data-ttu-id="c8769-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8769-109">-CdnProfile</span></span>
<span data-ttu-id="c8769-110">Определяет профиль, который обновляется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8769-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8769-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8769-111">-DefaultProfile</span></span>
<span data-ttu-id="c8769-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c8769-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8769-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8769-113">-Confirm</span></span>
<span data-ttu-id="c8769-114">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c8769-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8769-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8769-115">-WhatIf</span></span>
<span data-ttu-id="c8769-116">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8769-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8769-117">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c8769-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8769-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8769-118">CommonParameters</span></span>
<span data-ttu-id="c8769-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8769-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8769-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8769-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8769-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8769-121">INPUTS</span></span>

### <span data-ttu-id="c8769-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="c8769-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c8769-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8769-123">OUTPUTS</span></span>

### <span data-ttu-id="c8769-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="c8769-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c8769-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c8769-125">NOTES</span></span>

## <span data-ttu-id="c8769-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8769-126">RELATED LINKS</span></span>

[<span data-ttu-id="c8769-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8769-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="c8769-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8769-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="c8769-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8769-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


