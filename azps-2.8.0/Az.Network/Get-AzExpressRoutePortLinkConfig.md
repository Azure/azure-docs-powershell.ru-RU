---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 5288ca32e43635db69598d72948e345f9e4c3256
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902937"
---
# <span data-ttu-id="52d04-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="52d04-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="52d04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52d04-102">SYNOPSIS</span></span>
<span data-ttu-id="52d04-103">Возвращает конфигурацию ExpressRoutePort ссылки.</span><span class="sxs-lookup"><span data-stu-id="52d04-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="52d04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52d04-104">SYNTAX</span></span>

### <span data-ttu-id="52d04-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52d04-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52d04-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52d04-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52d04-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52d04-107">DESCRIPTION</span></span>
<span data-ttu-id="52d04-108">Командлет **Get-AzExpressRoutePortLinkConfig** извлекает конфигурацию ссылки ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="52d04-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="52d04-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52d04-109">EXAMPLES</span></span>

### <span data-ttu-id="52d04-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="52d04-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="52d04-111">Возвращает конфигурацию link1 ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="52d04-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="52d04-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="52d04-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="52d04-113">Возвращает конфигурацию ссылки с $id ResourceId в ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="52d04-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="52d04-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52d04-114">PARAMETERS</span></span>

### <span data-ttu-id="52d04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d04-115">-DefaultProfile</span></span>
<span data-ttu-id="52d04-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52d04-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52d04-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="52d04-117">-ExpressRoutePort</span></span>
<span data-ttu-id="52d04-118">Ссылка на ресурс ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="52d04-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="52d04-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="52d04-119">-Name</span></span>
<span data-ttu-id="52d04-120">Имя ссылки.</span><span class="sxs-lookup"><span data-stu-id="52d04-120">Name of the link.</span></span>

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

### <span data-ttu-id="52d04-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52d04-121">-ResourceId</span></span>
<span data-ttu-id="52d04-122">ResourceId ссылки.</span><span class="sxs-lookup"><span data-stu-id="52d04-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="52d04-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d04-123">CommonParameters</span></span>
<span data-ttu-id="52d04-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52d04-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d04-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52d04-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d04-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52d04-126">INPUTS</span></span>

### <span data-ttu-id="52d04-127">System. String</span><span class="sxs-lookup"><span data-stu-id="52d04-127">System.String</span></span>

### <span data-ttu-id="52d04-128">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="52d04-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="52d04-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52d04-129">OUTPUTS</span></span>

### <span data-ttu-id="52d04-130">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="52d04-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="52d04-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="52d04-131">NOTES</span></span>

## <span data-ttu-id="52d04-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52d04-132">RELATED LINKS</span></span>
