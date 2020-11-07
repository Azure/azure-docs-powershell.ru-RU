---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: a851722d02fa37c085649894f41f6273abf4372d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901450"
---
# <span data-ttu-id="e0787-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="e0787-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="e0787-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0787-102">SYNOPSIS</span></span>
<span data-ttu-id="e0787-103">Загружает содержимое в конечную точку.</span><span class="sxs-lookup"><span data-stu-id="e0787-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="e0787-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0787-104">SYNTAX</span></span>

### <span data-ttu-id="e0787-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e0787-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0787-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0787-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0787-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0787-107">DESCRIPTION</span></span>
<span data-ttu-id="e0787-108">Командлет **Publish-AzCdnEndpointContent** загружает содержимое с сервера-источника для конечной точки сети доставки содержимого Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="e0787-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e0787-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0787-109">EXAMPLES</span></span>

## <span data-ttu-id="e0787-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0787-110">PARAMETERS</span></span>

### <span data-ttu-id="e0787-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e0787-111">-CdnEndpoint</span></span>
<span data-ttu-id="e0787-112">Sepcifies конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="e0787-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="e0787-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0787-113">-DefaultProfile</span></span>
<span data-ttu-id="e0787-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e0787-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0787-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e0787-115">-EndpointName</span></span>
<span data-ttu-id="e0787-116">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="e0787-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="e0787-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="e0787-117">-LoadContent</span></span>
<span data-ttu-id="e0787-118">Задает массив относительных путей для содержимого на исходном сервере, которое публикует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e0787-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="e0787-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0787-119">-PassThru</span></span>
<span data-ttu-id="e0787-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e0787-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e0787-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e0787-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e0787-122">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="e0787-122">-ProfileName</span></span>
<span data-ttu-id="e0787-123">Указывает имя профиля, которому принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="e0787-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e0787-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0787-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0787-125">Указывает имя группы ресурсов, к которой принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="e0787-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e0787-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0787-126">CommonParameters</span></span>
<span data-ttu-id="e0787-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0787-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0787-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0787-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0787-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0787-129">INPUTS</span></span>

### <span data-ttu-id="e0787-130">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e0787-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="e0787-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e0787-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e0787-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0787-132">OUTPUTS</span></span>

### <span data-ttu-id="e0787-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e0787-133">System.Boolean</span></span>

## <span data-ttu-id="e0787-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0787-134">NOTES</span></span>

## <span data-ttu-id="e0787-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0787-135">RELATED LINKS</span></span>

[<span data-ttu-id="e0787-136">Отмена публикации — AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="e0787-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


