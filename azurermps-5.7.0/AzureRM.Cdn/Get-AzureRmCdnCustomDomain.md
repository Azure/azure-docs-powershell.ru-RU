---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: b87963b45010299dcb80c4b1859af8614f845526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559272"
---
# <span data-ttu-id="7d8b7-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7d8b7-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="7d8b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8b7-103">Получает настраиваемый домен CDN.</span><span class="sxs-lookup"><span data-stu-id="7d8b7-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d8b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d8b7-104">SYNTAX</span></span>

### <span data-ttu-id="7d8b7-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d8b7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d8b7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d8b7-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d8b7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d8b7-107">DESCRIPTION</span></span>
<span data-ttu-id="7d8b7-108">Командлет **Get-AzureRmCdnCustomDomain** получает настраиваемый домен сети доставки содержимого (CDN) для Azure и связанные с ним параметры.</span><span class="sxs-lookup"><span data-stu-id="7d8b7-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="7d8b7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d8b7-109">EXAMPLES</span></span>

## <span data-ttu-id="7d8b7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d8b7-110">PARAMETERS</span></span>

### <span data-ttu-id="7d8b7-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d8b7-111">-CdnEndpoint</span></span>
<span data-ttu-id="7d8b7-112">Указывает объект конечной точки CDN, членом которого является настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="7d8b7-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d8b7-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7d8b7-113">-CustomDomainName</span></span>
<span data-ttu-id="7d8b7-114">Указывает имя настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="7d8b7-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="7d8b7-115">Имя настраиваемого домена отличается от имени узла настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="7d8b7-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8b7-116">-DefaultProfile</span></span>
<span data-ttu-id="7d8b7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7d8b7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d8b7-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7d8b7-118">-EndpointName</span></span>
<span data-ttu-id="7d8b7-119">Указывает имя конечной точки, к которой принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="7d8b7-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="7d8b7-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="7d8b7-120">-ProfileName</span></span>
<span data-ttu-id="7d8b7-121">Указывает имя профиля, которому принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="7d8b7-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="7d8b7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d8b7-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d8b7-123">Указывает имя группы ресурсов, к которой принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="7d8b7-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="7d8b7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8b7-124">CommonParameters</span></span>
<span data-ttu-id="7d8b7-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d8b7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8b7-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d8b7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8b7-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d8b7-127">INPUTS</span></span>

### <span data-ttu-id="7d8b7-128">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d8b7-128">PSEndpoint</span></span>
<span data-ttu-id="7d8b7-129">Параметр "CdnEndpoint" принимает значение типа "PSEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7d8b7-129">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="7d8b7-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d8b7-130">OUTPUTS</span></span>

###  
<span data-ttu-id="7d8b7-131">Этот командлет возвращает настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="7d8b7-131">This cmdlet returns a custom domain object.</span></span>

## <span data-ttu-id="7d8b7-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d8b7-132">NOTES</span></span>

## <span data-ttu-id="7d8b7-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d8b7-133">RELATED LINKS</span></span>

[<span data-ttu-id="7d8b7-134">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7d8b7-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="7d8b7-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7d8b7-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


