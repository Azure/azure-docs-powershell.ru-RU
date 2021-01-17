---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404972"
---
# <span data-ttu-id="fe5c2-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="fe5c2-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="fe5c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe5c2-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5c2-103">Изменение или изменение сайта виртуального устройства, подключенного к ресурсу сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="fe5c2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe5c2-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe5c2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe5c2-105">DESCRIPTION</span></span>
<span data-ttu-id="fe5c2-106">Команда Update-AzVirtualApplianceSite изменяет ресурс сайта виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="fe5c2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe5c2-107">EXAMPLES</span></span>

### <span data-ttu-id="fe5c2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe5c2-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="fe5c2-109">Измените префикс адреса для ресурса сайта виртуальной устройства.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="fe5c2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe5c2-110">PARAMETERS</span></span>

### <span data-ttu-id="fe5c2-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="fe5c2-111">-AddresssPrefix</span></span>
<span data-ttu-id="fe5c2-112">Префикс адреса сайта.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-112">The address prefix for the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5c2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe5c2-113">-AsJob</span></span>
<span data-ttu-id="fe5c2-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fe5c2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe5c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5c2-115">-DefaultProfile</span></span>
<span data-ttu-id="fe5c2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe5c2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fe5c2-117">-Force</span></span>
<span data-ttu-id="fe5c2-118">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="fe5c2-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fe5c2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fe5c2-119">-Name</span></span>
<span data-ttu-id="fe5c2-120">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5c2-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="fe5c2-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="fe5c2-122">Сетевой виртуальный аппарат, к который подключен этот сайт.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="fe5c2-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="fe5c2-123">-O365Policy</span></span>
<span data-ttu-id="fe5c2-124">Политика разорвать Office 365.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe5c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe5c2-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-126">The resource group name.</span></span>

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

### <span data-ttu-id="fe5c2-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe5c2-127">-Tag</span></span>
<span data-ttu-id="fe5c2-128">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fe5c2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe5c2-129">-Confirm</span></span>
<span data-ttu-id="fe5c2-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe5c2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe5c2-131">-WhatIf</span></span>
<span data-ttu-id="fe5c2-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe5c2-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe5c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5c2-134">CommonParameters</span></span>
<span data-ttu-id="fe5c2-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe5c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5c2-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe5c2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5c2-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe5c2-137">INPUTS</span></span>

### <span data-ttu-id="fe5c2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fe5c2-138">System.String</span></span>

### <span data-ttu-id="fe5c2-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="fe5c2-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="fe5c2-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fe5c2-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fe5c2-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe5c2-141">OUTPUTS</span></span>

### <span data-ttu-id="fe5c2-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="fe5c2-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="fe5c2-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe5c2-143">NOTES</span></span>

## <span data-ttu-id="fe5c2-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe5c2-144">RELATED LINKS</span></span>
