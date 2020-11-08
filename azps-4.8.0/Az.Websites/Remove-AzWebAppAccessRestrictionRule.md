---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: ad0bdc95ea3d582a2f8b6b6b1f8bc772c795352c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079313"
---
# <span data-ttu-id="51e4e-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="51e4e-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="51e4e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="51e4e-103">Удаляет правило ограничения доступа из веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="51e4e-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="51e4e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51e4e-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-TargetScmSite] [-SlotName <String>] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51e4e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51e4e-105">DESCRIPTION</span></span>
<span data-ttu-id="51e4e-106">Командлет **Remove-AzWebAppAccessRestrictionRule** удаляет правило ограничения доступа из веб-приложения Azure</span><span class="sxs-lookup"><span data-stu-id="51e4e-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="51e4e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51e4e-107">EXAMPLES</span></span>

### <span data-ttu-id="51e4e-108">Пример 1: Удаление правила ограничения доступа для веб-приложения</span><span class="sxs-lookup"><span data-stu-id="51e4e-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="51e4e-109">Эта команда удаляет правило ограничения доступа IpRule из Azure Web App с именем ContosoSite, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="51e4e-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="51e4e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51e4e-110">PARAMETERS</span></span>

### <span data-ttu-id="51e4e-111">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="51e4e-111">-Action</span></span>
<span data-ttu-id="51e4e-112">Правило разрешения или отказа.</span><span class="sxs-lookup"><span data-stu-id="51e4e-112">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="51e4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e4e-113">-DefaultProfile</span></span>
<span data-ttu-id="51e4e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51e4e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51e4e-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="51e4e-115">-IpAddress</span></span>
<span data-ttu-id="51e4e-116">Диапазон CIDR для IP-адреса v4 или V6.</span><span class="sxs-lookup"><span data-stu-id="51e4e-116">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="51e4e-117">Например: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="51e4e-117">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="51e4e-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="51e4e-118">-Name</span></span>
<span data-ttu-id="51e4e-119">Имя правила ограничения доступа</span><span class="sxs-lookup"><span data-stu-id="51e4e-119">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="51e4e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51e4e-120">-PassThru</span></span>
<span data-ttu-id="51e4e-121">Возврат объекта конфигурации ограничения доступа.</span><span class="sxs-lookup"><span data-stu-id="51e4e-121">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="51e4e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e4e-122">-ResourceGroupName</span></span>
<span data-ttu-id="51e4e-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="51e4e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="51e4e-124">-SlotName</span><span class="sxs-lookup"><span data-stu-id="51e4e-124">-SlotName</span></span>
<span data-ttu-id="51e4e-125">Имя слота развертывания.</span><span class="sxs-lookup"><span data-stu-id="51e4e-125">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="51e4e-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="51e4e-126">-SubnetId</span></span>
<span data-ttu-id="51e4e-127">ResourceId подсети.</span><span class="sxs-lookup"><span data-stu-id="51e4e-127">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="51e4e-128">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="51e4e-128">-SubnetName</span></span>
<span data-ttu-id="51e4e-129">Имя подсети.</span><span class="sxs-lookup"><span data-stu-id="51e4e-129">Name of Subnet.</span></span>

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

### <span data-ttu-id="51e4e-130">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="51e4e-130">-TargetScmSite</span></span>
<span data-ttu-id="51e4e-131">Правило предназначено для основного сайта или сайта SCM.</span><span class="sxs-lookup"><span data-stu-id="51e4e-131">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="51e4e-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="51e4e-132">-VirtualNetworkName</span></span>
<span data-ttu-id="51e4e-133">Имя виртуальной сети (должно быть в той же группе ресурсов, что и веб-приложение).</span><span class="sxs-lookup"><span data-stu-id="51e4e-133">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="51e4e-134">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="51e4e-134">-WebAppName</span></span>
<span data-ttu-id="51e4e-135">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="51e4e-135">The name of the web app.</span></span>

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

### <span data-ttu-id="51e4e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51e4e-136">-Confirm</span></span>
<span data-ttu-id="51e4e-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="51e4e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51e4e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51e4e-138">-WhatIf</span></span>
<span data-ttu-id="51e4e-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="51e4e-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51e4e-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="51e4e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51e4e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e4e-141">CommonParameters</span></span>
<span data-ttu-id="51e4e-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51e4e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e4e-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51e4e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e4e-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51e4e-144">INPUTS</span></span>

### <span data-ttu-id="51e4e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="51e4e-145">System.String</span></span>

## <span data-ttu-id="51e4e-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51e4e-146">OUTPUTS</span></span>

### <span data-ttu-id="51e4e-147">Microsoft. Azure. Commands. Apps. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="51e4e-147">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="51e4e-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="51e4e-148">NOTES</span></span>

## <span data-ttu-id="51e4e-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51e4e-149">RELATED LINKS</span></span>

[<span data-ttu-id="51e4e-150">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="51e4e-150">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="51e4e-151">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="51e4e-151">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="51e4e-152">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="51e4e-152">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
