---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519697"
---
# <span data-ttu-id="86dc6-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="86dc6-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="86dc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="86dc6-103">Загружает содержимое в конечную точку.</span><span class="sxs-lookup"><span data-stu-id="86dc6-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="86dc6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86dc6-104">SYNTAX</span></span>

### <span data-ttu-id="86dc6-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86dc6-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86dc6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86dc6-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86dc6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86dc6-107">DESCRIPTION</span></span>
<span data-ttu-id="86dc6-108">Cmdlet **Publish-AzCdnEndpointContent** загружает содержимое с сервера-источника для конечной точки доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="86dc6-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="86dc6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86dc6-109">EXAMPLES</span></span>

## <span data-ttu-id="86dc6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86dc6-110">PARAMETERS</span></span>

### <span data-ttu-id="86dc6-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="86dc6-111">-CdnEndpoint</span></span>
<span data-ttu-id="86dc6-112">Указывает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="86dc6-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="86dc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86dc6-113">-DefaultProfile</span></span>
<span data-ttu-id="86dc6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="86dc6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86dc6-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="86dc6-115">-EndpointName</span></span>
<span data-ttu-id="86dc6-116">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="86dc6-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="86dc6-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="86dc6-117">-LoadContent</span></span>
<span data-ttu-id="86dc6-118">Определяет массив относительных путей для содержимого на сервере-источнике, который публикует этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86dc6-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="86dc6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86dc6-119">-PassThru</span></span>
<span data-ttu-id="86dc6-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="86dc6-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="86dc6-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="86dc6-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="86dc6-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="86dc6-122">-ProfileName</span></span>
<span data-ttu-id="86dc6-123">Определяет имя профиля, к которому принадлежит сервер-источник.</span><span class="sxs-lookup"><span data-stu-id="86dc6-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="86dc6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86dc6-124">-ResourceGroupName</span></span>
<span data-ttu-id="86dc6-125">Имя группы ресурсов, к которой принадлежит сервер-источник.</span><span class="sxs-lookup"><span data-stu-id="86dc6-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="86dc6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86dc6-126">CommonParameters</span></span>
<span data-ttu-id="86dc6-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86dc6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86dc6-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86dc6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86dc6-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86dc6-129">INPUTS</span></span>

### <span data-ttu-id="86dc6-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="86dc6-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="86dc6-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="86dc6-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="86dc6-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86dc6-132">OUTPUTS</span></span>

### <span data-ttu-id="86dc6-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="86dc6-133">System.Boolean</span></span>

## <span data-ttu-id="86dc6-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86dc6-134">NOTES</span></span>

## <span data-ttu-id="86dc6-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86dc6-135">RELATED LINKS</span></span>

[<span data-ttu-id="86dc6-136">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="86dc6-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


