---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244860"
---
# <span data-ttu-id="ff0e0-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="ff0e0-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="ff0e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0e0-103">Загрузка документа авторизации письма для порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="ff0e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff0e0-104">SYNTAX</span></span>

### <span data-ttu-id="ff0e0-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff0e0-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff0e0-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff0e0-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff0e0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff0e0-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff0e0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff0e0-108">DESCRIPTION</span></span>
<span data-ttu-id="ff0e0-109">New-AzExpressRoutePortLOA командлет загружает документ для проверки подлинности в формате PDF для порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="ff0e0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff0e0-110">EXAMPLES</span></span>

### <span data-ttu-id="ff0e0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff0e0-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="ff0e0-112">Скачайте документ для проверки подлинности для порта Express Route "myPort" и сохраните его в файле "loa.pdf".</span><span class="sxs-lookup"><span data-stu-id="ff0e0-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="ff0e0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff0e0-113">PARAMETERS</span></span>

### <span data-ttu-id="ff0e0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff0e0-114">-AsJob</span></span>
<span data-ttu-id="ff0e0-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ff0e0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff0e0-116">-Поля</span><span class="sxs-lookup"><span data-stu-id="ff0e0-116">-CustomerName</span></span>
<span data-ttu-id="ff0e0-117">Имя пользователя, которому назначен этот порт Express Route.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-117">The customer name to whom this Express Route Port is assigned to.</span></span>

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

### <span data-ttu-id="ff0e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0e0-118">-DefaultProfile</span></span>
<span data-ttu-id="ff0e0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff0e0-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="ff0e0-120">-Destination</span></span>
<span data-ttu-id="ff0e0-121">Выходной путь для хранения письма авторизации.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-121">The output filepath to store the Letter of Authorization to.</span></span>

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

### <span data-ttu-id="ff0e0-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ff0e0-122">-ExpressRoutePort</span></span>
<span data-ttu-id="ff0e0-123">Ресурс порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-123">The express route port resource.</span></span>

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

### <span data-ttu-id="ff0e0-124">-ID</span><span class="sxs-lookup"><span data-stu-id="ff0e0-124">-Id</span></span>
<span data-ttu-id="ff0e0-125">ResourceId для порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="ff0e0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff0e0-126">-PassThru</span></span>
<span data-ttu-id="ff0e0-127">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="ff0e0-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ff0e0-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="ff0e0-129">-PortName</span></span>
<span data-ttu-id="ff0e0-130">Имя порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-130">The express route port name.</span></span>

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

### <span data-ttu-id="ff0e0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff0e0-131">-ResourceGroupName</span></span>
<span data-ttu-id="ff0e0-132">Имя группы ресурсов для порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-132">The resource group name of the express route port.</span></span>

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

### <span data-ttu-id="ff0e0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0e0-133">CommonParameters</span></span>
<span data-ttu-id="ff0e0-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff0e0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0e0-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff0e0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0e0-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff0e0-136">INPUTS</span></span>

### <span data-ttu-id="ff0e0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ff0e0-137">System.String</span></span>

## <span data-ttu-id="ff0e0-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff0e0-138">OUTPUTS</span></span>

### <span data-ttu-id="ff0e0-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff0e0-139">System.Boolean</span></span>

## <span data-ttu-id="ff0e0-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff0e0-140">NOTES</span></span>

## <span data-ttu-id="ff0e0-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff0e0-141">RELATED LINKS</span></span>
