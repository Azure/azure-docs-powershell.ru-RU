---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995823"
---
# <span data-ttu-id="0226a-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="0226a-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="0226a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0226a-102">SYNOPSIS</span></span>
<span data-ttu-id="0226a-103">Удаляет правило ограничения доступа из Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0226a-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="0226a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0226a-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0226a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0226a-105">DESCRIPTION</span></span>
<span data-ttu-id="0226a-106">С **помощью cmdlet Remove-AzWebAppAccessRestrictionRule** можно удалить правило ограничения доступа для Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0226a-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="0226a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0226a-107">EXAMPLES</span></span>

### <span data-ttu-id="0226a-108">Пример 1. Удаление правила ограничения доступа к веб-приложению</span><span class="sxs-lookup"><span data-stu-id="0226a-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="0226a-109">Эта команда удаляет правило ограничения доступа IpRule для Azure Web App ContosoSite, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="0226a-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="0226a-110">Пример 2. Удаление правила ограничения доступа к веб-приложению "Тег службы"</span><span class="sxs-lookup"><span data-stu-id="0226a-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="0226a-111">Эта команда удаляет правило ограничения доступа с тем, что дляtag службы равняется AzureFrontDoor.Backend из Azure Web App ContosoSite, который принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="0226a-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0226a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0226a-112">PARAMETERS</span></span>

### <span data-ttu-id="0226a-113">-Action</span><span class="sxs-lookup"><span data-stu-id="0226a-113">-Action</span></span>
<span data-ttu-id="0226a-114">"Разрешить или запретить правило".</span><span class="sxs-lookup"><span data-stu-id="0226a-114">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0226a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0226a-115">-DefaultProfile</span></span>
<span data-ttu-id="0226a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0226a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0226a-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="0226a-117">-IpAddress</span></span>
<span data-ttu-id="0226a-118">Диапазон IP-адресов 4 или 6 CIDR.</span><span class="sxs-lookup"><span data-stu-id="0226a-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="0226a-119">Например: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="0226a-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="0226a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0226a-120">-Name</span></span>
<span data-ttu-id="0226a-121">Имя ограничения доступа к правилу</span><span class="sxs-lookup"><span data-stu-id="0226a-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="0226a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0226a-122">-PassThru</span></span>
<span data-ttu-id="0226a-123">Возвращает объект config с ограничением доступа.</span><span class="sxs-lookup"><span data-stu-id="0226a-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="0226a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0226a-124">-ResourceGroupName</span></span>
<span data-ttu-id="0226a-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0226a-125">Resource Group Name</span></span>

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

### <span data-ttu-id="0226a-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="0226a-126">-ServiceTag</span></span>
<span data-ttu-id="0226a-127">Имя тега службы</span><span class="sxs-lookup"><span data-stu-id="0226a-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="0226a-128">-SlotName</span><span class="sxs-lookup"><span data-stu-id="0226a-128">-SlotName</span></span>
<span data-ttu-id="0226a-129">Название слота развертывания.</span><span class="sxs-lookup"><span data-stu-id="0226a-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="0226a-130">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0226a-130">-SubnetId</span></span>
<span data-ttu-id="0226a-131">ResourceId подсети.</span><span class="sxs-lookup"><span data-stu-id="0226a-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="0226a-132">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="0226a-132">-SubnetName</span></span>
<span data-ttu-id="0226a-133">Имя подсети.</span><span class="sxs-lookup"><span data-stu-id="0226a-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="0226a-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="0226a-134">-TargetScmSite</span></span>
<span data-ttu-id="0226a-135">Правило ориентировано на основной сайт или SCM-сайт.</span><span class="sxs-lookup"><span data-stu-id="0226a-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="0226a-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0226a-136">-VirtualNetworkName</span></span>
<span data-ttu-id="0226a-137">Имя виртуальной сети (должно быть в той же группе ресурсов, что и в Web App).</span><span class="sxs-lookup"><span data-stu-id="0226a-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="0226a-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="0226a-138">-WebAppName</span></span>
<span data-ttu-id="0226a-139">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="0226a-139">The name of the web app.</span></span>

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

### <span data-ttu-id="0226a-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0226a-140">-Confirm</span></span>
<span data-ttu-id="0226a-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0226a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0226a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0226a-142">-WhatIf</span></span>
<span data-ttu-id="0226a-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0226a-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0226a-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0226a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0226a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0226a-145">CommonParameters</span></span>
<span data-ttu-id="0226a-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0226a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0226a-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0226a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0226a-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0226a-148">INPUTS</span></span>

### <span data-ttu-id="0226a-149">System.String</span><span class="sxs-lookup"><span data-stu-id="0226a-149">System.String</span></span>

## <span data-ttu-id="0226a-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0226a-150">OUTPUTS</span></span>

### <span data-ttu-id="0226a-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="0226a-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="0226a-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0226a-152">NOTES</span></span>

## <span data-ttu-id="0226a-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0226a-153">RELATED LINKS</span></span>

[<span data-ttu-id="0226a-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="0226a-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="0226a-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="0226a-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="0226a-156">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="0226a-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
