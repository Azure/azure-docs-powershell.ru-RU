---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: 0e69e48d29c96163acbb82ffe691de6affe8d131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567160"
---
# <span data-ttu-id="85315-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="85315-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="85315-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85315-102">SYNOPSIS</span></span>
<span data-ttu-id="85315-103">Создание профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="85315-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85315-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85315-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85315-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85315-105">DESCRIPTION</span></span>
<span data-ttu-id="85315-106">Командлет **New-AzureRmCdnProfile** создает профиль сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="85315-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="85315-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85315-107">EXAMPLES</span></span>

## <span data-ttu-id="85315-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85315-108">PARAMETERS</span></span>

### <span data-ttu-id="85315-109">-Location</span><span class="sxs-lookup"><span data-stu-id="85315-109">-Location</span></span>
<span data-ttu-id="85315-110">Указывает расположение ресурса для профиля.</span><span class="sxs-lookup"><span data-stu-id="85315-110">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="85315-111">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="85315-111">-ProfileName</span></span>
<span data-ttu-id="85315-112">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="85315-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="85315-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85315-113">-ResourceGroupName</span></span>
<span data-ttu-id="85315-114">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="85315-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="85315-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="85315-115">-Sku</span></span>
<span data-ttu-id="85315-116">Указывает SKU профиля.</span><span class="sxs-lookup"><span data-stu-id="85315-116">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85315-117">-Теги</span><span class="sxs-lookup"><span data-stu-id="85315-117">-Tags</span></span>
<span data-ttu-id="85315-118">Sepcifies хэш-таблицу тегов, связанных с этим профилем.</span><span class="sxs-lookup"><span data-stu-id="85315-118">Sepcifies a hash table of tags that are associated with this profile.</span></span>

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

### <span data-ttu-id="85315-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85315-119">-Confirm</span></span>
<span data-ttu-id="85315-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="85315-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85315-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85315-121">-WhatIf</span></span>
<span data-ttu-id="85315-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="85315-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85315-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="85315-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85315-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85315-124">-DefaultProfile</span></span>
<span data-ttu-id="85315-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85315-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85315-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85315-126">CommonParameters</span></span>
<span data-ttu-id="85315-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85315-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85315-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85315-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85315-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85315-129">INPUTS</span></span>

## <span data-ttu-id="85315-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85315-130">OUTPUTS</span></span>

### <span data-ttu-id="85315-131">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="85315-131">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="85315-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="85315-132">NOTES</span></span>

## <span data-ttu-id="85315-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85315-133">RELATED LINKS</span></span>

[<span data-ttu-id="85315-134">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="85315-134">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="85315-135">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="85315-135">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="85315-136">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="85315-136">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


