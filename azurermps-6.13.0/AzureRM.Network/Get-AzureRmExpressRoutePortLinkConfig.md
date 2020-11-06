---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
ms.openlocfilehash: c758131685787ec8627f6e0cd3760e2ee42107c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568883"
---
# <span data-ttu-id="b5d52-101">Get-AzureRmExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="b5d52-101">Get-AzureRmExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="b5d52-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5d52-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d52-103">Возвращает конфигурацию ExpressRoutePort ссылки.</span><span class="sxs-lookup"><span data-stu-id="b5d52-103">Gets an ExpressRoutePort link configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5d52-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5d52-104">SYNTAX</span></span>

### <span data-ttu-id="b5d52-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5d52-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5d52-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5d52-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> -ResourceId <String> 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5d52-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5d52-107">DESCRIPTION</span></span>
<span data-ttu-id="b5d52-108">Командлет **Get-AzureRmExpressRoutePortLinkConfig** извлекает конфигурацию ссылки ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b5d52-108">The **Get-AzureRmExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="b5d52-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5d52-109">EXAMPLES</span></span>

### <span data-ttu-id="b5d52-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b5d52-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="b5d52-111">Возвращает конфигурацию link1 ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="b5d52-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="b5d52-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b5d52-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="b5d52-113">Возвращает конфигурацию ссылки с $id ResourceId в ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="b5d52-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="b5d52-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5d52-114">PARAMETERS</span></span>

### <span data-ttu-id="b5d52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d52-115">-DefaultProfile</span></span>
<span data-ttu-id="b5d52-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5d52-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5d52-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b5d52-117">-ExpressRoutePort</span></span>
<span data-ttu-id="b5d52-118">Ссылка на ресурс ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b5d52-118">The reference of the ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d52-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5d52-119">-Name</span></span>
<span data-ttu-id="b5d52-120">Имя ссылки.</span><span class="sxs-lookup"><span data-stu-id="b5d52-120">Name of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d52-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5d52-121">-ResourceId</span></span>
<span data-ttu-id="b5d52-122">ResourceId ссылки.</span><span class="sxs-lookup"><span data-stu-id="b5d52-122">ResourceId of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d52-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d52-123">CommonParameters</span></span>
<span data-ttu-id="b5d52-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5d52-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d52-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5d52-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d52-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5d52-126">INPUTS</span></span>

### <span data-ttu-id="b5d52-127">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b5d52-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="b5d52-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5d52-128">OUTPUTS</span></span>

### <span data-ttu-id="b5d52-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="b5d52-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="b5d52-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5d52-130">NOTES</span></span>

## <span data-ttu-id="b5d52-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5d52-131">RELATED LINKS</span></span>
