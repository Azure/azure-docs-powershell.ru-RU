---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
ms.openlocfilehash: 703b686f11d7d55cc77bcfde929f9a9f261070f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731406"
---
# <span data-ttu-id="667ac-101">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="667ac-101">New-AzCdnProfile</span></span>

## <span data-ttu-id="667ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="667ac-102">SYNOPSIS</span></span>
<span data-ttu-id="667ac-103">Создание профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="667ac-103">Creates a CDN profile.</span></span>

## <span data-ttu-id="667ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="667ac-104">SYNTAX</span></span>

```
New-AzCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="667ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="667ac-105">DESCRIPTION</span></span>
<span data-ttu-id="667ac-106">Командлет **New-AzCdnProfile** создает профиль сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="667ac-106">The **New-AzCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="667ac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="667ac-107">EXAMPLES</span></span>

## <span data-ttu-id="667ac-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="667ac-108">PARAMETERS</span></span>

### <span data-ttu-id="667ac-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667ac-109">-DefaultProfile</span></span>
<span data-ttu-id="667ac-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="667ac-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="667ac-111">-Location</span><span class="sxs-lookup"><span data-stu-id="667ac-111">-Location</span></span>
<span data-ttu-id="667ac-112">Указывает расположение ресурса для профиля.</span><span class="sxs-lookup"><span data-stu-id="667ac-112">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="667ac-113">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="667ac-113">-ProfileName</span></span>
<span data-ttu-id="667ac-114">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="667ac-114">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="667ac-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667ac-115">-ResourceGroupName</span></span>
<span data-ttu-id="667ac-116">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="667ac-116">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="667ac-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="667ac-117">-Sku</span></span>
<span data-ttu-id="667ac-118">Указывает SKU профиля.</span><span class="sxs-lookup"><span data-stu-id="667ac-118">Specifies the SKU of the profile.</span></span>

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

### <span data-ttu-id="667ac-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="667ac-119">-Tag</span></span>
<span data-ttu-id="667ac-120">Теги, связываемые с профилем CDN в Azure.</span><span class="sxs-lookup"><span data-stu-id="667ac-120">The tags to associate with the Azure CDN profile.</span></span>

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

### <span data-ttu-id="667ac-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="667ac-121">-Confirm</span></span>
<span data-ttu-id="667ac-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="667ac-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="667ac-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="667ac-123">-WhatIf</span></span>
<span data-ttu-id="667ac-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="667ac-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="667ac-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="667ac-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="667ac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667ac-126">CommonParameters</span></span>
<span data-ttu-id="667ac-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="667ac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667ac-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="667ac-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667ac-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="667ac-129">INPUTS</span></span>

### <span data-ttu-id="667ac-130">System. String</span><span class="sxs-lookup"><span data-stu-id="667ac-130">System.String</span></span>

## <span data-ttu-id="667ac-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="667ac-131">OUTPUTS</span></span>

### <span data-ttu-id="667ac-132">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="667ac-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="667ac-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="667ac-133">NOTES</span></span>

## <span data-ttu-id="667ac-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="667ac-134">RELATED LINKS</span></span>

[<span data-ttu-id="667ac-135">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="667ac-135">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="667ac-136">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="667ac-136">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="667ac-137">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="667ac-137">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


