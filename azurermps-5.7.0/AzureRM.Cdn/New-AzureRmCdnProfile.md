---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: 5423844d7f466a827f3a452a05cf3999236198d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559252"
---
# <span data-ttu-id="d62bc-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d62bc-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="d62bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d62bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d62bc-103">Создание профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="d62bc-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d62bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d62bc-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d62bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d62bc-105">DESCRIPTION</span></span>
<span data-ttu-id="d62bc-106">Командлет **New-AzureRmCdnProfile** создает профиль сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="d62bc-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="d62bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d62bc-107">EXAMPLES</span></span>

## <span data-ttu-id="d62bc-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d62bc-108">PARAMETERS</span></span>

### <span data-ttu-id="d62bc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d62bc-109">-DefaultProfile</span></span>
<span data-ttu-id="d62bc-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d62bc-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d62bc-111">-Location</span><span class="sxs-lookup"><span data-stu-id="d62bc-111">-Location</span></span>
<span data-ttu-id="d62bc-112">Указывает расположение ресурса для профиля.</span><span class="sxs-lookup"><span data-stu-id="d62bc-112">Specifies the resource location of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d62bc-113">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="d62bc-113">-ProfileName</span></span>
<span data-ttu-id="d62bc-114">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="d62bc-114">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d62bc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d62bc-115">-ResourceGroupName</span></span>
<span data-ttu-id="d62bc-116">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="d62bc-116">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d62bc-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="d62bc-117">-Sku</span></span>
<span data-ttu-id="d62bc-118">Указывает SKU профиля.</span><span class="sxs-lookup"><span data-stu-id="d62bc-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d62bc-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="d62bc-119">-Tag</span></span>
<span data-ttu-id="d62bc-120">Теги, связываемые с профилем CDN в Azure.</span><span class="sxs-lookup"><span data-stu-id="d62bc-120">The tags to associate with the Azure CDN profile.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d62bc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d62bc-121">-Confirm</span></span>
<span data-ttu-id="d62bc-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d62bc-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d62bc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d62bc-123">-WhatIf</span></span>
<span data-ttu-id="d62bc-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d62bc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d62bc-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d62bc-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d62bc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d62bc-126">CommonParameters</span></span>
<span data-ttu-id="d62bc-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d62bc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d62bc-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d62bc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d62bc-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d62bc-129">INPUTS</span></span>

### <span data-ttu-id="d62bc-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="d62bc-130">None</span></span>
<span data-ttu-id="d62bc-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d62bc-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d62bc-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d62bc-132">OUTPUTS</span></span>

### <span data-ttu-id="d62bc-133">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="d62bc-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="d62bc-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="d62bc-134">NOTES</span></span>

## <span data-ttu-id="d62bc-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d62bc-135">RELATED LINKS</span></span>

[<span data-ttu-id="d62bc-136">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d62bc-136">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="d62bc-137">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d62bc-137">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="d62bc-138">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d62bc-138">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


