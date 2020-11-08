---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079141"
---
# <span data-ttu-id="6eed4-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="6eed4-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="6eed4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6eed4-102">SYNOPSIS</span></span>
<span data-ttu-id="6eed4-103">Загружает содержимое в конечную точку.</span><span class="sxs-lookup"><span data-stu-id="6eed4-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="6eed4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6eed4-104">SYNTAX</span></span>

### <span data-ttu-id="6eed4-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6eed4-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6eed4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eed4-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6eed4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6eed4-107">DESCRIPTION</span></span>
<span data-ttu-id="6eed4-108">Командлет **Publish-AzCdnEndpointContent** загружает содержимое с сервера-источника для конечной точки сети доставки содержимого Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="6eed4-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="6eed4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6eed4-109">EXAMPLES</span></span>

## <span data-ttu-id="6eed4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6eed4-110">PARAMETERS</span></span>

### <span data-ttu-id="6eed4-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6eed4-111">-CdnEndpoint</span></span>
<span data-ttu-id="6eed4-112">Задает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="6eed4-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="6eed4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eed4-113">-DefaultProfile</span></span>
<span data-ttu-id="6eed4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6eed4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6eed4-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6eed4-115">-EndpointName</span></span>
<span data-ttu-id="6eed4-116">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="6eed4-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="6eed4-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="6eed4-117">-LoadContent</span></span>
<span data-ttu-id="6eed4-118">Задает массив относительных путей для содержимого на исходном сервере, которое публикует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6eed4-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="6eed4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6eed4-119">-PassThru</span></span>
<span data-ttu-id="6eed4-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="6eed4-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6eed4-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6eed4-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6eed4-122">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="6eed4-122">-ProfileName</span></span>
<span data-ttu-id="6eed4-123">Указывает имя профиля, которому принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="6eed4-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="6eed4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eed4-124">-ResourceGroupName</span></span>
<span data-ttu-id="6eed4-125">Указывает имя группы ресурсов, к которой принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="6eed4-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="6eed4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eed4-126">CommonParameters</span></span>
<span data-ttu-id="6eed4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6eed4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eed4-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6eed4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eed4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6eed4-129">INPUTS</span></span>

### <span data-ttu-id="6eed4-130">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6eed4-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="6eed4-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6eed4-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6eed4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6eed4-132">OUTPUTS</span></span>

### <span data-ttu-id="6eed4-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6eed4-133">System.Boolean</span></span>

## <span data-ttu-id="6eed4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="6eed4-134">NOTES</span></span>

## <span data-ttu-id="6eed4-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6eed4-135">RELATED LINKS</span></span>

[<span data-ttu-id="6eed4-136">Отмена публикации — AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="6eed4-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)

