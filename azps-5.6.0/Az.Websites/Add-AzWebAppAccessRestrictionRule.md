---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983939"
---
# <span data-ttu-id="c9041-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="c9041-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="c9041-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9041-102">SYNOPSIS</span></span>
<span data-ttu-id="c9041-103">Добавляет правило рестикции Access в Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c9041-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="c9041-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c9041-104">SYNTAX</span></span>

### <span data-ttu-id="c9041-105">IpAddressParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9041-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9041-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9041-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9041-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9041-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9041-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9041-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9041-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9041-109">DESCRIPTION</span></span>
<span data-ttu-id="c9041-110">Cmdlet **Add-AzWebAppAccessRestrictionRule** добавляет правило ограничения доступа в Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c9041-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="c9041-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c9041-111">EXAMPLES</span></span>

### <span data-ttu-id="c9041-112">Пример 1. Добавление правила ограничения доступа IpAddress в веб-приложение</span><span class="sxs-lookup"><span data-stu-id="c9041-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="c9041-113">Эта команда добавляет правило ограничения доступа с приоритетом 200 и диапазоном IP-адресов к веб-приложению ContosoSite, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c9041-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="c9041-114">Пример 2. Добавление правила ограничения доступа конечной точки службы подсеть в веб-приложение</span><span class="sxs-lookup"><span data-stu-id="c9041-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="c9041-115">Эта команда добавляет правило ограничения доступа с приоритетом 300 и с подсеть appgw-subnet в corp-vnet к веб-приложению ContosoSite, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c9041-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="c9041-116">Пример 3. Добавление правила ограничения доступа к сотех службе в веб-приложении</span><span class="sxs-lookup"><span data-stu-id="c9041-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="c9041-117">Эта команда добавляет правило ограничения доступа с приоритетом 200 и тегом службы, представляющим область ip-адресов Azure Front Door, в веб-приложение ContosoSite, принадлежащее группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c9041-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="c9041-118">Пример 4. Добавление правила ограничения доступа с несколькими адресами в веб-приложение</span><span class="sxs-lookup"><span data-stu-id="c9041-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="c9041-119">Эта команда добавляет правило ограничения доступа с приоритетом 200 и двумя диапазонами IP-адресов в веб-приложение ContosoSite, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c9041-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="c9041-120">Пример 5. Добавление правила ограничения доступа с помощью http-загона в веб-приложение</span><span class="sxs-lookup"><span data-stu-id="c9041-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="c9041-121">Эта команда добавляет правило ограничения доступа с приоритетом 400 для службы AzureFrontDoor.Backend и дополнительно ограничивает доступ только к http-заглавным именам определенных значений веб-приложению ContosoSite, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c9041-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c9041-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9041-122">PARAMETERS</span></span>

### <span data-ttu-id="c9041-123">-Action</span><span class="sxs-lookup"><span data-stu-id="c9041-123">-Action</span></span>
<span data-ttu-id="c9041-124">"Разрешить или запретить правило".</span><span class="sxs-lookup"><span data-stu-id="c9041-124">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="c9041-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9041-125">-DefaultProfile</span></span>
<span data-ttu-id="c9041-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9041-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9041-127">-Description</span><span class="sxs-lookup"><span data-stu-id="c9041-127">-Description</span></span>
<span data-ttu-id="c9041-128">Описание ограничения доступа.</span><span class="sxs-lookup"><span data-stu-id="c9041-128">Access Restriction description.</span></span>

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

### <span data-ttu-id="c9041-129">-HttpHeader</span><span class="sxs-lookup"><span data-stu-id="c9041-129">-HttpHeader</span></span>
<span data-ttu-id="c9041-130">Ограничения на заглавные ссылки http.</span><span class="sxs-lookup"><span data-stu-id="c9041-130">Http header restrictions.</span></span> <span data-ttu-id="c9041-131">Пример: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span><span class="sxs-lookup"><span data-stu-id="c9041-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9041-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9041-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="c9041-133">Укажите, должна ли проверка регистрации конечной точки службы в подсети.</span><span class="sxs-lookup"><span data-stu-id="c9041-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

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

