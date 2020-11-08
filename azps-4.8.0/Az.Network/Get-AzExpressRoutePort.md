---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 670880a9fa82e4845f37cdb5f0d108533a2b72c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244153"
---
# <span data-ttu-id="bc2d6-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bc2d6-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="bc2d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="bc2d6-103">Получает ресурс Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="bc2d6-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="bc2d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc2d6-104">SYNTAX</span></span>

### <span data-ttu-id="bc2d6-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bc2d6-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc2d6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc2d6-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc2d6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc2d6-107">DESCRIPTION</span></span>
<span data-ttu-id="bc2d6-108">Командлет **Get-AzExpressRoutePort** используется для получения объекта ExpressRoutePort из подписки.</span><span class="sxs-lookup"><span data-stu-id="bc2d6-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="bc2d6-109">Возвращаемый объект expressrouteport можно использовать в качестве входных данных для других командлетов, которые работают с ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="bc2d6-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="bc2d6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc2d6-110">EXAMPLES</span></span>

### <span data-ttu-id="bc2d6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc2d6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="bc2d6-112">Получает объект ExpressRoutePort с именем $PortName в группе ресурсов, $rg в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="bc2d6-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="bc2d6-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bc2d6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="bc2d6-114">Получает все объекты ExpressRoutePort, имя которых начинается с "Test".</span><span class="sxs-lookup"><span data-stu-id="bc2d6-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="bc2d6-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bc2d6-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="bc2d6-116">Получает объект ExpressRoutePort с $idом ResourceId.</span><span class="sxs-lookup"><span data-stu-id="bc2d6-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="bc2d6-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc2d6-117">PARAMETERS</span></span>

### <span data-ttu-id="bc2d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc2d6-118">-DefaultProfile</span></span>
<span data-ttu-id="bc2d6-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc2d6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc2d6-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc2d6-120">-Name</span></span>
<span data-ttu-id="bc2d6-121">Имя ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="bc2d6-121">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="bc2d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc2d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="bc2d6-123">Имя группы ресурсов для ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="bc2d6-123">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="bc2d6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc2d6-124">-ResourceId</span></span>
<span data-ttu-id="bc2d6-125">ResourceId для порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="bc2d6-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="bc2d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc2d6-126">CommonParameters</span></span>
<span data-ttu-id="bc2d6-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc2d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc2d6-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc2d6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc2d6-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc2d6-129">INPUTS</span></span>

### <span data-ttu-id="bc2d6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bc2d6-130">System.String</span></span>

## <span data-ttu-id="bc2d6-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc2d6-131">OUTPUTS</span></span>

### <span data-ttu-id="bc2d6-132">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bc2d6-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="bc2d6-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc2d6-133">NOTES</span></span>

## <span data-ttu-id="bc2d6-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc2d6-134">RELATED LINKS</span></span>

[<span data-ttu-id="bc2d6-135">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bc2d6-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="bc2d6-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bc2d6-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="bc2d6-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bc2d6-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
