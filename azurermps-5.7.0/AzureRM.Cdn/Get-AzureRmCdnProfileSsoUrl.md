---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: d93dadc062f2cc12ed363039d69266daf365920e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559259"
---
# <span data-ttu-id="cd375-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="cd375-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="cd375-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd375-102">SYNOPSIS</span></span>
<span data-ttu-id="cd375-103">Возвращает URL-адрес для единого входа в профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="cd375-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd375-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd375-104">SYNTAX</span></span>

### <span data-ttu-id="cd375-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd375-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd375-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd375-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd375-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd375-107">DESCRIPTION</span></span>
<span data-ttu-id="cd375-108">Командлет **Get-AzureRmCdnProfileSsoUrl** получает URL-адрес единого входа для профиля сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="cd375-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="cd375-109">Этот URL-адрес позволяет пользователям conntect с дополнительным порталом и использовать дополнительные функции сети CDN.</span><span class="sxs-lookup"><span data-stu-id="cd375-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="cd375-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd375-110">EXAMPLES</span></span>

## <span data-ttu-id="cd375-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd375-111">PARAMETERS</span></span>

### <span data-ttu-id="cd375-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="cd375-112">-CdnProfile</span></span>
<span data-ttu-id="cd375-113">Задает профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="cd375-113">Specifies the CDN profile.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd375-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd375-114">-DefaultProfile</span></span>
<span data-ttu-id="cd375-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cd375-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd375-116">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="cd375-116">-ProfileName</span></span>
<span data-ttu-id="cd375-117">Указывает имя профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="cd375-117">Specifies the name of the CDN profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd375-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd375-118">-ResourceGroupName</span></span>
<span data-ttu-id="cd375-119">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="cd375-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd375-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd375-120">CommonParameters</span></span>
<span data-ttu-id="cd375-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd375-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd375-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd375-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd375-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd375-123">INPUTS</span></span>

### <span data-ttu-id="cd375-124">PSProfile</span><span class="sxs-lookup"><span data-stu-id="cd375-124">PSProfile</span></span>
<span data-ttu-id="cd375-125">Параметр "CdnProfile" принимает значение типа "PSProfile" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cd375-125">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="cd375-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd375-126">OUTPUTS</span></span>

###  
<span data-ttu-id="cd375-127">Этот командлет возвращает URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="cd375-127">This cmdlet returns a URL.</span></span>

## <span data-ttu-id="cd375-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd375-128">NOTES</span></span>

## <span data-ttu-id="cd375-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd375-129">RELATED LINKS</span></span>

[<span data-ttu-id="cd375-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cd375-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)


