---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 1df36c7816894f8ccfc642eac307a84b485ba7ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567157"
---
# <span data-ttu-id="12504-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="12504-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="12504-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12504-102">SYNOPSIS</span></span>
<span data-ttu-id="12504-103">Загружает содержимое в конечную точку.</span><span class="sxs-lookup"><span data-stu-id="12504-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12504-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12504-104">SYNTAX</span></span>

### <span data-ttu-id="12504-105">Параметры, заданные для параметров полей (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="12504-105">Parameter Set for fields parameters (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12504-106">Параметр, заданный для параметров объекта</span><span class="sxs-lookup"><span data-stu-id="12504-106">Parameter Set for object parameters</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12504-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12504-107">DESCRIPTION</span></span>
<span data-ttu-id="12504-108">Командлет **Publish-AzureRmCdnEndpointContent** загружает содержимое с сервера-источника для конечной точки сети доставки содержимого Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="12504-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="12504-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12504-109">EXAMPLES</span></span>

## <span data-ttu-id="12504-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12504-110">PARAMETERS</span></span>

### <span data-ttu-id="12504-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="12504-111">-CdnEndpoint</span></span>
<span data-ttu-id="12504-112">Sepcifies конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="12504-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="12504-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="12504-113">-EndpointName</span></span>
<span data-ttu-id="12504-114">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="12504-114">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="12504-115">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="12504-115">-LoadContent</span></span>
<span data-ttu-id="12504-116">Задает массив относительных путей для содержимого на исходном сервере, которое публикует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="12504-116">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="12504-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12504-117">-PassThru</span></span>
<span data-ttu-id="12504-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="12504-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="12504-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="12504-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="12504-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="12504-120">-ProfileName</span></span>
<span data-ttu-id="12504-121">Указывает имя профиля, которому принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="12504-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="12504-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12504-122">-ResourceGroupName</span></span>
<span data-ttu-id="12504-123">Указывает имя группы ресурсов, к которой принадлежит сервер источника.</span><span class="sxs-lookup"><span data-stu-id="12504-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="12504-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12504-124">-DefaultProfile</span></span>
<span data-ttu-id="12504-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12504-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12504-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12504-126">CommonParameters</span></span>
<span data-ttu-id="12504-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12504-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12504-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12504-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12504-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12504-129">INPUTS</span></span>

### <span data-ttu-id="12504-130">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="12504-130">PSEndpoint</span></span>
<span data-ttu-id="12504-131">Параметр "CdnEndpoint" принимает значение типа "PSEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="12504-131">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="12504-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12504-132">OUTPUTS</span></span>

### <span data-ttu-id="12504-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12504-133">System.Boolean</span></span>

## <span data-ttu-id="12504-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="12504-134">NOTES</span></span>

## <span data-ttu-id="12504-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12504-135">RELATED LINKS</span></span>

[<span data-ttu-id="12504-136">Отмена публикации — AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="12504-136">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


