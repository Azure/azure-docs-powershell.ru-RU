---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 5f4cfe702b975bf69098aa3c002c756b5cf3da78
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066385"
---
# <span data-ttu-id="5af58-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5af58-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="5af58-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5af58-102">SYNOPSIS</span></span>
<span data-ttu-id="5af58-103">Удалите политики общего доступа в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="5af58-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5af58-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5af58-104">SYNTAX</span></span>

### <span data-ttu-id="5af58-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5af58-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5af58-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5af58-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5af58-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5af58-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5af58-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5af58-108">DESCRIPTION</span></span>
<span data-ttu-id="5af58-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5af58-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5af58-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5af58-110">EXAMPLES</span></span>

### <span data-ttu-id="5af58-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5af58-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="5af58-112">Удаление политики общего доступа "mypolicy" в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="5af58-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="5af58-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5af58-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="5af58-114">Удаление политики общего доступа "mypolicy" в службе подготовки устройств центра для Azure IoT с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="5af58-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="5af58-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5af58-115">PARAMETERS</span></span>

### <span data-ttu-id="5af58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af58-116">-DefaultProfile</span></span>
<span data-ttu-id="5af58-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5af58-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5af58-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5af58-118">-InputObject</span></span>
<span data-ttu-id="5af58-119">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="5af58-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5af58-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5af58-120">-KeyName</span></span>
<span data-ttu-id="5af58-121">Имя ключа политики доступа к службе для подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="5af58-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="5af58-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5af58-122">-Name</span></span>
<span data-ttu-id="5af58-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="5af58-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5af58-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5af58-124">-PassThru</span></span>
<span data-ttu-id="5af58-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="5af58-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5af58-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af58-126">-ResourceGroupName</span></span>
<span data-ttu-id="5af58-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5af58-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5af58-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5af58-128">-ResourceId</span></span>
<span data-ttu-id="5af58-129">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="5af58-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5af58-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5af58-130">-Confirm</span></span>
<span data-ttu-id="5af58-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5af58-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5af58-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5af58-132">-WhatIf</span></span>
<span data-ttu-id="5af58-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5af58-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5af58-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5af58-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5af58-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af58-135">CommonParameters</span></span>
<span data-ttu-id="5af58-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5af58-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af58-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5af58-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af58-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5af58-138">INPUTS</span></span>

### <span data-ttu-id="5af58-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="5af58-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="5af58-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5af58-140">System.String</span></span>

## <span data-ttu-id="5af58-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5af58-141">OUTPUTS</span></span>

### <span data-ttu-id="5af58-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5af58-142">System.Boolean</span></span>

## <span data-ttu-id="5af58-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="5af58-143">NOTES</span></span>

## <span data-ttu-id="5af58-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5af58-144">RELATED LINKS</span></span>
