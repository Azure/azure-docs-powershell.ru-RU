---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073685"
---
# <span data-ttu-id="9ef2f-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9ef2f-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="9ef2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ef2f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef2f-103">Получает профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="9ef2f-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="9ef2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ef2f-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ef2f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ef2f-105">DESCRIPTION</span></span>
<span data-ttu-id="9ef2f-106">Командлет **Get-AzCdnProfile** получает профиль сети доставки содержимого (CDN) для Azure и связанную с ней информацию.</span><span class="sxs-lookup"><span data-stu-id="9ef2f-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="9ef2f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ef2f-107">EXAMPLES</span></span>

## <span data-ttu-id="9ef2f-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ef2f-108">PARAMETERS</span></span>

### <span data-ttu-id="9ef2f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef2f-109">-DefaultProfile</span></span>
<span data-ttu-id="9ef2f-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9ef2f-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ef2f-111">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="9ef2f-111">-ProfileName</span></span>
<span data-ttu-id="9ef2f-112">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="9ef2f-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="9ef2f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef2f-113">-ResourceGroupName</span></span>
<span data-ttu-id="9ef2f-114">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="9ef2f-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="9ef2f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef2f-115">CommonParameters</span></span>
<span data-ttu-id="9ef2f-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ef2f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef2f-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ef2f-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef2f-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ef2f-118">INPUTS</span></span>

### <span data-ttu-id="9ef2f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="9ef2f-119">System.String</span></span>

## <span data-ttu-id="9ef2f-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ef2f-120">OUTPUTS</span></span>

### <span data-ttu-id="9ef2f-121">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="9ef2f-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="9ef2f-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ef2f-122">NOTES</span></span>

## <span data-ttu-id="9ef2f-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ef2f-123">RELATED LINKS</span></span>

[<span data-ttu-id="9ef2f-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9ef2f-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="9ef2f-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9ef2f-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="9ef2f-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9ef2f-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


