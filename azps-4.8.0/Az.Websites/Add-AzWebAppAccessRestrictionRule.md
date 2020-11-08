---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0abad2b3d38a5f614222a8eda7e3c27b9fda9556
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236925"
---
# <span data-ttu-id="8884f-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="8884f-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="8884f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8884f-102">SYNOPSIS</span></span>
<span data-ttu-id="8884f-103">Добавляет правило restiction доступа к веб-приложению Azure.</span><span class="sxs-lookup"><span data-stu-id="8884f-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="8884f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8884f-104">SYNTAX</span></span>

### <span data-ttu-id="8884f-105">IpAddressParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8884f-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8884f-106">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8884f-106">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8884f-107">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8884f-107">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8884f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8884f-108">DESCRIPTION</span></span>
<span data-ttu-id="8884f-109">Командлет **Add-AzWebAppAccessRestrictionRule** добавляет правило ограничения доступа к веб-приложению Azure.</span><span class="sxs-lookup"><span data-stu-id="8884f-109">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="8884f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8884f-110">EXAMPLES</span></span>

### <span data-ttu-id="8884f-111">Пример 1: Добавление IP-адресного правила ограничения доступа к Web App</span><span class="sxs-lookup"><span data-stu-id="8884f-111">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="8884f-112">Эта команда добавляет правило ограничения доступа с приоритетом 200 и диапазоном IP-адресов в приложение с именем ContosoSite, которое принадлежит к группе ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8884f-112">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="8884f-113">Пример 2: Добавление правила ограничения доступа к конечной точке службы подсети к веб-приложению</span><span class="sxs-lookup"><span data-stu-id="8884f-113">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="8884f-114">Эта команда добавляет правило ограничения доступа с приоритетом 300 и с помощью подсети appgw-Subnet в Corp-vnet на веб-приложение ContosoSite, которое принадлежит к группе ресурсов по умолчанию-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8884f-114">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8884f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8884f-115">PARAMETERS</span></span>

### <span data-ttu-id="8884f-116">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="8884f-116">-Action</span></span>
<span data-ttu-id="8884f-117">Правило разрешения или отказа.</span><span class="sxs-lookup"><span data-stu-id="8884f-117">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: Allow
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8884f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8884f-118">-DefaultProfile</span></span>
<span data-ttu-id="8884f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8884f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8884f-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="8884f-120">-Description</span></span>
<span data-ttu-id="8884f-121">Описание ограничения доступа.</span><span class="sxs-lookup"><span data-stu-id="8884f-121">Access Restriction description.</span></span>

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

### <span data-ttu-id="8884f-122">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="8884f-122">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="8884f-123">Укажите, следует ли проверять регистрацию конечной точки службы в подсети.</span><span class="sxs-lookup"><span data-stu-id="8884f-123">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubnetNameParameterSet, SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8884f-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="8884f-124">-IpAddress</span></span>
<span data-ttu-id="8884f-125">Диапазон CIDR для IP-адреса v4 или V6.</span><span class="sxs-lookup"><span data-stu-id="8884f-125">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="8884f-126">Например: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="8884f-126">E.g.: 192.168.0.0/24</span></span>

```yaml
Type: System.String
Parameter Sets: IpAddressParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8884f-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8884f-127">-Name</span></span>
<span data-ttu-id="8884f-128">Имя правила</span><span class="sxs-lookup"><span data-stu-id="8884f-128">Rule Name</span></span>

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

### <span data-ttu-id="8884f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8884f-129">-PassThru</span></span>
<span data-ttu-id="8884f-130">Возврат объекта конфигурации ограничения доступа.</span><span class="sxs-lookup"><span data-stu-id="8884f-130">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="8884f-131">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="8884f-131">-Priority</span></span>
<span data-ttu-id="8884f-132">Приоритет ограничения доступа.</span><span class="sxs-lookup"><span data-stu-id="8884f-132">Access Restriction priority.</span></span> <span data-ttu-id="8884f-133">Например: 500.</span><span class="sxs-lookup"><span data-stu-id="8884f-133">E.g.: 500.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8884f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8884f-134">-ResourceGroupName</span></span>
<span data-ttu-id="8884f-135">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8884f-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8884f-136">-SlotName</span><span class="sxs-lookup"><span data-stu-id="8884f-136">-SlotName</span></span>
<span data-ttu-id="8884f-137">Имя слота развертывания.</span><span class="sxs-lookup"><span data-stu-id="8884f-137">Deployment Slot name.</span></span>

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

### <span data-ttu-id="8884f-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8884f-138">-SubnetId</span></span>
<span data-ttu-id="8884f-139">ResourceId подсети.</span><span class="sxs-lookup"><span data-stu-id="8884f-139">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="8884f-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="8884f-140">-SubnetName</span></span>
<span data-ttu-id="8884f-141">Имя подсети.</span><span class="sxs-lookup"><span data-stu-id="8884f-141">Name of Subnet.</span></span>

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

### <span data-ttu-id="8884f-142">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="8884f-142">-TargetScmSite</span></span>
<span data-ttu-id="8884f-143">Правило предназначено для основного сайта или сайта SCM.</span><span class="sxs-lookup"><span data-stu-id="8884f-143">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="8884f-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8884f-144">-VirtualNetworkName</span></span>
<span data-ttu-id="8884f-145">Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8884f-145">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="8884f-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="8884f-146">-WebAppName</span></span>
<span data-ttu-id="8884f-147">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="8884f-147">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8884f-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8884f-148">-Confirm</span></span>
<span data-ttu-id="8884f-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8884f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8884f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8884f-150">-WhatIf</span></span>
<span data-ttu-id="8884f-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8884f-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8884f-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8884f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8884f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8884f-153">CommonParameters</span></span>
<span data-ttu-id="8884f-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8884f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8884f-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8884f-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8884f-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8884f-156">INPUTS</span></span>

### <span data-ttu-id="8884f-157">System. String</span><span class="sxs-lookup"><span data-stu-id="8884f-157">System.String</span></span>

## <span data-ttu-id="8884f-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8884f-158">OUTPUTS</span></span>

### <span data-ttu-id="8884f-159">Microsoft. Azure. Commands. Apps. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8884f-159">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="8884f-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="8884f-160">NOTES</span></span>

## <span data-ttu-id="8884f-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8884f-161">RELATED LINKS</span></span>

[<span data-ttu-id="8884f-162">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8884f-162">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="8884f-163">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8884f-163">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="8884f-164">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="8884f-164">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
