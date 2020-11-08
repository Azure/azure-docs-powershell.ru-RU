---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236446"
---
# <span data-ttu-id="16c4f-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="16c4f-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="16c4f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="16c4f-103">Создание устройства в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="16c4f-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="16c4f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16c4f-104">SYNTAX</span></span>

### <span data-ttu-id="16c4f-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16c4f-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16c4f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="16c4f-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16c4f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="16c4f-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16c4f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16c4f-108">DESCRIPTION</span></span>
<span data-ttu-id="16c4f-109">Создание устройства с другим типом авторизации в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="16c4f-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="16c4f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16c4f-110">EXAMPLES</span></span>

### <span data-ttu-id="16c4f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16c4f-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="16c4f-112">Создание пограничного устройства IoT с включенной авторизацией по умолчанию (общего закрытого ключа).</span><span class="sxs-lookup"><span data-stu-id="16c4f-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="16c4f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="16c4f-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="16c4f-114">Создание устройства IoT с авторизацией корневого ЦС с отключенным состоянием и причиной.</span><span class="sxs-lookup"><span data-stu-id="16c4f-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="16c4f-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="16c4f-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="16c4f-116">Создание пограничного устройства IoT и добавление к нему дочерних устройств.</span><span class="sxs-lookup"><span data-stu-id="16c4f-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="16c4f-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="16c4f-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="16c4f-118">Создание устройства IoT и установка родительского устройства.</span><span class="sxs-lookup"><span data-stu-id="16c4f-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="16c4f-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16c4f-119">PARAMETERS</span></span>

### <span data-ttu-id="16c4f-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="16c4f-120">-AuthMethod</span></span>
<span data-ttu-id="16c4f-121">Тип авторизации, с которым будет создана сущность.</span><span class="sxs-lookup"><span data-stu-id="16c4f-121">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="16c4f-122">-Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="16c4f-122">-Children</span></span>
<span data-ttu-id="16c4f-123">Добавить дочерний список устройств (разделенный запятыми) включает только устройства, не имеющие пограничного.</span><span class="sxs-lookup"><span data-stu-id="16c4f-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="16c4f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c4f-124">-DefaultProfile</span></span>
<span data-ttu-id="16c4f-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16c4f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c4f-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="16c4f-126">-DeviceId</span></span>
<span data-ttu-id="16c4f-127">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="16c4f-127">Target Device Id.</span></span>

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

### <span data-ttu-id="16c4f-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="16c4f-128">-EdgeEnabled</span></span>
<span data-ttu-id="16c4f-129">Флаг, указывающий на включение Edge.</span><span class="sxs-lookup"><span data-stu-id="16c4f-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="16c4f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="16c4f-130">-Force</span></span>
<span data-ttu-id="16c4f-131">Перезаписывает родительский объект устройства, не являющегося Edge.</span><span class="sxs-lookup"><span data-stu-id="16c4f-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="16c4f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16c4f-132">-InputObject</span></span>
<span data-ttu-id="16c4f-133">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="16c4f-133">IotHub object</span></span>

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

### <span data-ttu-id="16c4f-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="16c4f-134">-IotHubName</span></span>
<span data-ttu-id="16c4f-135">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="16c4f-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="16c4f-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="16c4f-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="16c4f-137">Явный заверенный отпечаток сертификата для использования в качестве первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="16c4f-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="16c4f-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="16c4f-138">-ParentDeviceId</span></span>
<span data-ttu-id="16c4f-139">Идентификатор устройства Edge.</span><span class="sxs-lookup"><span data-stu-id="16c4f-139">Id of edge device.</span></span>

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

### <span data-ttu-id="16c4f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c4f-140">-ResourceGroupName</span></span>
<span data-ttu-id="16c4f-141">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="16c4f-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="16c4f-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16c4f-142">-ResourceId</span></span>
<span data-ttu-id="16c4f-143">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="16c4f-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="16c4f-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="16c4f-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="16c4f-145">Явный заверенный отпечаток сертификата, который будет использоваться для вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="16c4f-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="16c4f-146">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="16c4f-146">-Status</span></span>
<span data-ttu-id="16c4f-147">Настройка состояния устройства после создания.</span><span class="sxs-lookup"><span data-stu-id="16c4f-147">Set device status upon creation.</span></span>

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

### <span data-ttu-id="16c4f-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="16c4f-148">-StatusReason</span></span>
<span data-ttu-id="16c4f-149">Описание состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="16c4f-149">Description for device status.</span></span>

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

### <span data-ttu-id="16c4f-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16c4f-150">-Confirm</span></span>
<span data-ttu-id="16c4f-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="16c4f-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16c4f-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16c4f-152">-WhatIf</span></span>
<span data-ttu-id="16c4f-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="16c4f-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16c4f-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="16c4f-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16c4f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c4f-155">CommonParameters</span></span>
<span data-ttu-id="16c4f-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16c4f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c4f-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16c4f-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c4f-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16c4f-158">INPUTS</span></span>

### <span data-ttu-id="16c4f-159">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="16c4f-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="16c4f-160">System. String</span><span class="sxs-lookup"><span data-stu-id="16c4f-160">System.String</span></span>

## <span data-ttu-id="16c4f-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16c4f-161">OUTPUTS</span></span>

### <span data-ttu-id="16c4f-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="16c4f-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="16c4f-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="16c4f-163">NOTES</span></span>

## <span data-ttu-id="16c4f-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16c4f-164">RELATED LINKS</span></span>
