---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: e80b82f567dd1c0935dd56d8e3996a63bcce72e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565885"
---
# <span data-ttu-id="4d33a-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4d33a-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="4d33a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d33a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d33a-103">Обновляет профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="4d33a-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d33a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d33a-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d33a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d33a-105">DESCRIPTION</span></span>
<span data-ttu-id="4d33a-106">Командлет **Set-AzureRmCdnProfile** обновляет профиль сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="4d33a-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="4d33a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d33a-107">EXAMPLES</span></span>

## <span data-ttu-id="4d33a-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d33a-108">PARAMETERS</span></span>

### <span data-ttu-id="4d33a-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="4d33a-109">-CdnProfile</span></span>
<span data-ttu-id="4d33a-110">Указывает профиль, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4d33a-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="4d33a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d33a-111">-DefaultProfile</span></span>
<span data-ttu-id="4d33a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4d33a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d33a-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d33a-113">-Confirm</span></span>
<span data-ttu-id="4d33a-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4d33a-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d33a-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d33a-115">-WhatIf</span></span>
<span data-ttu-id="4d33a-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d33a-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d33a-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4d33a-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d33a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d33a-118">CommonParameters</span></span>
<span data-ttu-id="4d33a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d33a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d33a-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d33a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d33a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d33a-121">INPUTS</span></span>

### <span data-ttu-id="4d33a-122">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="4d33a-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="4d33a-123">Параметры: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d33a-123">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="4d33a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d33a-124">OUTPUTS</span></span>

### <span data-ttu-id="4d33a-125">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="4d33a-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="4d33a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d33a-126">NOTES</span></span>

## <span data-ttu-id="4d33a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d33a-127">RELATED LINKS</span></span>

[<span data-ttu-id="4d33a-128">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4d33a-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="4d33a-129">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4d33a-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="4d33a-130">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4d33a-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


