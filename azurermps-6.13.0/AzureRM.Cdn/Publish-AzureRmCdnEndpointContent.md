---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/publish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: a4a2479c6dc7c116ff7da9151fcd5dea5ec26660
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565896"
---
# <span data-ttu-id="5a2a0-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="5a2a0-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="5a2a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="5a2a0-103">Загружает содержимое в конечную точку.</span><span class="sxs-lookup"><span data-stu-id="5a2a0-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a2a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a2a0-104">SYNTAX</span></span>

### <span data-ttu-id="5a2a0-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a2a0-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a2a0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a2a0-106">ByObjectParameterSet</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a2a0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a2a0-107">DESCRIPTION</span></span>
<span data-ttu-id="5a2a0-108">Командлет **Publish-AzureRmCdnEndpointContent** загружает содержимое с сервера-источника для конечной точки сети доставки содержимого Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="5a2a0-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="5a2a0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a2a0-109">EXAMPLES</span></span>

## <span data-ttu-id="5a2a0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a2a0-110">PARAMETERS</span></span>

### <span data-ttu-id="5a2a0-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a2a0-111">-CdnEndpoint</span></span>
<span data-ttu-id="5a2a0-112">Sepcifies конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="5a2a0-112">Sepcifies the CDN endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a2a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a2a0-113">-DefaultProfile</span></span>
<span data-ttu-id="5a2a0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5a2a0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a2a0-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5a2a0-115">-EndpointName</span></span>
<span data-ttu-id="5a2a0-116">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="5a2a0-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="5a2a0-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="5a2a0-117">-LoadContent</span></span>
<span data-ttu-id="5a2a0-118">Задает массив относительных путей для содержимого на исходном сервере, которое публикует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5a2a0-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a2a0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a2a0-119">-PassThru</span></span>
<span data-ttu-id="5a2a0-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5a2a0-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5a2a0-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5a2a0-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a2a0-122">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="5a2a0-122">-ProfileName</span></span>
<span data-ttu-id="5a2a0-123">Указывает имя профиля, которому принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="5a2a0-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="5a2a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a2a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="5a2a0-125">Указывает имя группы ресурсов, к которой принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="5a2a0-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="5a2a0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a2a0-126">CommonParameters</span></span>
<span data-ttu-id="5a2a0-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a2a0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a2a0-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a2a0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a2a0-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a2a0-129">INPUTS</span></span>

### <span data-ttu-id="5a2a0-130">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a2a0-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="5a2a0-131">Параметры: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5a2a0-131">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="5a2a0-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5a2a0-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a2a0-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a2a0-133">OUTPUTS</span></span>

### <span data-ttu-id="5a2a0-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a2a0-134">System.Boolean</span></span>

## <span data-ttu-id="5a2a0-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a2a0-135">NOTES</span></span>

## <span data-ttu-id="5a2a0-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a2a0-136">RELATED LINKS</span></span>

[<span data-ttu-id="5a2a0-137">Отмена публикации — AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="5a2a0-137">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


