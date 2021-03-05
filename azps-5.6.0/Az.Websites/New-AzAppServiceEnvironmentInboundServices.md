---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironmentinboundservices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
ms.openlocfilehash: 68b2957e959365187ad82980bd2be2f055632a57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002115"
---
# <span data-ttu-id="48937-101">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="48937-101">New-AzAppServiceEnvironmentInboundServices</span></span>

## <span data-ttu-id="48937-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48937-102">SYNOPSIS</span></span>
<span data-ttu-id="48937-103">Создает входящие службы для среды служб приложений.</span><span class="sxs-lookup"><span data-stu-id="48937-103">Creates inbound services for App Service Environment.</span></span> <span data-ttu-id="48937-104">Для ASEv2 ILB будет создать частную зону DNS Azure и записи для связи с внутренним IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="48937-104">For ASEv2 ILB, this will create an Azure Private DNS Zone and records to map to the internal IP.</span></span> <span data-ttu-id="48937-105">Для ASEv3 она также гарантирует отключение сетевой политики подсети и создание закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="48937-105">For ASEv3 it will in addition ensure subnet has Network Policy disabled and will create a private endpoint.</span></span>

## <span data-ttu-id="48937-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="48937-106">SYNTAX</span></span>

### <span data-ttu-id="48937-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="48937-107">SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkName <String> -SubnetName <String> [-SkipDns] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48937-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48937-108">SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String> -SubnetId <String>
 [-SkipDns] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48937-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48937-109">DESCRIPTION</span></span>
<span data-ttu-id="48937-110">С **помощью cmdlet New-AzAppServiceEnvironmentInboundServices** создаются входящие службы для среды служб приложений.</span><span class="sxs-lookup"><span data-stu-id="48937-110">The **New-AzAppServiceEnvironmentInboundServices** cmdlet create inbound services for an App Service Environment.</span></span>

## <span data-ttu-id="48937-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="48937-111">EXAMPLES</span></span>

### <span data-ttu-id="48937-112">Пример 1. Создание личной зоны DNS и записей для ASEv2</span><span class="sxs-lookup"><span data-stu-id="48937-112">Example 1: Create Private DNS Zone and records for ASEv2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="48937-113">Создание зоны частных DNS и записей для ASEv2</span><span class="sxs-lookup"><span data-stu-id="48937-113">Create Private DNS Zone and records for ASEv2</span></span>

### <span data-ttu-id="48937-114">Пример 2. Создание закрытой конечной точки, личной зоны DNS и записей для ASEv3</span><span class="sxs-lookup"><span data-stu-id="48937-114">Example 2: Create private endpoint, Private DNS Zone and records for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="48937-115">Создание закрытой конечной точки, личной зоны DNS и записей для ASEv3</span><span class="sxs-lookup"><span data-stu-id="48937-115">Create private endpoint, Private DNS Zone and records for ASEv3</span></span>

### <span data-ttu-id="48937-116">Пример 3. Создание закрытой конечной точки для ASEv3</span><span class="sxs-lookup"><span data-stu-id="48937-116">Example 3: Create private endpoint for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet -SkipDns
```

<span data-ttu-id="48937-117">Создание закрытой конечной точки для ASEv3</span><span class="sxs-lookup"><span data-stu-id="48937-117">Create private endpoint for ASEv3</span></span>

## <span data-ttu-id="48937-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48937-118">PARAMETERS</span></span>

### <span data-ttu-id="48937-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48937-119">-DefaultProfile</span></span>
<span data-ttu-id="48937-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48937-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48937-121">-Name</span><span class="sxs-lookup"><span data-stu-id="48937-121">-Name</span></span>
<span data-ttu-id="48937-122">Имя среды службы приложений.</span><span class="sxs-lookup"><span data-stu-id="48937-122">The name of the app service environment.</span></span>

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

### <span data-ttu-id="48937-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48937-123">-PassThru</span></span>
<span data-ttu-id="48937-124">Состояние возврата.</span><span class="sxs-lookup"><span data-stu-id="48937-124">Return status.</span></span>

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

### <span data-ttu-id="48937-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48937-125">-ResourceGroupName</span></span>
<span data-ttu-id="48937-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48937-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="48937-127">-SkipDns</span><span class="sxs-lookup"><span data-stu-id="48937-127">-SkipDns</span></span>
<span data-ttu-id="48937-128">Не создавайте частную зону DNS и записи Azure.</span><span class="sxs-lookup"><span data-stu-id="48937-128">Do not create Azure Private DNS Zone and records.</span></span>

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

### <span data-ttu-id="48937-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="48937-129">-SubnetId</span></span>
<span data-ttu-id="48937-130">ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="48937-130">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48937-131">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="48937-131">-SubnetName</span></span>
<span data-ttu-id="48937-132">Имя подсети.</span><span class="sxs-lookup"><span data-stu-id="48937-132">The subnet name.</span></span> <span data-ttu-id="48937-133">Используется в сочетании с -VirtualNetworkName и должна быть в той же группе ресурсов, что и ASE.</span><span class="sxs-lookup"><span data-stu-id="48937-133">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="48937-134">Если нет, используйте -SubnetId</span><span class="sxs-lookup"><span data-stu-id="48937-134">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48937-135">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="48937-135">-VirtualNetworkName</span></span>
<span data-ttu-id="48937-136">Имя vNet.</span><span class="sxs-lookup"><span data-stu-id="48937-136">The vNet name.</span></span> <span data-ttu-id="48937-137">Используется в сочетании с -SubnetName и должен быть в той же группе ресурсов, что и ASE.</span><span class="sxs-lookup"><span data-stu-id="48937-137">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="48937-138">Если нет, используйте -SubnetId</span><span class="sxs-lookup"><span data-stu-id="48937-138">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48937-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48937-139">-Confirm</span></span>
<span data-ttu-id="48937-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48937-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48937-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48937-141">-WhatIf</span></span>
<span data-ttu-id="48937-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48937-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48937-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="48937-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48937-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48937-144">CommonParameters</span></span>
<span data-ttu-id="48937-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48937-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48937-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48937-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48937-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48937-147">INPUTS</span></span>

### <span data-ttu-id="48937-148">Нет</span><span class="sxs-lookup"><span data-stu-id="48937-148">None</span></span>

## <span data-ttu-id="48937-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="48937-149">OUTPUTS</span></span>

### <span data-ttu-id="48937-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="48937-150">System.Object</span></span>
## <span data-ttu-id="48937-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="48937-151">NOTES</span></span>

## <span data-ttu-id="48937-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48937-152">RELATED LINKS</span></span>

[<span data-ttu-id="48937-153">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="48937-153">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="48937-154">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="48937-154">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="48937-155">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="48937-155">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)