---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: aba554d2c81e4fce438e9bd6e10a8dfec63da465
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570107"
---
# <span data-ttu-id="e109f-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e109f-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="e109f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e109f-102">SYNOPSIS</span></span>
<span data-ttu-id="e109f-103">Возвращает сервер источника сети CDN.</span><span class="sxs-lookup"><span data-stu-id="e109f-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e109f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e109f-104">SYNTAX</span></span>

### <span data-ttu-id="e109f-105">Параметры, заданные для параметров полей (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e109f-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e109f-106">Параметр, заданный для параметров объекта</span><span class="sxs-lookup"><span data-stu-id="e109f-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e109f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e109f-107">DESCRIPTION</span></span>
<span data-ttu-id="e109f-108">Командлет **Get-AzureRmCdnOrigin** получает исходный сервер сети доставки содержимого (CDN) для Azure и данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e109f-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="e109f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e109f-109">EXAMPLES</span></span>

## <span data-ttu-id="e109f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e109f-110">PARAMETERS</span></span>

### <span data-ttu-id="e109f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e109f-111">-CdnEndpoint</span></span>
<span data-ttu-id="e109f-112">Указывает объект конечной точки сети CDN, к которому относится источник.</span><span class="sxs-lookup"><span data-stu-id="e109f-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e109f-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e109f-113">-EndpointName</span></span>
<span data-ttu-id="e109f-114">Указывает имя конечной точки, к которой принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="e109f-114">Specifies the name of the endpoint to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e109f-115">-OriginName</span><span class="sxs-lookup"><span data-stu-id="e109f-115">-OriginName</span></span>
<span data-ttu-id="e109f-116">Указывает имя исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="e109f-116">Specifies the name of the origin server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e109f-117">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="e109f-117">-ProfileName</span></span>
<span data-ttu-id="e109f-118">Указывает имя профиля, которому принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="e109f-118">Specifies the name of the profile to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e109f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e109f-119">-ResourceGroupName</span></span>
<span data-ttu-id="e109f-120">Указывает имя группы ресурсов, к которой принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="e109f-120">Specifies the name of the resource group to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e109f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e109f-121">-DefaultProfile</span></span>
<span data-ttu-id="e109f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e109f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e109f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e109f-123">CommonParameters</span></span>
<span data-ttu-id="e109f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e109f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e109f-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e109f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e109f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e109f-126">INPUTS</span></span>

### <span data-ttu-id="e109f-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e109f-127">PSEndpoint</span></span>
<span data-ttu-id="e109f-128">Параметр "CdnEndpoint" принимает значение типа "PSEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e109f-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="e109f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e109f-129">OUTPUTS</span></span>

###  
<span data-ttu-id="e109f-130">Этот командлет возвращает объект исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="e109f-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="e109f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e109f-131">NOTES</span></span>

## <span data-ttu-id="e109f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e109f-132">RELATED LINKS</span></span>

[<span data-ttu-id="e109f-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e109f-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


