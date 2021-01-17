---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403079"
---
# <span data-ttu-id="638b8-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="638b8-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="638b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="638b8-102">SYNOPSIS</span></span>
<span data-ttu-id="638b8-103">Скачайте досье на перенос экспресс-маршрутов.</span><span class="sxs-lookup"><span data-stu-id="638b8-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="638b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="638b8-104">SYNTAX</span></span>

### <span data-ttu-id="638b8-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="638b8-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="638b8-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="638b8-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="638b8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="638b8-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="638b8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="638b8-108">DESCRIPTION</span></span>
<span data-ttu-id="638b8-109">New-AzExpressRoutePortLOA-файл загружает досье в формате PDF для порта express route.</span><span class="sxs-lookup"><span data-stu-id="638b8-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="638b8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="638b8-110">EXAMPLES</span></span>

### <span data-ttu-id="638b8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="638b8-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="638b8-112">Скачайте документ авторизации для порта express route "myPort" и храните его в файле "loa.pdf".</span><span class="sxs-lookup"><span data-stu-id="638b8-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="638b8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="638b8-113">PARAMETERS</span></span>

### <span data-ttu-id="638b8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="638b8-114">-AsJob</span></span>
<span data-ttu-id="638b8-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="638b8-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="638b8-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="638b8-116">-CustomerName</span></span>
<span data-ttu-id="638b8-117">Имя клиента, которому назначен этот порт Express Route.</span><span class="sxs-lookup"><span data-stu-id="638b8-117">The customer name to whom this Express Route Port is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="638b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="638b8-118">-DefaultProfile</span></span>
<span data-ttu-id="638b8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="638b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="638b8-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="638b8-120">-Destination</span></span>
<span data-ttu-id="638b8-121">Выходной файл, в котором будет храниться досье.</span><span class="sxs-lookup"><span data-stu-id="638b8-121">The output filepath to store the Letter of Authorization to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="638b8-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="638b8-122">-ExpressRoutePort</span></span>
<span data-ttu-id="638b8-123">Ресурс порта express route.</span><span class="sxs-lookup"><span data-stu-id="638b8-123">The express route port resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="638b8-124">-Id</span><span class="sxs-lookup"><span data-stu-id="638b8-124">-Id</span></span>
<span data-ttu-id="638b8-125">ResourceId порта express route.</span><span class="sxs-lookup"><span data-stu-id="638b8-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="638b8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="638b8-126">-PassThru</span></span>
<span data-ttu-id="638b8-127">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="638b8-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="638b8-128">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="638b8-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="638b8-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="638b8-129">-PortName</span></span>
<span data-ttu-id="638b8-130">Имя порта express route.</span><span class="sxs-lookup"><span data-stu-id="638b8-130">The express route port name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="638b8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="638b8-131">-ResourceGroupName</span></span>
<span data-ttu-id="638b8-132">Имя группы ресурсов для порта express route.</span><span class="sxs-lookup"><span data-stu-id="638b8-132">The resource group name of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="638b8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="638b8-133">CommonParameters</span></span>
<span data-ttu-id="638b8-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="638b8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="638b8-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="638b8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="638b8-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="638b8-136">INPUTS</span></span>

### <span data-ttu-id="638b8-137">System.String</span><span class="sxs-lookup"><span data-stu-id="638b8-137">System.String</span></span>

## <span data-ttu-id="638b8-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="638b8-138">OUTPUTS</span></span>

### <span data-ttu-id="638b8-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="638b8-139">System.Boolean</span></span>

## <span data-ttu-id="638b8-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="638b8-140">NOTES</span></span>

## <span data-ttu-id="638b8-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="638b8-141">RELATED LINKS</span></span>
