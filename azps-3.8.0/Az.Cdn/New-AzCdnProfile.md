---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
ms.openlocfilehash: 6c17b3732cf5eab46f5826896dacafd3639aa788
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072844"
---
# <span data-ttu-id="7a7f3-101">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7a7f3-101">New-AzCdnProfile</span></span>

## <span data-ttu-id="7a7f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a7f3-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7f3-103">Создание профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="7a7f3-103">Creates a CDN profile.</span></span>

## <span data-ttu-id="7a7f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a7f3-104">SYNTAX</span></span>

```
New-AzCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a7f3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a7f3-105">DESCRIPTION</span></span>
<span data-ttu-id="7a7f3-106">Командлет **New-AzCdnProfile** создает профиль сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="7a7f3-106">The **New-AzCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="7a7f3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a7f3-107">EXAMPLES</span></span>

## <span data-ttu-id="7a7f3-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a7f3-108">PARAMETERS</span></span>

### <span data-ttu-id="7a7f3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7f3-109">-DefaultProfile</span></span>
<span data-ttu-id="7a7f3-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7a7f3-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a7f3-111">-Location</span><span class="sxs-lookup"><span data-stu-id="7a7f3-111">-Location</span></span>
<span data-ttu-id="7a7f3-112">Указывает расположение ресурса для профиля.</span><span class="sxs-lookup"><span data-stu-id="7a7f3-112">Specifies the resource location of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a7f3-113">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="7a7f3-113">-ProfileName</span></span>
<span data-ttu-id="7a7f3-114">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="7a7f3-114">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="7a7f3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a7f3-115">-ResourceGroupName</span></span>
<span data-ttu-id="7a7f3-116">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="7a7f3-116">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="7a7f3-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="7a7f3-117">-Sku</span></span>
<span data-ttu-id="7a7f3-118">Указывает SKU профиля.</span><span class="sxs-lookup"><span data-stu-id="7a7f3-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn, Standard_Microsoft

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a7f3-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="7a7f3-119">-Tag</span></span>
<span data-ttu-id="7a7f3-120">Теги, связываемые с профилем CDN в Azure.</span><span class="sxs-lookup"><span data-stu-id="7a7f3-120">The tags to associate with the Azure CDN profile.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a7f3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a7f3-121">-Confirm</span></span>
<span data-ttu-id="7a7f3-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a7f3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a7f3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a7f3-123">-WhatIf</span></span>
<span data-ttu-id="7a7f3-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a7f3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a7f3-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a7f3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a7f3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7f3-126">CommonParameters</span></span>
<span data-ttu-id="7a7f3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a7f3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7f3-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a7f3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7f3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a7f3-129">INPUTS</span></span>

### <span data-ttu-id="7a7f3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7a7f3-130">System.String</span></span>

## <span data-ttu-id="7a7f3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a7f3-131">OUTPUTS</span></span>

### <span data-ttu-id="7a7f3-132">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="7a7f3-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="7a7f3-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a7f3-133">NOTES</span></span>

## <span data-ttu-id="7a7f3-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a7f3-134">RELATED LINKS</span></span>

[<span data-ttu-id="7a7f3-135">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7a7f3-135">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="7a7f3-136">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7a7f3-136">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="7a7f3-137">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7a7f3-137">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


