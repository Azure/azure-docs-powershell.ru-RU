---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 74bc4fae4dd55a85c4aca811819a0348f5df5f2c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519711"
---
# <span data-ttu-id="5d4b4-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="5d4b4-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="5d4b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d4b4-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4b4-103">Получает URL-адрес единого вход в профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="5d4b4-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="5d4b4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5d4b4-104">SYNTAX</span></span>

### <span data-ttu-id="5d4b4-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d4b4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d4b4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d4b4-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d4b4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d4b4-107">DESCRIPTION</span></span>
<span data-ttu-id="5d4b4-108">Cmdlet **Get-AzCdnProfileSsoUrl** получает URL-адрес единого входного адреса профиля сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="5d4b4-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="5d4b4-109">Этот URL-адрес позволяет пользователям подключаться к дополнительному порталу и использовать дополнительные возможности сети CDN.</span><span class="sxs-lookup"><span data-stu-id="5d4b4-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="5d4b4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5d4b4-110">EXAMPLES</span></span>

## <span data-ttu-id="5d4b4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d4b4-111">PARAMETERS</span></span>

### <span data-ttu-id="5d4b4-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="5d4b4-112">-CdnProfile</span></span>
<span data-ttu-id="5d4b4-113">Определяет профиль сети CDN.</span><span class="sxs-lookup"><span data-stu-id="5d4b4-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="5d4b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d4b4-114">-DefaultProfile</span></span>
<span data-ttu-id="5d4b4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5d4b4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d4b4-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5d4b4-116">-ProfileName</span></span>
<span data-ttu-id="5d4b4-117">Указывает имя профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="5d4b4-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="5d4b4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d4b4-118">-ResourceGroupName</span></span>
<span data-ttu-id="5d4b4-119">Имя группы ресурсов, к которой принадлежит профиль.</span><span class="sxs-lookup"><span data-stu-id="5d4b4-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="5d4b4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4b4-120">CommonParameters</span></span>
<span data-ttu-id="5d4b4-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d4b4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4b4-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d4b4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4b4-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d4b4-123">INPUTS</span></span>

### <span data-ttu-id="5d4b4-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="5d4b4-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="5d4b4-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5d4b4-125">OUTPUTS</span></span>

### <span data-ttu-id="5d4b4-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="5d4b4-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="5d4b4-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5d4b4-127">NOTES</span></span>

## <span data-ttu-id="5d4b4-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d4b4-128">RELATED LINKS</span></span>

[<span data-ttu-id="5d4b4-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5d4b4-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


