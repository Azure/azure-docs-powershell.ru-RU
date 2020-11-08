---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 0b87bece7bca0ea3f534746dd20a163f69f21262
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073801"
---
# <span data-ttu-id="26671-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="26671-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="26671-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26671-102">SYNOPSIS</span></span>
<span data-ttu-id="26671-103">Удалите конфигурацию устройства IoT.</span><span class="sxs-lookup"><span data-stu-id="26671-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="26671-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26671-104">SYNTAX</span></span>

### <span data-ttu-id="26671-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26671-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26671-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="26671-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26671-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="26671-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26671-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26671-108">DESCRIPTION</span></span>
<span data-ttu-id="26671-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="26671-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="26671-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26671-110">EXAMPLES</span></span>

### <span data-ttu-id="26671-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26671-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="26671-112">Удалите конфигурацию устройства IoT.</span><span class="sxs-lookup"><span data-stu-id="26671-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="26671-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26671-113">PARAMETERS</span></span>

### <span data-ttu-id="26671-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26671-114">-DefaultProfile</span></span>
<span data-ttu-id="26671-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26671-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26671-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26671-116">-InputObject</span></span>
<span data-ttu-id="26671-117">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="26671-117">IotHub object</span></span>

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

### <span data-ttu-id="26671-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="26671-118">-IotHubName</span></span>
<span data-ttu-id="26671-119">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="26671-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="26671-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="26671-120">-Name</span></span>
<span data-ttu-id="26671-121">Идентификатор конфигурации.</span><span class="sxs-lookup"><span data-stu-id="26671-121">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="26671-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26671-122">-PassThru</span></span>
<span data-ttu-id="26671-123">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="26671-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="26671-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="26671-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="26671-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26671-125">-ResourceGroupName</span></span>
<span data-ttu-id="26671-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="26671-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="26671-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26671-127">-ResourceId</span></span>
<span data-ttu-id="26671-128">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="26671-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="26671-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26671-129">-Confirm</span></span>
<span data-ttu-id="26671-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26671-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26671-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26671-131">-WhatIf</span></span>
<span data-ttu-id="26671-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26671-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26671-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26671-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26671-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26671-134">CommonParameters</span></span>
<span data-ttu-id="26671-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26671-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26671-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26671-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26671-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26671-137">INPUTS</span></span>

### <span data-ttu-id="26671-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="26671-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="26671-139">System. String</span><span class="sxs-lookup"><span data-stu-id="26671-139">System.String</span></span>

## <span data-ttu-id="26671-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26671-140">OUTPUTS</span></span>

### <span data-ttu-id="26671-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26671-141">System.Boolean</span></span>

## <span data-ttu-id="26671-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="26671-142">NOTES</span></span>

## <span data-ttu-id="26671-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26671-143">RELATED LINKS</span></span>
