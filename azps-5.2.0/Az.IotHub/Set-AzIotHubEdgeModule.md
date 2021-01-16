---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407756"
---
# <span data-ttu-id="74ad4-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="74ad4-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="74ad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="74ad4-103">Установите модули edge на одном устройстве с одним краем.</span><span class="sxs-lookup"><span data-stu-id="74ad4-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="74ad4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="74ad4-104">SYNTAX</span></span>

### <span data-ttu-id="74ad4-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74ad4-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74ad4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="74ad4-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74ad4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="74ad4-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74ad4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74ad4-108">DESCRIPTION</span></span>
<span data-ttu-id="74ad4-109">Применяет содержимое конфигурации предоставленных модулей к указанному устройству границы.</span><span class="sxs-lookup"><span data-stu-id="74ad4-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="74ad4-110">Примечание. При выполнении команды будет выводит коллекцию модулей, примененных к устройству.</span><span class="sxs-lookup"><span data-stu-id="74ad4-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="74ad4-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="74ad4-111">EXAMPLES</span></span>

### <span data-ttu-id="74ad4-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74ad4-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="74ad4-113">Тестировать модули на время разработки, устанавливая модули на целевое устройство.</span><span class="sxs-lookup"><span data-stu-id="74ad4-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="74ad4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74ad4-114">PARAMETERS</span></span>

### <span data-ttu-id="74ad4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ad4-115">-DefaultProfile</span></span>
<span data-ttu-id="74ad4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74ad4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74ad4-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="74ad4-117">-DeviceId</span></span>
<span data-ttu-id="74ad4-118">ИД целевого устройства Edge.</span><span class="sxs-lookup"><span data-stu-id="74ad4-118">Target Edge Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ad4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74ad4-119">-InputObject</span></span>
<span data-ttu-id="74ad4-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="74ad4-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74ad4-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="74ad4-121">-IotHubName</span></span>
<span data-ttu-id="74ad4-122">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="74ad4-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ad4-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="74ad4-123">-ModulesContent</span></span>
<span data-ttu-id="74ad4-124">Содержимое конфигурации модулей для устройств IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="74ad4-124">Configuration content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ad4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74ad4-125">-ResourceGroupName</span></span>
<span data-ttu-id="74ad4-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="74ad4-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ad4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74ad4-127">-ResourceId</span></span>
<span data-ttu-id="74ad4-128">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="74ad4-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74ad4-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74ad4-129">-Confirm</span></span>
<span data-ttu-id="74ad4-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74ad4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74ad4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74ad4-131">-WhatIf</span></span>
<span data-ttu-id="74ad4-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74ad4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74ad4-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="74ad4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74ad4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ad4-134">CommonParameters</span></span>
<span data-ttu-id="74ad4-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74ad4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ad4-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74ad4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ad4-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74ad4-137">INPUTS</span></span>

### <span data-ttu-id="74ad4-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="74ad4-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="74ad4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="74ad4-139">System.String</span></span>

## <span data-ttu-id="74ad4-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="74ad4-140">OUTPUTS</span></span>

### <span data-ttu-id="74ad4-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="74ad4-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="74ad4-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="74ad4-142">NOTES</span></span>

## <span data-ttu-id="74ad4-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74ad4-143">RELATED LINKS</span></span>
