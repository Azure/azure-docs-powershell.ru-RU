---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: 8e294b457d93c5e9aeb9f8391fccdedc3ccfd778
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565634"
---
# <span data-ttu-id="d79da-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d79da-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="d79da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d79da-102">SYNOPSIS</span></span>
<span data-ttu-id="d79da-103">Обновляет профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="d79da-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d79da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d79da-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d79da-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d79da-105">DESCRIPTION</span></span>
<span data-ttu-id="d79da-106">Командлет **Set-AzureRmCdnProfile** обновляет профиль сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="d79da-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="d79da-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d79da-107">EXAMPLES</span></span>

## <span data-ttu-id="d79da-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d79da-108">PARAMETERS</span></span>

### <span data-ttu-id="d79da-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="d79da-109">-CdnProfile</span></span>
<span data-ttu-id="d79da-110">Указывает профиль, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d79da-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="d79da-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d79da-111">-Confirm</span></span>
<span data-ttu-id="d79da-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d79da-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d79da-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d79da-113">-WhatIf</span></span>
<span data-ttu-id="d79da-114">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d79da-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d79da-115">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d79da-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d79da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79da-116">-DefaultProfile</span></span>
<span data-ttu-id="d79da-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d79da-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d79da-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79da-118">CommonParameters</span></span>
<span data-ttu-id="d79da-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d79da-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79da-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d79da-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79da-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d79da-121">INPUTS</span></span>

### <span data-ttu-id="d79da-122">PSProfile</span><span class="sxs-lookup"><span data-stu-id="d79da-122">PSProfile</span></span>
<span data-ttu-id="d79da-123">Параметр "CdnProfile" принимает значение типа "PSProfile" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d79da-123">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="d79da-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d79da-124">OUTPUTS</span></span>

### <span data-ttu-id="d79da-125">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="d79da-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="d79da-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="d79da-126">NOTES</span></span>

## <span data-ttu-id="d79da-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d79da-127">RELATED LINKS</span></span>

[<span data-ttu-id="d79da-128">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d79da-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="d79da-129">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d79da-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="d79da-130">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d79da-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


