---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
ms.openlocfilehash: 5a9e4f7a4a3d7b8173cf7ef797edfc354d655cc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562831"
---
# <span data-ttu-id="879c4-101">Remove-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="879c4-101">Remove-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="879c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="879c4-102">SYNOPSIS</span></span>
<span data-ttu-id="879c4-103">Удаление ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="879c4-103">Removes an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="879c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="879c4-104">SYNTAX</span></span>

### <span data-ttu-id="879c4-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="879c4-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="879c4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="879c4-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="879c4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="879c4-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="879c4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="879c4-108">DESCRIPTION</span></span>
<span data-ttu-id="879c4-109">Командлет **Remove-AzureRmExpressRoutePort** удаляет ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="879c4-109">The **Remove-AzureRmExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="879c4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="879c4-110">EXAMPLES</span></span>

### <span data-ttu-id="879c4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="879c4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="879c4-112">Удаляет $PortName ресурс ExpressRoutePort в $rg группе ресурсов в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="879c4-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="879c4-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="879c4-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -InputObject $erPort
```
<span data-ttu-id="879c4-114">Удаляет ресурс ExpressRoutePort в InputObject.</span><span class="sxs-lookup"><span data-stu-id="879c4-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="879c4-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="879c4-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="879c4-116">Удаляет ресурс ExpressRoutePort с ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="879c4-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="879c4-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="879c4-117">PARAMETERS</span></span>

### <span data-ttu-id="879c4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="879c4-118">-AsJob</span></span>
<span data-ttu-id="879c4-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="879c4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="879c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="879c4-120">-DefaultProfile</span></span>
<span data-ttu-id="879c4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="879c4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="879c4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="879c4-122">-Force</span></span>
<span data-ttu-id="879c4-123">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="879c4-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="879c4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="879c4-124">-InputObject</span></span>
<span data-ttu-id="879c4-125">Объект порта Express Route</span><span class="sxs-lookup"><span data-stu-id="879c4-125">The express route port object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="879c4-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="879c4-126">-Name</span></span>
<span data-ttu-id="879c4-127">Имя ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="879c4-127">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="879c4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="879c4-128">-PassThru</span></span>
<span data-ttu-id="879c4-129">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="879c4-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="879c4-130">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="879c4-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="879c4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="879c4-131">-ResourceGroupName</span></span>
<span data-ttu-id="879c4-132">Имя группы ресурсов для ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="879c4-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="879c4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="879c4-133">-ResourceId</span></span>
<span data-ttu-id="879c4-134">ResourceId для порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="879c4-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="879c4-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="879c4-135">-Confirm</span></span>
<span data-ttu-id="879c4-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="879c4-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879c4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="879c4-137">-WhatIf</span></span>
<span data-ttu-id="879c4-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="879c4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="879c4-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="879c4-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879c4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="879c4-140">CommonParameters</span></span>
<span data-ttu-id="879c4-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="879c4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="879c4-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="879c4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="879c4-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="879c4-143">INPUTS</span></span>

### <span data-ttu-id="879c4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="879c4-144">System.String</span></span>

### <span data-ttu-id="879c4-145">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="879c4-145">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="879c4-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="879c4-146">OUTPUTS</span></span>

### <span data-ttu-id="879c4-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="879c4-147">System.Object</span></span>
## <span data-ttu-id="879c4-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="879c4-148">NOTES</span></span>

## <span data-ttu-id="879c4-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="879c4-149">RELATED LINKS</span></span>
