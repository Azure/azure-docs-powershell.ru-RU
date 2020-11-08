---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078162"
---
# <span data-ttu-id="e8ec9-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e8ec9-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="e8ec9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ec9-103">Получает профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="e8ec9-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="e8ec9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8ec9-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8ec9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8ec9-105">DESCRIPTION</span></span>
<span data-ttu-id="e8ec9-106">Командлет **Get-AzCdnProfile** получает профиль сети доставки содержимого (CDN) для Azure и связанную с ней информацию.</span><span class="sxs-lookup"><span data-stu-id="e8ec9-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="e8ec9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8ec9-107">EXAMPLES</span></span>

## <span data-ttu-id="e8ec9-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8ec9-108">PARAMETERS</span></span>

### <span data-ttu-id="e8ec9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ec9-109">-DefaultProfile</span></span>
<span data-ttu-id="e8ec9-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e8ec9-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8ec9-111">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="e8ec9-111">-ProfileName</span></span>
<span data-ttu-id="e8ec9-112">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="e8ec9-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="e8ec9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ec9-113">-ResourceGroupName</span></span>
<span data-ttu-id="e8ec9-114">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="e8ec9-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="e8ec9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ec9-115">CommonParameters</span></span>
<span data-ttu-id="e8ec9-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8ec9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ec9-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8ec9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ec9-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8ec9-118">INPUTS</span></span>

### <span data-ttu-id="e8ec9-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e8ec9-119">System.String</span></span>

## <span data-ttu-id="e8ec9-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8ec9-120">OUTPUTS</span></span>

### <span data-ttu-id="e8ec9-121">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="e8ec9-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="e8ec9-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8ec9-122">NOTES</span></span>

## <span data-ttu-id="e8ec9-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8ec9-123">RELATED LINKS</span></span>

[<span data-ttu-id="e8ec9-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e8ec9-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="e8ec9-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e8ec9-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="e8ec9-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e8ec9-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


