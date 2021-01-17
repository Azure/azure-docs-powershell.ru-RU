---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425284"
---
# <span data-ttu-id="eb761-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="eb761-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="eb761-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb761-102">SYNOPSIS</span></span>
<span data-ttu-id="eb761-103">Создание сайта, подключенного к сетевому виртуальному устройству.</span><span class="sxs-lookup"><span data-stu-id="eb761-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="eb761-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eb761-104">SYNTAX</span></span>

### <span data-ttu-id="eb761-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eb761-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb761-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb761-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb761-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb761-107">DESCRIPTION</span></span>
<span data-ttu-id="eb761-108">Команда New-AzVirtualApplianceSite создает сайт виртуального устройства, подключенного к ресурсу сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="eb761-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="eb761-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eb761-109">EXAMPLES</span></span>

### <span data-ttu-id="eb761-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eb761-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="eb761-111">Создайте сайт виртуальной устройства в группе ресурсов Testrg.</span><span class="sxs-lookup"><span data-stu-id="eb761-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="eb761-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb761-112">PARAMETERS</span></span>

### <span data-ttu-id="eb761-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="eb761-113">-AddressPrefix</span></span>
<span data-ttu-id="eb761-114">Префикс адреса сайта.</span><span class="sxs-lookup"><span data-stu-id="eb761-114">The address prefix for the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb761-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb761-115">-AsJob</span></span>
<span data-ttu-id="eb761-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="eb761-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb761-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb761-117">-DefaultProfile</span></span>
<span data-ttu-id="eb761-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb761-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb761-119">-Force</span><span class="sxs-lookup"><span data-stu-id="eb761-119">-Force</span></span>
<span data-ttu-id="eb761-120">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="eb761-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="eb761-121">-Name</span><span class="sxs-lookup"><span data-stu-id="eb761-121">-Name</span></span>
<span data-ttu-id="eb761-122">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="eb761-122">The resource name.</span></span>

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

### <span data-ttu-id="eb761-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="eb761-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="eb761-124">Сетевой виртуальный аппарат, к который подключен этот сайт.</span><span class="sxs-lookup"><span data-stu-id="eb761-124">The Network virtual appliance that this site is attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb761-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="eb761-125">-O365Policy</span></span>
<span data-ttu-id="eb761-126">Политика разорвать Office 365.</span><span class="sxs-lookup"><span data-stu-id="eb761-126">The Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb761-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb761-127">-ResourceGroupName</span></span>
<span data-ttu-id="eb761-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb761-128">The resource group name.</span></span>

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

### <span data-ttu-id="eb761-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb761-129">-ResourceId</span></span>
<span data-ttu-id="eb761-130">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="eb761-130">The resource id.</span></span>

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

### <span data-ttu-id="eb761-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="eb761-131">-Tag</span></span>
<span data-ttu-id="eb761-132">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="eb761-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb761-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb761-133">-Confirm</span></span>
<span data-ttu-id="eb761-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb761-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb761-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb761-135">-WhatIf</span></span>
<span data-ttu-id="eb761-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb761-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb761-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eb761-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb761-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb761-138">CommonParameters</span></span>
<span data-ttu-id="eb761-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb761-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb761-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb761-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb761-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb761-141">INPUTS</span></span>

### <span data-ttu-id="eb761-142">System.String</span><span class="sxs-lookup"><span data-stu-id="eb761-142">System.String</span></span>

### <span data-ttu-id="eb761-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="eb761-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="eb761-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="eb761-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eb761-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eb761-145">OUTPUTS</span></span>

### <span data-ttu-id="eb761-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="eb761-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="eb761-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eb761-147">NOTES</span></span>

## <span data-ttu-id="eb761-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb761-148">RELATED LINKS</span></span>
