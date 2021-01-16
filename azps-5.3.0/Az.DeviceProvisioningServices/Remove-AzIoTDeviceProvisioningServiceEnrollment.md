---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8b16d95d582e29be6f49cac9eaeb00bcda67de0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420471"
---
# <span data-ttu-id="2abc8-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="2abc8-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="2abc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2abc8-102">SYNOPSIS</span></span>
<span data-ttu-id="2abc8-103">Удаление записи о регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="2abc8-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="2abc8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2abc8-104">SYNTAX</span></span>

### <span data-ttu-id="2abc8-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2abc8-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2abc8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2abc8-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2abc8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2abc8-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2abc8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2abc8-108">DESCRIPTION</span></span>
<span data-ttu-id="2abc8-109">Удалите регистрацию устройства в службе регистрации устройств azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="2abc8-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="2abc8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2abc8-110">EXAMPLES</span></span>

### <span data-ttu-id="2abc8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2abc8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="2abc8-112">Удаление указанной записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="2abc8-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="2abc8-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2abc8-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="2abc8-114">Удалите все записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="2abc8-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="2abc8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2abc8-115">PARAMETERS</span></span>

### <span data-ttu-id="2abc8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2abc8-116">-DefaultProfile</span></span>
<span data-ttu-id="2abc8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2abc8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2abc8-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="2abc8-118">-DpsName</span></span>
<span data-ttu-id="2abc8-119">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="2abc8-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2abc8-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2abc8-120">-DpsObject</span></span>
<span data-ttu-id="2abc8-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="2abc8-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2abc8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2abc8-122">-PassThru</span></span>
<span data-ttu-id="2abc8-123">Разрешает возвращать boolean object.</span><span class="sxs-lookup"><span data-stu-id="2abc8-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="2abc8-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2abc8-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2abc8-125">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="2abc8-125">-RegistrationId</span></span>
<span data-ttu-id="2abc8-126">Индивидуальный регистрационный номер.</span><span class="sxs-lookup"><span data-stu-id="2abc8-126">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="2abc8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2abc8-127">-ResourceGroupName</span></span>
<span data-ttu-id="2abc8-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2abc8-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2abc8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2abc8-129">-ResourceId</span></span>
<span data-ttu-id="2abc8-130">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="2abc8-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2abc8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2abc8-131">-Confirm</span></span>
<span data-ttu-id="2abc8-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2abc8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2abc8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2abc8-133">-WhatIf</span></span>
<span data-ttu-id="2abc8-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2abc8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2abc8-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2abc8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2abc8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2abc8-136">CommonParameters</span></span>
<span data-ttu-id="2abc8-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2abc8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2abc8-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2abc8-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2abc8-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2abc8-139">INPUTS</span></span>

### <span data-ttu-id="2abc8-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2abc8-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2abc8-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2abc8-141">System.String</span></span>

## <span data-ttu-id="2abc8-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2abc8-142">OUTPUTS</span></span>

### <span data-ttu-id="2abc8-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2abc8-143">System.Boolean</span></span>

## <span data-ttu-id="2abc8-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2abc8-144">NOTES</span></span>

## <span data-ttu-id="2abc8-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2abc8-145">RELATED LINKS</span></span>
