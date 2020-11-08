---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244513"
---
# <span data-ttu-id="a8cfb-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="a8cfb-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="a8cfb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="a8cfb-103">Удаление модуля (ов) на целевом устройстве IoT в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="a8cfb-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="a8cfb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8cfb-104">SYNTAX</span></span>

### <span data-ttu-id="a8cfb-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8cfb-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8cfb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a8cfb-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8cfb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a8cfb-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8cfb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8cfb-108">DESCRIPTION</span></span>
<span data-ttu-id="a8cfb-109">Удаление модуля (ов) на целевом устройстве IoT в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="a8cfb-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="a8cfb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8cfb-110">EXAMPLES</span></span>

### <span data-ttu-id="a8cfb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a8cfb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="a8cfb-112">Удаление модуля устройства IOT.</span><span class="sxs-lookup"><span data-stu-id="a8cfb-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="a8cfb-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a8cfb-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="a8cfb-114">Удалите все модули устройств IOT.</span><span class="sxs-lookup"><span data-stu-id="a8cfb-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="a8cfb-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8cfb-115">PARAMETERS</span></span>

### <span data-ttu-id="a8cfb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8cfb-116">-DefaultProfile</span></span>
<span data-ttu-id="a8cfb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8cfb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8cfb-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a8cfb-118">-DeviceId</span></span>
<span data-ttu-id="a8cfb-119">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="a8cfb-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cfb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8cfb-120">-InputObject</span></span>
<span data-ttu-id="a8cfb-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="a8cfb-121">IotHub object</span></span>

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

### <span data-ttu-id="a8cfb-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a8cfb-122">-IotHubName</span></span>
<span data-ttu-id="a8cfb-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="a8cfb-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a8cfb-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="a8cfb-124">-ModuleId</span></span>
<span data-ttu-id="a8cfb-125">Идентификатор целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="a8cfb-125">Target Module Id.</span></span>

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

### <span data-ttu-id="a8cfb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8cfb-126">-PassThru</span></span>
<span data-ttu-id="a8cfb-127">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="a8cfb-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="a8cfb-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a8cfb-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a8cfb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8cfb-129">-ResourceGroupName</span></span>
<span data-ttu-id="a8cfb-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a8cfb-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a8cfb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8cfb-131">-ResourceId</span></span>
<span data-ttu-id="a8cfb-132">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="a8cfb-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a8cfb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8cfb-133">-Confirm</span></span>
<span data-ttu-id="a8cfb-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a8cfb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8cfb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8cfb-135">-WhatIf</span></span>
<span data-ttu-id="a8cfb-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a8cfb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8cfb-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a8cfb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8cfb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8cfb-138">CommonParameters</span></span>
<span data-ttu-id="a8cfb-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8cfb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8cfb-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8cfb-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8cfb-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8cfb-141">INPUTS</span></span>

### <span data-ttu-id="a8cfb-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a8cfb-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a8cfb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a8cfb-143">System.String</span></span>

## <span data-ttu-id="a8cfb-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8cfb-144">OUTPUTS</span></span>

### <span data-ttu-id="a8cfb-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8cfb-145">System.Boolean</span></span>

## <span data-ttu-id="a8cfb-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8cfb-146">NOTES</span></span>

## <span data-ttu-id="a8cfb-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8cfb-147">RELATED LINKS</span></span>