### <span data-ttu-id="c9041-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="c9041-134">-IpAddress</span></span>
<span data-ttu-id="c9041-135">Диапазон IP-адресов 4 или 6 CIDR.</span><span class="sxs-lookup"><span data-stu-id="c9041-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="c9041-136">Например: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="c9041-136">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="c9041-137">-Name</span><span class="sxs-lookup"><span data-stu-id="c9041-137">-Name</span></span>
<span data-ttu-id="c9041-138">Имя правила</span><span class="sxs-lookup"><span data-stu-id="c9041-138">Rule Name</span></span>

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

### <span data-ttu-id="c9041-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9041-139">-PassThru</span></span>
<span data-ttu-id="c9041-140">Возвращает объект config с ограничением доступа.</span><span class="sxs-lookup"><span data-stu-id="c9041-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="c9041-141">-Priority</span><span class="sxs-lookup"><span data-stu-id="c9041-141">-Priority</span></span>
<span data-ttu-id="c9041-142">Приоритет ограничений доступа.</span><span class="sxs-lookup"><span data-stu-id="c9041-142">Access Restriction priority.</span></span> <span data-ttu-id="c9041-143">Например: 500.</span><span class="sxs-lookup"><span data-stu-id="c9041-143">E.g.: 500.</span></span>

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

### <span data-ttu-id="c9041-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9041-144">-ResourceGroupName</span></span>
<span data-ttu-id="c9041-145">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c9041-145">Resource Group Name</span></span>

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

### <span data-ttu-id="c9041-146">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="c9041-146">-ServiceTag</span></span>
<span data-ttu-id="c9041-147">Имя тега службы</span><span class="sxs-lookup"><span data-stu-id="c9041-147">Name of Service Tag</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9041-148">-SlotName</span><span class="sxs-lookup"><span data-stu-id="c9041-148">-SlotName</span></span>
<span data-ttu-id="c9041-149">Название слота развертывания.</span><span class="sxs-lookup"><span data-stu-id="c9041-149">Deployment Slot name.</span></span>

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

### <span data-ttu-id="c9041-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c9041-150">-SubnetId</span></span>
<span data-ttu-id="c9041-151">ResourceId подсети.</span><span class="sxs-lookup"><span data-stu-id="c9041-151">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="c9041-152">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c9041-152">-SubnetName</span></span>
<span data-ttu-id="c9041-153">Имя подсети.</span><span class="sxs-lookup"><span data-stu-id="c9041-153">Name of Subnet.</span></span>

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

### <span data-ttu-id="c9041-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="c9041-154">-TargetScmSite</span></span>
<span data-ttu-id="c9041-155">Правило ориентировано на основной сайт или SCM-сайт.</span><span class="sxs-lookup"><span data-stu-id="c9041-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="c9041-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c9041-156">-VirtualNetworkName</span></span>
<span data-ttu-id="c9041-157">Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c9041-157">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="c9041-158">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="c9041-158">-WebAppName</span></span>
<span data-ttu-id="c9041-159">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c9041-159">The name of the web app.</span></span>

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

### <span data-ttu-id="c9041-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9041-160">-Confirm</span></span>
<span data-ttu-id="c9041-161">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9041-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9041-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9041-162">-WhatIf</span></span>
<span data-ttu-id="c9041-163">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9041-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9041-164">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c9041-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9041-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9041-165">CommonParameters</span></span>
<span data-ttu-id="c9041-166">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9041-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9041-167">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9041-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9041-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9041-168">INPUTS</span></span>

### <span data-ttu-id="c9041-169">System.String</span><span class="sxs-lookup"><span data-stu-id="c9041-169">System.String</span></span>

## <span data-ttu-id="c9041-170">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c9041-170">OUTPUTS</span></span>

### <span data-ttu-id="c9041-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="c9041-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="c9041-172">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c9041-172">NOTES</span></span>

## <span data-ttu-id="c9041-173">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9041-173">RELATED LINKS</span></span>

[<span data-ttu-id="c9041-174">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="c9041-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="c9041-175">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="c9041-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="c9041-176">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="c9041-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
