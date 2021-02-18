---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: 7e6ee711de551de00a54930be2bdb285998e3ccb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218377"
---
# <span data-ttu-id="083e7-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="083e7-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="083e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="083e7-102">SYNOPSIS</span></span>
<span data-ttu-id="083e7-103">Удаляет ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="083e7-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="083e7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="083e7-104">SYNTAX</span></span>

### <span data-ttu-id="083e7-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="083e7-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="083e7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="083e7-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="083e7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="083e7-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="083e7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="083e7-108">DESCRIPTION</span></span>
<span data-ttu-id="083e7-109">Для **удаления ExpressRoutePort удаляется cmdlet Remove-AzExpressRoutePort.**</span><span class="sxs-lookup"><span data-stu-id="083e7-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="083e7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="083e7-110">EXAMPLES</span></span>

### <span data-ttu-id="083e7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="083e7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="083e7-112">Удаляет $PortName ExpressRoutePort в $rg группу ресурсов в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="083e7-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="083e7-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="083e7-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="083e7-114">Удаляет ресурс ExpressRoutePort в InputObject.</span><span class="sxs-lookup"><span data-stu-id="083e7-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="083e7-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="083e7-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="083e7-116">Удаляет ресурс ExpressRoutePort с resourceId $id.</span><span class="sxs-lookup"><span data-stu-id="083e7-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="083e7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="083e7-117">PARAMETERS</span></span>

### <span data-ttu-id="083e7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="083e7-118">-AsJob</span></span>
<span data-ttu-id="083e7-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="083e7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="083e7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083e7-120">-DefaultProfile</span></span>
<span data-ttu-id="083e7-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="083e7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="083e7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="083e7-122">-Force</span></span>
<span data-ttu-id="083e7-123">Не спрашивайте подтверждения, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="083e7-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="083e7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="083e7-124">-InputObject</span></span>
<span data-ttu-id="083e7-125">Объект порта express route</span><span class="sxs-lookup"><span data-stu-id="083e7-125">The express route port object</span></span>

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

### <span data-ttu-id="083e7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="083e7-126">-Name</span></span>
<span data-ttu-id="083e7-127">Имя ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="083e7-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="083e7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="083e7-128">-PassThru</span></span>
<span data-ttu-id="083e7-129">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="083e7-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="083e7-130">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="083e7-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="083e7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="083e7-131">-ResourceGroupName</span></span>
<span data-ttu-id="083e7-132">Имя группы ресурсов ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="083e7-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="083e7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="083e7-133">-ResourceId</span></span>
<span data-ttu-id="083e7-134">ResourceId порта express route.</span><span class="sxs-lookup"><span data-stu-id="083e7-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="083e7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="083e7-135">-Confirm</span></span>
<span data-ttu-id="083e7-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="083e7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="083e7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="083e7-137">-WhatIf</span></span>
<span data-ttu-id="083e7-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="083e7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="083e7-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="083e7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="083e7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083e7-140">CommonParameters</span></span>
<span data-ttu-id="083e7-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083e7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083e7-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="083e7-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083e7-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="083e7-143">INPUTS</span></span>

### <span data-ttu-id="083e7-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="083e7-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="083e7-145">System.String</span><span class="sxs-lookup"><span data-stu-id="083e7-145">System.String</span></span>

## <span data-ttu-id="083e7-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="083e7-146">OUTPUTS</span></span>

### <span data-ttu-id="083e7-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="083e7-147">System.Boolean</span></span>

## <span data-ttu-id="083e7-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="083e7-148">NOTES</span></span>

## <span data-ttu-id="083e7-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="083e7-149">RELATED LINKS</span></span>

[<span data-ttu-id="083e7-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="083e7-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="083e7-151">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="083e7-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="083e7-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="083e7-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
