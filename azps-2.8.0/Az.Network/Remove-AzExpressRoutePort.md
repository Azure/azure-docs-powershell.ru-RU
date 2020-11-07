---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: 52eae037fb3c41940b1e1b67235f0affe729a41f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903482"
---
# <span data-ttu-id="31bed-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="31bed-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="31bed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31bed-102">SYNOPSIS</span></span>
<span data-ttu-id="31bed-103">Удаление ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="31bed-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="31bed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31bed-104">SYNTAX</span></span>

### <span data-ttu-id="31bed-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31bed-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31bed-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31bed-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31bed-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31bed-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31bed-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31bed-108">DESCRIPTION</span></span>
<span data-ttu-id="31bed-109">Командлет **Remove-AzExpressRoutePort** удаляет ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="31bed-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="31bed-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31bed-110">EXAMPLES</span></span>

### <span data-ttu-id="31bed-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31bed-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="31bed-112">Удаляет $PortName ресурс ExpressRoutePort в $rg группе ресурсов в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="31bed-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="31bed-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="31bed-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="31bed-114">Удаляет ресурс ExpressRoutePort в InputObject.</span><span class="sxs-lookup"><span data-stu-id="31bed-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="31bed-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="31bed-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="31bed-116">Удаляет ресурс ExpressRoutePort с ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="31bed-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="31bed-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31bed-117">PARAMETERS</span></span>

### <span data-ttu-id="31bed-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31bed-118">-AsJob</span></span>
<span data-ttu-id="31bed-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="31bed-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31bed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31bed-120">-DefaultProfile</span></span>
<span data-ttu-id="31bed-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31bed-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31bed-122">-Force</span><span class="sxs-lookup"><span data-stu-id="31bed-122">-Force</span></span>
<span data-ttu-id="31bed-123">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="31bed-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="31bed-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31bed-124">-InputObject</span></span>
<span data-ttu-id="31bed-125">Объект порта Express Route</span><span class="sxs-lookup"><span data-stu-id="31bed-125">The express route port object</span></span>

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

### <span data-ttu-id="31bed-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31bed-126">-Name</span></span>
<span data-ttu-id="31bed-127">Имя ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="31bed-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="31bed-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31bed-128">-PassThru</span></span>
<span data-ttu-id="31bed-129">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="31bed-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="31bed-130">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="31bed-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="31bed-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31bed-131">-ResourceGroupName</span></span>
<span data-ttu-id="31bed-132">Имя группы ресурсов для ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="31bed-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="31bed-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31bed-133">-ResourceId</span></span>
<span data-ttu-id="31bed-134">ResourceId для порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="31bed-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="31bed-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31bed-135">-Confirm</span></span>
<span data-ttu-id="31bed-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="31bed-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31bed-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31bed-137">-WhatIf</span></span>
<span data-ttu-id="31bed-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="31bed-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31bed-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="31bed-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31bed-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31bed-140">CommonParameters</span></span>
<span data-ttu-id="31bed-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31bed-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31bed-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31bed-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31bed-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31bed-143">INPUTS</span></span>

### <span data-ttu-id="31bed-144">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="31bed-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="31bed-145">System. String</span><span class="sxs-lookup"><span data-stu-id="31bed-145">System.String</span></span>

## <span data-ttu-id="31bed-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31bed-146">OUTPUTS</span></span>

### <span data-ttu-id="31bed-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31bed-147">System.Boolean</span></span>

## <span data-ttu-id="31bed-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="31bed-148">NOTES</span></span>

## <span data-ttu-id="31bed-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31bed-149">RELATED LINKS</span></span>

[<span data-ttu-id="31bed-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="31bed-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="31bed-151">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="31bed-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="31bed-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="31bed-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
