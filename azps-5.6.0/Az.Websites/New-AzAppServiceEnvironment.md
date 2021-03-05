---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
ms.openlocfilehash: a922958ec2e15ea9cb4a3b0189f74dda6d71eab2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011139"
---
# <span data-ttu-id="9276d-101">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="9276d-101">New-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="9276d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9276d-102">SYNOPSIS</span></span>
<span data-ttu-id="9276d-103">Создает среду служб приложения, включаемую рекомендуемую таблицу маршрутов и группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="9276d-103">Creates an App Service Environment including the recommended Route Table and Network Security Group</span></span>

## <span data-ttu-id="9276d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9276d-104">SYNTAX</span></span>

### <span data-ttu-id="9276d-105">ASEv2SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9276d-105">ASEv2SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> -LoadBalancerMode <String>
 [-SkipRouteTable] [-SkipNetworkSecurityGroup] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9276d-106">ASEv3SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9276d-106">ASEv3SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9276d-107">ASEv2SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9276d-107">ASEv2SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> -LoadBalancerMode <String> [-SkipRouteTable] [-SkipNetworkSecurityGroup]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9276d-108">ASEv3SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9276d-108">ASEv3SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9276d-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9276d-109">DESCRIPTION</span></span>
<span data-ttu-id="9276d-110">С **помощью cmdlet New-AzAppServiceEnvironment** создается среда службы приложений.</span><span class="sxs-lookup"><span data-stu-id="9276d-110">The **New-AzAppServiceEnvironment** cmdlet creates an App Service Environment.</span></span>

## <span data-ttu-id="9276d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9276d-111">EXAMPLES</span></span>

### <span data-ttu-id="9276d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9276d-112">Example 1</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
```

<span data-ttu-id="9276d-113">Создание среды службы приложений с именем MyAseV2, включая рекомендуемую таблицу маршрутов и группу безопасности сети</span><span class="sxs-lookup"><span data-stu-id="9276d-113">Create App Service Environment named MyAseV2 including recommended Route Table and Network Security Group</span></span>

### <span data-ttu-id="9276d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9276d-114">Example 2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
        -SkipRouteTable -SkipNetworkSecurityGroup
```

<span data-ttu-id="9276d-115">Создайте среду службы приложений с именем MyAseV2 без рекомендуемой таблицы маршрутов и группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="9276d-115">Create App Service Environment named MyAseV2 without recommended Route Table and Network Security Group.</span></span>
<span data-ttu-id="9276d-116">Они должны создаваться до или сразу после подготовки среды службы приложений для обеспечения функционального экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9276d-116">These should be create before or right after provisioning the App Service Environment to ensure a functional instance.</span></span>

## <span data-ttu-id="9276d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9276d-117">PARAMETERS</span></span>

### <span data-ttu-id="9276d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9276d-118">-AsJob</span></span>
<span data-ttu-id="9276d-119">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="9276d-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9276d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9276d-120">-DefaultProfile</span></span>
<span data-ttu-id="9276d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9276d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9276d-122">-Kind</span><span class="sxs-lookup"><span data-stu-id="9276d-122">-Kind</span></span>
<span data-ttu-id="9276d-123">Версия среды службы приложений.</span><span class="sxs-lookup"><span data-stu-id="9276d-123">The version of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ASEv2, ASEv3

Required: False
Position: 3
Default value: ASEv2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9276d-124">-LoadBalancerMode</span><span class="sxs-lookup"><span data-stu-id="9276d-124">-LoadBalancerMode</span></span>
<span data-ttu-id="9276d-125">Режим балансировки загрузки среды службы приложений.</span><span class="sxs-lookup"><span data-stu-id="9276d-125">Load balancer mode of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:
Accepted values: Internal, External

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9276d-126">-Location</span><span class="sxs-lookup"><span data-stu-id="9276d-126">-Location</span></span>
<span data-ttu-id="9276d-127">Расположение среды служб приложений, например: Западная Европа.</span><span class="sxs-lookup"><span data-stu-id="9276d-127">The Location of the app service environment eg: West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9276d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="9276d-128">-Name</span></span>
<span data-ttu-id="9276d-129">Имя среды службы приложений.</span><span class="sxs-lookup"><span data-stu-id="9276d-129">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9276d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9276d-130">-PassThru</span></span>
<span data-ttu-id="9276d-131">Возврат объекта среды службы приложений.</span><span class="sxs-lookup"><span data-stu-id="9276d-131">Return the app service environment object.</span></span>

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

### <span data-ttu-id="9276d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9276d-132">-ResourceGroupName</span></span>
<span data-ttu-id="9276d-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9276d-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9276d-134">-SkipNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9276d-134">-SkipNetworkSecurityGroup</span></span>
<span data-ttu-id="9276d-135">Не создавайте рекомендуемую группу безопасности сети в среде службы приложений.</span><span class="sxs-lookup"><span data-stu-id="9276d-135">Do not create the recommended network security group as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9276d-136">-SkipRouteTable</span><span class="sxs-lookup"><span data-stu-id="9276d-136">-SkipRouteTable</span></span>
<span data-ttu-id="9276d-137">Не создавайте рекомендуемую таблицу маршрутов в среде службы приложений.</span><span class="sxs-lookup"><span data-stu-id="9276d-137">Do not create the recommended route table as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9276d-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9276d-138">-SubnetId</span></span>
<span data-ttu-id="9276d-139">ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="9276d-139">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetIdParameterSet, ASEv3SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9276d-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="9276d-140">-SubnetName</span></span>
<span data-ttu-id="9276d-141">Имя подсети.</span><span class="sxs-lookup"><span data-stu-id="9276d-141">The subnet name.</span></span> <span data-ttu-id="9276d-142">Используется в сочетании с -VirtualNetworkName и должна быть в той же группе ресурсов, что и ASE.</span><span class="sxs-lookup"><span data-stu-id="9276d-142">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="9276d-143">Если нет, используйте -SubnetId</span><span class="sxs-lookup"><span data-stu-id="9276d-143">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9276d-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="9276d-144">-VirtualNetworkName</span></span>
<span data-ttu-id="9276d-145">Имя vNet.</span><span class="sxs-lookup"><span data-stu-id="9276d-145">The vNet name.</span></span> <span data-ttu-id="9276d-146">Используется в сочетании с subnetName и должен быть в той же группе ресурсов, что и ASE.</span><span class="sxs-lookup"><span data-stu-id="9276d-146">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="9276d-147">Если нет, используйте -SubnetId</span><span class="sxs-lookup"><span data-stu-id="9276d-147">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9276d-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9276d-148">-Confirm</span></span>
<span data-ttu-id="9276d-149">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9276d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9276d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9276d-150">-WhatIf</span></span>
<span data-ttu-id="9276d-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9276d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9276d-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9276d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9276d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9276d-153">CommonParameters</span></span>
<span data-ttu-id="9276d-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9276d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9276d-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9276d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9276d-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9276d-156">INPUTS</span></span>

### <span data-ttu-id="9276d-157">Нет</span><span class="sxs-lookup"><span data-stu-id="9276d-157">None</span></span>

## <span data-ttu-id="9276d-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9276d-158">OUTPUTS</span></span>

### <span data-ttu-id="9276d-159">System.Object</span><span class="sxs-lookup"><span data-stu-id="9276d-159">System.Object</span></span>
## <span data-ttu-id="9276d-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9276d-160">NOTES</span></span>

## <span data-ttu-id="9276d-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9276d-161">RELATED LINKS</span></span>

[<span data-ttu-id="9276d-162">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="9276d-162">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="9276d-163">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="9276d-163">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="9276d-164">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="9276d-164">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)
