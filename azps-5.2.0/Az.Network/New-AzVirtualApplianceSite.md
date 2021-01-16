---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391519"
---
# <span data-ttu-id="3cd4c-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="3cd4c-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="3cd4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cd4c-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd4c-103">Создание сайта, подключенного к сетевому виртуальному устройству.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="3cd4c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3cd4c-104">SYNTAX</span></span>

### <span data-ttu-id="3cd4c-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3cd4c-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd4c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cd4c-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cd4c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cd4c-107">DESCRIPTION</span></span>
<span data-ttu-id="3cd4c-108">Команда New-AzVirtualApplianceSite создает сайт виртуального устройства, подключенного к ресурсу сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="3cd4c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3cd4c-109">EXAMPLES</span></span>

### <span data-ttu-id="3cd4c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3cd4c-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="3cd4c-111">Создайте сайт виртуальной устройства в группе ресурсов Testrg.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="3cd4c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cd4c-112">PARAMETERS</span></span>

### <span data-ttu-id="3cd4c-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3cd4c-113">-AddressPrefix</span></span>
<span data-ttu-id="3cd4c-114">Префикс адреса сайта.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="3cd4c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cd4c-115">-AsJob</span></span>
<span data-ttu-id="3cd4c-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3cd4c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cd4c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd4c-117">-DefaultProfile</span></span>
<span data-ttu-id="3cd4c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cd4c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3cd4c-119">-Force</span></span>
<span data-ttu-id="3cd4c-120">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="3cd4c-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3cd4c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3cd4c-121">-Name</span></span>
<span data-ttu-id="3cd4c-122">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-122">The resource name.</span></span>

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

### <span data-ttu-id="3cd4c-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="3cd4c-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="3cd4c-124">Сетевой виртуальный аппарат, к который подключен этот сайт.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="3cd4c-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="3cd4c-125">-O365Policy</span></span>
<span data-ttu-id="3cd4c-126">Политика разорвать Office 365.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-126">The Office 365 breakout policy.</span></span>

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

### <span data-ttu-id="3cd4c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cd4c-127">-ResourceGroupName</span></span>
<span data-ttu-id="3cd4c-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-128">The resource group name.</span></span>

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

### <span data-ttu-id="3cd4c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cd4c-129">-ResourceId</span></span>
<span data-ttu-id="3cd4c-130">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-130">The resource id.</span></span>

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

### <span data-ttu-id="3cd4c-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="3cd4c-131">-Tag</span></span>
<span data-ttu-id="3cd4c-132">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3cd4c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cd4c-133">-Confirm</span></span>
<span data-ttu-id="3cd4c-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cd4c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cd4c-135">-WhatIf</span></span>
<span data-ttu-id="3cd4c-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cd4c-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cd4c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd4c-138">CommonParameters</span></span>
<span data-ttu-id="3cd4c-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cd4c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd4c-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cd4c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd4c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3cd4c-141">INPUTS</span></span>

### <span data-ttu-id="3cd4c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3cd4c-142">System.String</span></span>

### <span data-ttu-id="3cd4c-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="3cd4c-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="3cd4c-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3cd4c-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3cd4c-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3cd4c-145">OUTPUTS</span></span>

### <span data-ttu-id="3cd4c-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="3cd4c-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="3cd4c-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3cd4c-147">NOTES</span></span>

## <span data-ttu-id="3cd4c-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cd4c-148">RELATED LINKS</span></span>
