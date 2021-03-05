---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: c458973a5cff000cab13c4602e1a73234314c0d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963299"
---
# <span data-ttu-id="61d1d-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="61d1d-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="61d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="61d1d-103">Получает URL-адрес единого вход в профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="61d1d-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="61d1d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61d1d-104">SYNTAX</span></span>

### <span data-ttu-id="61d1d-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61d1d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61d1d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61d1d-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61d1d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61d1d-107">DESCRIPTION</span></span>
<span data-ttu-id="61d1d-108">Cmdlet **Get-AzCdnProfileSsoUrl** получает URL-адрес единого входного адреса профиля сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="61d1d-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="61d1d-109">Этот URL-адрес позволяет пользователям подключаться к дополнительному порталу и использовать дополнительные возможности сети CDN.</span><span class="sxs-lookup"><span data-stu-id="61d1d-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="61d1d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61d1d-110">EXAMPLES</span></span>

## <span data-ttu-id="61d1d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61d1d-111">PARAMETERS</span></span>

### <span data-ttu-id="61d1d-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="61d1d-112">-CdnProfile</span></span>
<span data-ttu-id="61d1d-113">Определяет профиль сети CDN.</span><span class="sxs-lookup"><span data-stu-id="61d1d-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61d1d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d1d-114">-DefaultProfile</span></span>
<span data-ttu-id="61d1d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="61d1d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61d1d-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="61d1d-116">-ProfileName</span></span>
<span data-ttu-id="61d1d-117">Указывает имя профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="61d1d-117">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61d1d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61d1d-118">-ResourceGroupName</span></span>
<span data-ttu-id="61d1d-119">Имя группы ресурсов, к которой принадлежит профиль.</span><span class="sxs-lookup"><span data-stu-id="61d1d-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61d1d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d1d-120">CommonParameters</span></span>
<span data-ttu-id="61d1d-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61d1d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d1d-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61d1d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d1d-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61d1d-123">INPUTS</span></span>

### <span data-ttu-id="61d1d-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="61d1d-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="61d1d-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61d1d-125">OUTPUTS</span></span>

### <span data-ttu-id="61d1d-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="61d1d-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="61d1d-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61d1d-127">NOTES</span></span>

## <span data-ttu-id="61d1d-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61d1d-128">RELATED LINKS</span></span>

[<span data-ttu-id="61d1d-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="61d1d-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


