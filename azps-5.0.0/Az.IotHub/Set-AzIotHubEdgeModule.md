---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250245"
---
# <span data-ttu-id="d95f9-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="d95f9-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="d95f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d95f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d95f9-103">Настройте краевые модули на одном пограничном устройстве.</span><span class="sxs-lookup"><span data-stu-id="d95f9-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="d95f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d95f9-104">SYNTAX</span></span>

### <span data-ttu-id="d95f9-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d95f9-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d95f9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d95f9-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d95f9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d95f9-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d95f9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d95f9-108">DESCRIPTION</span></span>
<span data-ttu-id="d95f9-109">Применяет содержимое конфигурации указанных модулей к указанному пограничному устройству.</span><span class="sxs-lookup"><span data-stu-id="d95f9-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="d95f9-110">Примечание. при выполнении команды будет выводиться коллекция модулей, примененных к устройству.</span><span class="sxs-lookup"><span data-stu-id="d95f9-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="d95f9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d95f9-111">EXAMPLES</span></span>

### <span data-ttu-id="d95f9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d95f9-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="d95f9-113">Тестирование модулей EDGE во время разработки путем настройки модулей на целевом устройстве.</span><span class="sxs-lookup"><span data-stu-id="d95f9-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="d95f9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d95f9-114">PARAMETERS</span></span>

### <span data-ttu-id="d95f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d95f9-115">-DefaultProfile</span></span>
<span data-ttu-id="d95f9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d95f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d95f9-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d95f9-117">-DeviceId</span></span>
<span data-ttu-id="d95f9-118">Идентификатор целевого устройства с оконечными краями.</span><span class="sxs-lookup"><span data-stu-id="d95f9-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="d95f9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d95f9-119">-InputObject</span></span>
<span data-ttu-id="d95f9-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="d95f9-120">IotHub object</span></span>

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

### <span data-ttu-id="d95f9-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d95f9-121">-IotHubName</span></span>
<span data-ttu-id="d95f9-122">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="d95f9-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d95f9-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="d95f9-123">-ModulesContent</span></span>
<span data-ttu-id="d95f9-124">Содержимое конфигурации модулей для устройств с границами Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="d95f9-124">Configuration content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="d95f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d95f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="d95f9-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d95f9-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d95f9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d95f9-127">-ResourceId</span></span>
<span data-ttu-id="d95f9-128">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="d95f9-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d95f9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d95f9-129">-Confirm</span></span>
<span data-ttu-id="d95f9-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d95f9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d95f9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d95f9-131">-WhatIf</span></span>
<span data-ttu-id="d95f9-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d95f9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d95f9-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d95f9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d95f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95f9-134">CommonParameters</span></span>
<span data-ttu-id="d95f9-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d95f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95f9-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d95f9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95f9-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d95f9-137">INPUTS</span></span>

### <span data-ttu-id="d95f9-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d95f9-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d95f9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d95f9-139">System.String</span></span>

## <span data-ttu-id="d95f9-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d95f9-140">OUTPUTS</span></span>

### <span data-ttu-id="d95f9-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSModules []</span><span class="sxs-lookup"><span data-stu-id="d95f9-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="d95f9-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="d95f9-142">NOTES</span></span>

## <span data-ttu-id="d95f9-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d95f9-143">RELATED LINKS</span></span>
