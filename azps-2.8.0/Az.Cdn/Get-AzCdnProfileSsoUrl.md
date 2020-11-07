---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: e32d8312d0046786e6fd36ce30e525241fe78c6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727597"
---
# <span data-ttu-id="dcf5f-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="dcf5f-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="dcf5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcf5f-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf5f-103">Возвращает URL-адрес для единого входа в профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="dcf5f-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="dcf5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcf5f-104">SYNTAX</span></span>

### <span data-ttu-id="dcf5f-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcf5f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcf5f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcf5f-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcf5f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcf5f-107">DESCRIPTION</span></span>
<span data-ttu-id="dcf5f-108">Командлет **Get-AzCdnProfileSsoUrl** получает URL-адрес единого входа для профиля сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="dcf5f-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="dcf5f-109">Этот URL-адрес позволяет пользователям подключаться к вспомогательному порталу и использовать дополнительные функции сети CDN.</span><span class="sxs-lookup"><span data-stu-id="dcf5f-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="dcf5f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcf5f-110">EXAMPLES</span></span>

## <span data-ttu-id="dcf5f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcf5f-111">PARAMETERS</span></span>

### <span data-ttu-id="dcf5f-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="dcf5f-112">-CdnProfile</span></span>
<span data-ttu-id="dcf5f-113">Задает профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="dcf5f-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="dcf5f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf5f-114">-DefaultProfile</span></span>
<span data-ttu-id="dcf5f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dcf5f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcf5f-116">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="dcf5f-116">-ProfileName</span></span>
<span data-ttu-id="dcf5f-117">Указывает имя профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="dcf5f-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="dcf5f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcf5f-118">-ResourceGroupName</span></span>
<span data-ttu-id="dcf5f-119">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="dcf5f-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="dcf5f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf5f-120">CommonParameters</span></span>
<span data-ttu-id="dcf5f-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcf5f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf5f-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcf5f-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf5f-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcf5f-123">INPUTS</span></span>

### <span data-ttu-id="dcf5f-124">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="dcf5f-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="dcf5f-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcf5f-125">OUTPUTS</span></span>

### <span data-ttu-id="dcf5f-126">Microsoft. Azure. Commands. CDN. Models. Profile. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="dcf5f-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="dcf5f-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcf5f-127">NOTES</span></span>

## <span data-ttu-id="dcf5f-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcf5f-128">RELATED LINKS</span></span>

[<span data-ttu-id="dcf5f-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="dcf5f-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


