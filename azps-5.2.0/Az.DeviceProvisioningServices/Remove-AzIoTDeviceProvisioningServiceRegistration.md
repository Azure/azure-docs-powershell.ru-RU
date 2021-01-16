---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: b0fa84887a54eb1f4e9c689c49fb08a1300cd62b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396647"
---
# <span data-ttu-id="ba9c4-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="ba9c4-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="ba9c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba9c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba9c4-103">Удаляет регистрацию устройства.</span><span class="sxs-lookup"><span data-stu-id="ba9c4-103">Deletes the device registration.</span></span>

## <span data-ttu-id="ba9c4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ba9c4-104">SYNTAX</span></span>

### <span data-ttu-id="ba9c4-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba9c4-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba9c4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ba9c4-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba9c4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ba9c4-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba9c4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba9c4-108">DESCRIPTION</span></span>
<span data-ttu-id="ba9c4-109">Удалите регистрацию устройства в службе регистрации устройств azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="ba9c4-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="ba9c4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ba9c4-110">EXAMPLES</span></span>

### <span data-ttu-id="ba9c4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba9c4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="ba9c4-112">Удалите регистрацию устройства в службе регистрации устройств azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="ba9c4-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="ba9c4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba9c4-113">PARAMETERS</span></span>

### <span data-ttu-id="ba9c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba9c4-114">-DefaultProfile</span></span>
<span data-ttu-id="ba9c4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba9c4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba9c4-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="ba9c4-116">-DpsName</span></span>
<span data-ttu-id="ba9c4-117">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="ba9c4-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ba9c4-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="ba9c4-118">-DpsObject</span></span>
<span data-ttu-id="ba9c4-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="ba9c4-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ba9c4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba9c4-120">-PassThru</span></span>
<span data-ttu-id="ba9c4-121">Возвращает объект boolean.</span><span class="sxs-lookup"><span data-stu-id="ba9c4-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="ba9c4-122">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ba9c4-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ba9c4-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="ba9c4-123">-RegistrationId</span></span>
<span data-ttu-id="ba9c4-124">ИД регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="ba9c4-124">ID of device registration.</span></span>

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

### <span data-ttu-id="ba9c4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba9c4-125">-ResourceGroupName</span></span>
<span data-ttu-id="ba9c4-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ba9c4-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ba9c4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba9c4-127">-ResourceId</span></span>
<span data-ttu-id="ba9c4-128">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="ba9c4-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ba9c4-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba9c4-129">-Confirm</span></span>
<span data-ttu-id="ba9c4-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba9c4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba9c4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba9c4-131">-WhatIf</span></span>
<span data-ttu-id="ba9c4-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba9c4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba9c4-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ba9c4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba9c4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba9c4-134">CommonParameters</span></span>
<span data-ttu-id="ba9c4-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba9c4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba9c4-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba9c4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba9c4-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba9c4-137">INPUTS</span></span>

### <span data-ttu-id="ba9c4-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ba9c4-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="ba9c4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ba9c4-139">System.String</span></span>

## <span data-ttu-id="ba9c4-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba9c4-140">OUTPUTS</span></span>

### <span data-ttu-id="ba9c4-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba9c4-141">System.Boolean</span></span>

## <span data-ttu-id="ba9c4-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ba9c4-142">NOTES</span></span>

## <span data-ttu-id="ba9c4-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba9c4-143">RELATED LINKS</span></span>
