---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250249"
---
# <span data-ttu-id="5922a-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="5922a-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="5922a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5922a-102">SYNOPSIS</span></span>
<span data-ttu-id="5922a-103">Обновите устройство центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="5922a-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="5922a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5922a-104">SYNTAX</span></span>

### <span data-ttu-id="5922a-105">ResourceSetForStatus (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5922a-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5922a-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="5922a-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5922a-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="5922a-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5922a-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="5922a-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5922a-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="5922a-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5922a-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="5922a-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5922a-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="5922a-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5922a-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="5922a-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5922a-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="5922a-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5922a-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5922a-114">DESCRIPTION</span></span>
<span data-ttu-id="5922a-115">Обновите устройство центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="5922a-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="5922a-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5922a-116">EXAMPLES</span></span>

### <span data-ttu-id="5922a-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5922a-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="5922a-118">Включите возможности Edge для устройства.</span><span class="sxs-lookup"><span data-stu-id="5922a-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="5922a-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5922a-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="5922a-120">Отключите состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="5922a-120">Disable device status.</span></span>

### <span data-ttu-id="5922a-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5922a-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="5922a-122">Обновление типа авторизации устройства центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="5922a-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="5922a-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5922a-123">PARAMETERS</span></span>

### <span data-ttu-id="5922a-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="5922a-124">-AuthMethod</span></span>
<span data-ttu-id="5922a-125">Тип авторизации, с которым будет создана сущность.</span><span class="sxs-lookup"><span data-stu-id="5922a-125">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5922a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5922a-126">-DefaultProfile</span></span>
<span data-ttu-id="5922a-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5922a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5922a-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5922a-128">-DeviceId</span></span>
<span data-ttu-id="5922a-129">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="5922a-129">Target Device Id.</span></span>

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

### <span data-ttu-id="5922a-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="5922a-130">-EdgeEnabled</span></span>
<span data-ttu-id="5922a-131">Флаг, указывающий на включение Edge.</span><span class="sxs-lookup"><span data-stu-id="5922a-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: InputObjectSetForEdgeEnabled, ResourceSetForEdgeEnabled, ResourceIdSetForEdgeEnabled
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5922a-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5922a-132">-InputObject</span></span>
<span data-ttu-id="5922a-133">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="5922a-133">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSetForAuth, InputObjectSetForStatus, InputObjectSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5922a-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5922a-134">-IotHubName</span></span>
<span data-ttu-id="5922a-135">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="5922a-135">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5922a-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="5922a-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="5922a-137">Явный заверенный отпечаток сертификата для использования в качестве первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="5922a-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5922a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5922a-138">-ResourceGroupName</span></span>
<span data-ttu-id="5922a-139">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5922a-139">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5922a-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5922a-140">-ResourceId</span></span>
<span data-ttu-id="5922a-141">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="5922a-141">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetForAuth, ResourceIdSetForStatus, ResourceIdSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5922a-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="5922a-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="5922a-143">Явный заверенный отпечаток сертификата, который будет использоваться для вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="5922a-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5922a-144">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="5922a-144">-Status</span></span>
<span data-ttu-id="5922a-145">Настройка состояния устройства после создания.</span><span class="sxs-lookup"><span data-stu-id="5922a-145">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5922a-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="5922a-146">-StatusReason</span></span>
<span data-ttu-id="5922a-147">Описание состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="5922a-147">Description for device status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5922a-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5922a-148">-Confirm</span></span>
<span data-ttu-id="5922a-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5922a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5922a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5922a-150">-WhatIf</span></span>
<span data-ttu-id="5922a-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5922a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5922a-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5922a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5922a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5922a-153">CommonParameters</span></span>
<span data-ttu-id="5922a-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5922a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5922a-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5922a-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5922a-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5922a-156">INPUTS</span></span>

### <span data-ttu-id="5922a-157">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5922a-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5922a-158">System. String</span><span class="sxs-lookup"><span data-stu-id="5922a-158">System.String</span></span>

## <span data-ttu-id="5922a-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5922a-159">OUTPUTS</span></span>

### <span data-ttu-id="5922a-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="5922a-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="5922a-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="5922a-161">NOTES</span></span>

## <span data-ttu-id="5922a-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5922a-162">RELATED LINKS</span></span>