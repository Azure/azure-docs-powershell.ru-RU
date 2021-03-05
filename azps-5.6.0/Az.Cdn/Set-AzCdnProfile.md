---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 88e10d5f887d290139ee465217756c598bef0a3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975496"
---
# <span data-ttu-id="09ace-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="09ace-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="09ace-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09ace-102">SYNOPSIS</span></span>
<span data-ttu-id="09ace-103">Обновляет профиль сети CDN.</span><span class="sxs-lookup"><span data-stu-id="09ace-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="09ace-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="09ace-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09ace-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09ace-105">DESCRIPTION</span></span>
<span data-ttu-id="09ace-106">**Настройка Set-AzCdnProfile** обновляет профиль сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="09ace-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="09ace-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="09ace-107">EXAMPLES</span></span>

## <span data-ttu-id="09ace-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09ace-108">PARAMETERS</span></span>

### <span data-ttu-id="09ace-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="09ace-109">-CdnProfile</span></span>
<span data-ttu-id="09ace-110">Определяет профиль, который обновляется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09ace-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="09ace-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ace-111">-DefaultProfile</span></span>
<span data-ttu-id="09ace-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="09ace-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09ace-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09ace-113">-Confirm</span></span>
<span data-ttu-id="09ace-114">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="09ace-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09ace-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09ace-115">-WhatIf</span></span>
<span data-ttu-id="09ace-116">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09ace-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09ace-117">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="09ace-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09ace-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ace-118">CommonParameters</span></span>
<span data-ttu-id="09ace-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09ace-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ace-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09ace-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ace-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09ace-121">INPUTS</span></span>

### <span data-ttu-id="09ace-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="09ace-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="09ace-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="09ace-123">OUTPUTS</span></span>

### <span data-ttu-id="09ace-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="09ace-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="09ace-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="09ace-125">NOTES</span></span>

## <span data-ttu-id="09ace-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09ace-126">RELATED LINKS</span></span>

[<span data-ttu-id="09ace-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="09ace-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="09ace-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="09ace-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="09ace-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="09ace-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


