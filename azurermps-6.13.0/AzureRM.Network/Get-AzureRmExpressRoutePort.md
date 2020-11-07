---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
ms.openlocfilehash: 36c15c9a0bfae9bbf3a14f59877d23c1c8778163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734624"
---
# <span data-ttu-id="9bb85-101">Get-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9bb85-101">Get-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="9bb85-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9bb85-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb85-103">Получает ресурс Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="9bb85-103">Gets an Azure ExpressRoutePort resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bb85-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9bb85-104">SYNTAX</span></span>

### <span data-ttu-id="9bb85-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9bb85-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bb85-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bb85-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bb85-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bb85-107">DESCRIPTION</span></span>
<span data-ttu-id="9bb85-108">Командлет **Get-AzureRmExpressRoutePort** используется для получения объекта ExpressRoutePort из подписки.</span><span class="sxs-lookup"><span data-stu-id="9bb85-108">The **Get-AzureRmExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="9bb85-109">Возвращаемый объект expressrouteport можно использовать в качестве входных данных для других командлетов, которые работают с ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="9bb85-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="9bb85-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9bb85-110">EXAMPLES</span></span>

### <span data-ttu-id="9bb85-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9bb85-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="9bb85-112">Получает объект ExpressRoutePort с именем $PortName в группе ресурсов, $rg в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="9bb85-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="9bb85-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9bb85-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -ResourceId $id
```

<span data-ttu-id="9bb85-114">Получает объект ExpressRoutePort с $idом ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9bb85-114">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="9bb85-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9bb85-115">PARAMETERS</span></span>

### <span data-ttu-id="9bb85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb85-116">-DefaultProfile</span></span>
<span data-ttu-id="9bb85-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb85-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bb85-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9bb85-118">-Name</span></span>
<span data-ttu-id="9bb85-119">Имя ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="9bb85-119">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb85-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bb85-120">-ResourceGroupName</span></span>
<span data-ttu-id="9bb85-121">Имя группы ресурсов для ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="9bb85-121">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb85-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bb85-122">-ResourceId</span></span>
<span data-ttu-id="9bb85-123">ResourceId для порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="9bb85-123">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="9bb85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb85-124">CommonParameters</span></span>
<span data-ttu-id="9bb85-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9bb85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb85-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bb85-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb85-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9bb85-127">INPUTS</span></span>

### <span data-ttu-id="9bb85-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9bb85-128">System.String</span></span>

## <span data-ttu-id="9bb85-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bb85-129">OUTPUTS</span></span>

### <span data-ttu-id="9bb85-130">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9bb85-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="9bb85-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="9bb85-131">NOTES</span></span>

## <span data-ttu-id="9bb85-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bb85-132">RELATED LINKS</span></span>
