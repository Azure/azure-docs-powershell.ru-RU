---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 5f4cfe702b975bf69098aa3c002c756b5cf3da78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420484"
---
# <span data-ttu-id="3eef4-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3eef4-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="3eef4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eef4-102">SYNOPSIS</span></span>
<span data-ttu-id="3eef4-103">Удалите политики общего доступа в службе azure IoT Hub для устройств.</span><span class="sxs-lookup"><span data-stu-id="3eef4-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3eef4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3eef4-104">SYNTAX</span></span>

### <span data-ttu-id="3eef4-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3eef4-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3eef4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3eef4-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eef4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3eef4-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eef4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3eef4-108">DESCRIPTION</span></span>
<span data-ttu-id="3eef4-109">Введение в службу по подготовкам устройств через Azure IoT см. в https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="3eef4-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="3eef4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3eef4-110">EXAMPLES</span></span>

### <span data-ttu-id="3eef4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3eef4-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="3eef4-112">Удалите политику общего доступа "mypolicy" в службе по подготовкам устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3eef4-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="3eef4-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3eef4-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="3eef4-114">Удалите политику общего доступа "mypolicy" в службе по подготовкам устройств через Azure IoT Hub с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="3eef4-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="3eef4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3eef4-115">PARAMETERS</span></span>

### <span data-ttu-id="3eef4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eef4-116">-DefaultProfile</span></span>
<span data-ttu-id="3eef4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3eef4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eef4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eef4-118">-InputObject</span></span>
<span data-ttu-id="3eef4-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="3eef4-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eef4-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3eef4-120">-KeyName</span></span>
<span data-ttu-id="3eef4-121">Имя ключа политики доступа к службе предварительного доступа к устройствам IoT</span><span class="sxs-lookup"><span data-stu-id="3eef4-121">IoT Device Provisioning Service access policy key name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eef4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3eef4-122">-Name</span></span>
<span data-ttu-id="3eef4-123">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="3eef4-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3eef4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3eef4-124">-PassThru</span></span>
<span data-ttu-id="3eef4-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3eef4-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3eef4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eef4-126">-ResourceGroupName</span></span>
<span data-ttu-id="3eef4-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3eef4-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3eef4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3eef4-128">-ResourceId</span></span>
<span data-ttu-id="3eef4-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="3eef4-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="3eef4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3eef4-130">-Confirm</span></span>
<span data-ttu-id="3eef4-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3eef4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eef4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eef4-132">-WhatIf</span></span>
<span data-ttu-id="3eef4-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3eef4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eef4-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3eef4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eef4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eef4-135">CommonParameters</span></span>
<span data-ttu-id="3eef4-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eef4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eef4-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eef4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eef4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3eef4-138">INPUTS</span></span>

### <span data-ttu-id="3eef4-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="3eef4-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="3eef4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3eef4-140">System.String</span></span>

## <span data-ttu-id="3eef4-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3eef4-141">OUTPUTS</span></span>

### <span data-ttu-id="3eef4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3eef4-142">System.Boolean</span></span>

## <span data-ttu-id="3eef4-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3eef4-143">NOTES</span></span>

## <span data-ttu-id="3eef4-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3eef4-144">RELATED LINKS</span></span>
