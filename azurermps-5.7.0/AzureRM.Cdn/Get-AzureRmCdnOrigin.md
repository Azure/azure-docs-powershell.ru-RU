---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: b4800b77441a82fc0e9966be16f91c9d81a2214a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732171"
---
# <span data-ttu-id="d8494-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="d8494-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="d8494-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8494-102">SYNOPSIS</span></span>
<span data-ttu-id="d8494-103">Возвращает сервер источника сети CDN.</span><span class="sxs-lookup"><span data-stu-id="d8494-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8494-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8494-104">SYNTAX</span></span>

### <span data-ttu-id="d8494-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8494-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8494-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8494-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8494-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8494-107">DESCRIPTION</span></span>
<span data-ttu-id="d8494-108">Командлет **Get-AzureRmCdnOrigin** получает исходный сервер сети доставки содержимого (CDN) для Azure и данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d8494-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="d8494-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8494-109">EXAMPLES</span></span>

## <span data-ttu-id="d8494-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8494-110">PARAMETERS</span></span>

### <span data-ttu-id="d8494-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8494-111">-CdnEndpoint</span></span>
<span data-ttu-id="d8494-112">Указывает объект конечной точки сети CDN, к которому относится источник.</span><span class="sxs-lookup"><span data-stu-id="d8494-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="d8494-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8494-113">-DefaultProfile</span></span>
<span data-ttu-id="d8494-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d8494-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8494-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d8494-115">-EndpointName</span></span>
<span data-ttu-id="d8494-116">Указывает имя конечной точки, к которой принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="d8494-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="d8494-117">-OriginName</span><span class="sxs-lookup"><span data-stu-id="d8494-117">-OriginName</span></span>
<span data-ttu-id="d8494-118">Указывает имя исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="d8494-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="d8494-119">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="d8494-119">-ProfileName</span></span>
<span data-ttu-id="d8494-120">Указывает имя профиля, которому принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="d8494-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="d8494-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8494-121">-ResourceGroupName</span></span>
<span data-ttu-id="d8494-122">Указывает имя группы ресурсов, к которой принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="d8494-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="d8494-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8494-123">CommonParameters</span></span>
<span data-ttu-id="d8494-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8494-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8494-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8494-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8494-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8494-126">INPUTS</span></span>

### <span data-ttu-id="d8494-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8494-127">PSEndpoint</span></span>
<span data-ttu-id="d8494-128">Параметр "CdnEndpoint" принимает значение типа "PSEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d8494-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="d8494-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8494-129">OUTPUTS</span></span>

###  
<span data-ttu-id="d8494-130">Этот командлет возвращает объект исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="d8494-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="d8494-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8494-131">NOTES</span></span>

## <span data-ttu-id="d8494-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8494-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8494-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="d8494-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


