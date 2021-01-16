---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425956"
---
# <span data-ttu-id="972ac-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="972ac-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="972ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="972ac-102">SYNOPSIS</span></span>
<span data-ttu-id="972ac-103">Обновите устройство концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="972ac-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="972ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="972ac-104">SYNTAX</span></span>

### <span data-ttu-id="972ac-105">ResourceSetForStatus (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="972ac-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="972ac-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="972ac-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="972ac-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="972ac-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="972ac-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="972ac-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="972ac-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="972ac-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="972ac-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="972ac-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="972ac-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="972ac-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="972ac-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="972ac-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="972ac-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="972ac-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="972ac-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="972ac-114">DESCRIPTION</span></span>
<span data-ttu-id="972ac-115">Обновите устройство концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="972ac-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="972ac-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="972ac-116">EXAMPLES</span></span>

### <span data-ttu-id="972ac-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="972ac-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="972ac-118">Включи edge capabilities для устройства.</span><span class="sxs-lookup"><span data-stu-id="972ac-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="972ac-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="972ac-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="972ac-120">"Отключить состояние устройства".</span><span class="sxs-lookup"><span data-stu-id="972ac-120">Disable device status.</span></span>

### <span data-ttu-id="972ac-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="972ac-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="972ac-122">Тип авторизации для устройства Iot Hub.</span><span class="sxs-lookup"><span data-stu-id="972ac-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="972ac-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="972ac-123">PARAMETERS</span></span>

### <span data-ttu-id="972ac-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="972ac-124">-AuthMethod</span></span>
<span data-ttu-id="972ac-125">Тип авторизации для создания сущности.</span><span class="sxs-lookup"><span data-stu-id="972ac-125">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="972ac-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="972ac-126">-DefaultProfile</span></span>
<span data-ttu-id="972ac-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="972ac-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="972ac-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="972ac-128">-DeviceId</span></span>
<span data-ttu-id="972ac-129">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="972ac-129">Target Device Id.</span></span>

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

### <span data-ttu-id="972ac-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="972ac-130">-EdgeEnabled</span></span>
<span data-ttu-id="972ac-131">Пометка, указывающая на то, что граница включается.</span><span class="sxs-lookup"><span data-stu-id="972ac-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="972ac-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="972ac-132">-InputObject</span></span>
<span data-ttu-id="972ac-133">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="972ac-133">IotHub object</span></span>

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

### <span data-ttu-id="972ac-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="972ac-134">-IotHubName</span></span>
<span data-ttu-id="972ac-135">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="972ac-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="972ac-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="972ac-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="972ac-137">Явный самозаверяный эскиз сертификата, который нужно использовать в качестве первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="972ac-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="972ac-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="972ac-138">-ResourceGroupName</span></span>
<span data-ttu-id="972ac-139">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="972ac-139">Name of the Resource Group</span></span>

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

### <span data-ttu-id="972ac-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="972ac-140">-ResourceId</span></span>
<span data-ttu-id="972ac-141">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="972ac-141">IotHub Resource Id</span></span>

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

### <span data-ttu-id="972ac-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="972ac-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="972ac-143">Явный самозаверяный эскиз сертификата, который нужно использовать для дополнительного ключа.</span><span class="sxs-lookup"><span data-stu-id="972ac-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="972ac-144">-Status</span><span class="sxs-lookup"><span data-stu-id="972ac-144">-Status</span></span>
<span data-ttu-id="972ac-145">Установите состояние устройства при создании.</span><span class="sxs-lookup"><span data-stu-id="972ac-145">Set device status upon creation.</span></span>

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

### <span data-ttu-id="972ac-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="972ac-146">-StatusReason</span></span>
<span data-ttu-id="972ac-147">Описание состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="972ac-147">Description for device status.</span></span>

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

### <span data-ttu-id="972ac-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="972ac-148">-Confirm</span></span>
<span data-ttu-id="972ac-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="972ac-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="972ac-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="972ac-150">-WhatIf</span></span>
<span data-ttu-id="972ac-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="972ac-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="972ac-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="972ac-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="972ac-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="972ac-153">CommonParameters</span></span>
<span data-ttu-id="972ac-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="972ac-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="972ac-155">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="972ac-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="972ac-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="972ac-156">INPUTS</span></span>

### <span data-ttu-id="972ac-157">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="972ac-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="972ac-158">System.String</span><span class="sxs-lookup"><span data-stu-id="972ac-158">System.String</span></span>

## <span data-ttu-id="972ac-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="972ac-159">OUTPUTS</span></span>

### <span data-ttu-id="972ac-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="972ac-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="972ac-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="972ac-161">NOTES</span></span>

## <span data-ttu-id="972ac-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="972ac-162">RELATED LINKS</span></span>
