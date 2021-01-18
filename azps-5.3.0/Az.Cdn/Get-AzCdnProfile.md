---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519712"
---
# <span data-ttu-id="63e3d-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="63e3d-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="63e3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="63e3d-103">Получает профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="63e3d-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="63e3d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="63e3d-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63e3d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63e3d-105">DESCRIPTION</span></span>
<span data-ttu-id="63e3d-106">Для получения профиля сети доставки содержимого (CDN) Azure и связанных с ним данных с его использованием можно получить **cmddnProfile Get-AzCdnProfile.**</span><span class="sxs-lookup"><span data-stu-id="63e3d-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="63e3d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="63e3d-107">EXAMPLES</span></span>

## <span data-ttu-id="63e3d-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63e3d-108">PARAMETERS</span></span>

### <span data-ttu-id="63e3d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e3d-109">-DefaultProfile</span></span>
<span data-ttu-id="63e3d-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="63e3d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63e3d-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="63e3d-111">-ProfileName</span></span>
<span data-ttu-id="63e3d-112">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="63e3d-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="63e3d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e3d-113">-ResourceGroupName</span></span>
<span data-ttu-id="63e3d-114">Имя группы ресурсов, к которой принадлежит профиль.</span><span class="sxs-lookup"><span data-stu-id="63e3d-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="63e3d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e3d-115">CommonParameters</span></span>
<span data-ttu-id="63e3d-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e3d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e3d-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63e3d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e3d-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63e3d-118">INPUTS</span></span>

### <span data-ttu-id="63e3d-119">System.String</span><span class="sxs-lookup"><span data-stu-id="63e3d-119">System.String</span></span>

## <span data-ttu-id="63e3d-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="63e3d-120">OUTPUTS</span></span>

### <span data-ttu-id="63e3d-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="63e3d-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="63e3d-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="63e3d-122">NOTES</span></span>

## <span data-ttu-id="63e3d-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63e3d-123">RELATED LINKS</span></span>

[<span data-ttu-id="63e3d-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="63e3d-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="63e3d-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="63e3d-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="63e3d-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="63e3d-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


