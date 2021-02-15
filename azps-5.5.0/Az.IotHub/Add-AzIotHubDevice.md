---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222337"
---
# <span data-ttu-id="43e46-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="43e46-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="43e46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43e46-102">SYNOPSIS</span></span>
<span data-ttu-id="43e46-103">Создайте устройство в концентраторе IoT.</span><span class="sxs-lookup"><span data-stu-id="43e46-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="43e46-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="43e46-104">SYNTAX</span></span>

### <span data-ttu-id="43e46-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43e46-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e46-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="43e46-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43e46-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="43e46-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43e46-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43e46-108">DESCRIPTION</span></span>
<span data-ttu-id="43e46-109">Создайте устройство с другим типом авторизации в центре IoT.</span><span class="sxs-lookup"><span data-stu-id="43e46-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="43e46-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="43e46-110">EXAMPLES</span></span>

### <span data-ttu-id="43e46-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43e46-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="43e46-112">Создайте устройство IoT с поддержкой edge с авторизацией по умолчанию (общий закрытый ключ).</span><span class="sxs-lookup"><span data-stu-id="43e46-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="43e46-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="43e46-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="43e46-114">Создайте устройство IoT с корневой авторизацией ЦС с отключенным состоянием и причиной.</span><span class="sxs-lookup"><span data-stu-id="43e46-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="43e46-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="43e46-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="43e46-116">Создайте устройство IoT с поддержкой edge и добавьте на него устройства ребенка.</span><span class="sxs-lookup"><span data-stu-id="43e46-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="43e46-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="43e46-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="43e46-118">Создайте устройство IoT и установите его родительское устройство.</span><span class="sxs-lookup"><span data-stu-id="43e46-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="43e46-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43e46-119">PARAMETERS</span></span>

### <span data-ttu-id="43e46-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="43e46-120">-AuthMethod</span></span>
<span data-ttu-id="43e46-121">Тип авторизации для создания сущности.</span><span class="sxs-lookup"><span data-stu-id="43e46-121">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e46-122">-Дети</span><span class="sxs-lookup"><span data-stu-id="43e46-122">-Children</span></span>
<span data-ttu-id="43e46-123">Список устройств ребенка (разделенный запятой) включает только устройства, не включающее в себя границы.</span><span class="sxs-lookup"><span data-stu-id="43e46-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e46-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e46-124">-DefaultProfile</span></span>
<span data-ttu-id="43e46-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43e46-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43e46-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="43e46-126">-DeviceId</span></span>
<span data-ttu-id="43e46-127">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="43e46-127">Target Device Id.</span></span>

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

### <span data-ttu-id="43e46-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="43e46-128">-EdgeEnabled</span></span>
<span data-ttu-id="43e46-129">Пометка, указывающая на то, что граница включается.</span><span class="sxs-lookup"><span data-stu-id="43e46-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="43e46-130">-Force</span><span class="sxs-lookup"><span data-stu-id="43e46-130">-Force</span></span>
<span data-ttu-id="43e46-131">Переопишет родительское устройство на устройстве, которое не является границым.</span><span class="sxs-lookup"><span data-stu-id="43e46-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="43e46-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43e46-132">-InputObject</span></span>
<span data-ttu-id="43e46-133">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="43e46-133">IotHub object</span></span>

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

### <span data-ttu-id="43e46-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="43e46-134">-IotHubName</span></span>
<span data-ttu-id="43e46-135">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="43e46-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="43e46-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="43e46-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="43e46-137">Явный самозаверяя сертификат, который нужно использовать в качестве первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="43e46-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="43e46-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="43e46-138">-ParentDeviceId</span></span>
<span data-ttu-id="43e46-139">Id of edge device.</span><span class="sxs-lookup"><span data-stu-id="43e46-139">Id of edge device.</span></span>

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

### <span data-ttu-id="43e46-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e46-140">-ResourceGroupName</span></span>
<span data-ttu-id="43e46-141">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="43e46-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="43e46-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43e46-142">-ResourceId</span></span>
<span data-ttu-id="43e46-143">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="43e46-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="43e46-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="43e46-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="43e46-145">Явный самозаверяный эскиз сертификата, который нужно использовать для дополнительного ключа.</span><span class="sxs-lookup"><span data-stu-id="43e46-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="43e46-146">-Status</span><span class="sxs-lookup"><span data-stu-id="43e46-146">-Status</span></span>
<span data-ttu-id="43e46-147">Установите состояние устройства при создании.</span><span class="sxs-lookup"><span data-stu-id="43e46-147">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e46-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="43e46-148">-StatusReason</span></span>
<span data-ttu-id="43e46-149">Описание состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="43e46-149">Description for device status.</span></span>

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

### <span data-ttu-id="43e46-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43e46-150">-Confirm</span></span>
<span data-ttu-id="43e46-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43e46-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43e46-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43e46-152">-WhatIf</span></span>
<span data-ttu-id="43e46-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43e46-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43e46-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="43e46-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43e46-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e46-155">CommonParameters</span></span>
<span data-ttu-id="43e46-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43e46-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e46-157">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43e46-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e46-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43e46-158">INPUTS</span></span>

### <span data-ttu-id="43e46-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="43e46-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="43e46-160">System.String</span><span class="sxs-lookup"><span data-stu-id="43e46-160">System.String</span></span>

## <span data-ttu-id="43e46-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43e46-161">OUTPUTS</span></span>

### <span data-ttu-id="43e46-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="43e46-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="43e46-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="43e46-163">NOTES</span></span>

## <span data-ttu-id="43e46-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43e46-164">RELATED LINKS</span></span>
