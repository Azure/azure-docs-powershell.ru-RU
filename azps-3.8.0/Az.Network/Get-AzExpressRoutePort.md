---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 670880a9fa82e4845f37cdb5f0d108533a2b72c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073361"
---
# <span data-ttu-id="f45ef-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f45ef-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="f45ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f45ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f45ef-103">Получает ресурс Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f45ef-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="f45ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f45ef-104">SYNTAX</span></span>

### <span data-ttu-id="f45ef-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f45ef-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f45ef-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f45ef-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f45ef-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f45ef-107">DESCRIPTION</span></span>
<span data-ttu-id="f45ef-108">Командлет **Get-AzExpressRoutePort** используется для получения объекта ExpressRoutePort из подписки.</span><span class="sxs-lookup"><span data-stu-id="f45ef-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="f45ef-109">Возвращаемый объект expressrouteport можно использовать в качестве входных данных для других командлетов, которые работают с ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f45ef-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="f45ef-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f45ef-110">EXAMPLES</span></span>

### <span data-ttu-id="f45ef-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f45ef-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="f45ef-112">Получает объект ExpressRoutePort с именем $PortName в группе ресурсов, $rg в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="f45ef-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="f45ef-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f45ef-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="f45ef-114">Получает все объекты ExpressRoutePort, имя которых начинается с "Test".</span><span class="sxs-lookup"><span data-stu-id="f45ef-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="f45ef-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f45ef-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="f45ef-116">Получает объект ExpressRoutePort с $idом ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f45ef-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="f45ef-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f45ef-117">PARAMETERS</span></span>

### <span data-ttu-id="f45ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45ef-118">-DefaultProfile</span></span>
<span data-ttu-id="f45ef-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f45ef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f45ef-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f45ef-120">-Name</span></span>
<span data-ttu-id="f45ef-121">Имя ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f45ef-121">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f45ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f45ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="f45ef-123">Имя группы ресурсов для ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f45ef-123">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f45ef-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f45ef-124">-ResourceId</span></span>
<span data-ttu-id="f45ef-125">ResourceId для порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="f45ef-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="f45ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45ef-126">CommonParameters</span></span>
<span data-ttu-id="f45ef-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f45ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45ef-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f45ef-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45ef-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f45ef-129">INPUTS</span></span>

### <span data-ttu-id="f45ef-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f45ef-130">System.String</span></span>

## <span data-ttu-id="f45ef-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f45ef-131">OUTPUTS</span></span>

### <span data-ttu-id="f45ef-132">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f45ef-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="f45ef-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f45ef-133">NOTES</span></span>

## <span data-ttu-id="f45ef-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f45ef-134">RELATED LINKS</span></span>

[<span data-ttu-id="f45ef-135">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f45ef-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="f45ef-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f45ef-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="f45ef-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f45ef-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
