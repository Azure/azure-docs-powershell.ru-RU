---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: f53b02d54164b6cc4e3aad8cf07357e7f2e156e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568218"
---
# <span data-ttu-id="ba138-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ba138-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="ba138-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba138-102">SYNOPSIS</span></span>
<span data-ttu-id="ba138-103">Получает профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="ba138-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba138-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba138-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba138-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba138-105">DESCRIPTION</span></span>
<span data-ttu-id="ba138-106">Командлет **Get-AzureRMCdnProfile** получает профиль сети доставки содержимого (CDN) для Azure и связанную с ней информацию.</span><span class="sxs-lookup"><span data-stu-id="ba138-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="ba138-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba138-107">EXAMPLES</span></span>

## <span data-ttu-id="ba138-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba138-108">PARAMETERS</span></span>

### <span data-ttu-id="ba138-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba138-109">-DefaultProfile</span></span>
<span data-ttu-id="ba138-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ba138-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba138-111">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="ba138-111">-ProfileName</span></span>
<span data-ttu-id="ba138-112">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="ba138-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba138-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba138-113">-ResourceGroupName</span></span>
<span data-ttu-id="ba138-114">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="ba138-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba138-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba138-115">CommonParameters</span></span>
<span data-ttu-id="ba138-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba138-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba138-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba138-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba138-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba138-118">INPUTS</span></span>

### <span data-ttu-id="ba138-119">System. String</span><span class="sxs-lookup"><span data-stu-id="ba138-119">System.String</span></span>

## <span data-ttu-id="ba138-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba138-120">OUTPUTS</span></span>

### <span data-ttu-id="ba138-121">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="ba138-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="ba138-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba138-122">NOTES</span></span>

## <span data-ttu-id="ba138-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba138-123">RELATED LINKS</span></span>

[<span data-ttu-id="ba138-124">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ba138-124">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="ba138-125">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ba138-125">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="ba138-126">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ba138-126">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


