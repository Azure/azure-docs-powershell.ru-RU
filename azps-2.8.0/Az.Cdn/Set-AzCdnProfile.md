---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 6cfc4a418f92a5e30a36c0f2317aef93226d72cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727567"
---
# <span data-ttu-id="1f403-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1f403-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="1f403-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f403-102">SYNOPSIS</span></span>
<span data-ttu-id="1f403-103">Обновляет профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="1f403-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="1f403-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f403-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f403-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f403-105">DESCRIPTION</span></span>
<span data-ttu-id="1f403-106">Командлет **Set-AzCdnProfile** обновляет профиль сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="1f403-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="1f403-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f403-107">EXAMPLES</span></span>

## <span data-ttu-id="1f403-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f403-108">PARAMETERS</span></span>

### <span data-ttu-id="1f403-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="1f403-109">-CdnProfile</span></span>
<span data-ttu-id="1f403-110">Указывает профиль, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="1f403-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="1f403-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f403-111">-DefaultProfile</span></span>
<span data-ttu-id="1f403-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1f403-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f403-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f403-113">-Confirm</span></span>
<span data-ttu-id="1f403-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f403-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f403-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f403-115">-WhatIf</span></span>
<span data-ttu-id="1f403-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f403-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f403-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f403-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f403-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f403-118">CommonParameters</span></span>
<span data-ttu-id="1f403-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f403-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f403-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f403-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f403-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f403-121">INPUTS</span></span>

### <span data-ttu-id="1f403-122">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="1f403-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="1f403-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f403-123">OUTPUTS</span></span>

### <span data-ttu-id="1f403-124">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="1f403-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="1f403-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f403-125">NOTES</span></span>

## <span data-ttu-id="1f403-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f403-126">RELATED LINKS</span></span>

[<span data-ttu-id="1f403-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1f403-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="1f403-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1f403-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="1f403-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1f403-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


