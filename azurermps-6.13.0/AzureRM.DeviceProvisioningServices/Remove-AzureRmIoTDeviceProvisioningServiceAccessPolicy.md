---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: b3a813623ed11a64a23dc35afe2f81c3f5de61da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566469"
---
# <span data-ttu-id="06a77-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="06a77-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="06a77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06a77-102">SYNOPSIS</span></span>
<span data-ttu-id="06a77-103">Удалите политики общего доступа в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="06a77-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06a77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06a77-104">SYNTAX</span></span>

### <span data-ttu-id="06a77-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="06a77-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06a77-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="06a77-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06a77-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="06a77-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06a77-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06a77-108">DESCRIPTION</span></span>
<span data-ttu-id="06a77-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="06a77-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="06a77-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06a77-110">EXAMPLES</span></span>

### <span data-ttu-id="06a77-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="06a77-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="06a77-112">Удаление политики общего доступа "mypolicy" в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="06a77-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="06a77-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="06a77-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzureRmIoTDpsAccessPolicy
```

<span data-ttu-id="06a77-114">Удаление политики общего доступа "mypolicy" в службе подготовки устройств центра для Azure IoT с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="06a77-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="06a77-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06a77-115">PARAMETERS</span></span>

### <span data-ttu-id="06a77-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a77-116">-DefaultProfile</span></span>
<span data-ttu-id="06a77-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06a77-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a77-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06a77-118">-InputObject</span></span>
<span data-ttu-id="06a77-119">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="06a77-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="06a77-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="06a77-120">-KeyName</span></span>
<span data-ttu-id="06a77-121">Имя ключа политики доступа к службе для подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="06a77-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="06a77-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="06a77-122">-Name</span></span>
<span data-ttu-id="06a77-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="06a77-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="06a77-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06a77-124">-PassThru</span></span>
<span data-ttu-id="06a77-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="06a77-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="06a77-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a77-126">-ResourceGroupName</span></span>
<span data-ttu-id="06a77-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="06a77-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="06a77-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06a77-128">-ResourceId</span></span>
<span data-ttu-id="06a77-129">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="06a77-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="06a77-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06a77-130">-Confirm</span></span>
<span data-ttu-id="06a77-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="06a77-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06a77-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06a77-132">-WhatIf</span></span>
<span data-ttu-id="06a77-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="06a77-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06a77-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="06a77-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06a77-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a77-135">CommonParameters</span></span>
<span data-ttu-id="06a77-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06a77-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a77-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06a77-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a77-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06a77-138">INPUTS</span></span>

### <span data-ttu-id="06a77-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="06a77-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="06a77-140">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="06a77-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="06a77-141">System. String</span><span class="sxs-lookup"><span data-stu-id="06a77-141">System.String</span></span>

## <span data-ttu-id="06a77-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06a77-142">OUTPUTS</span></span>

### <span data-ttu-id="06a77-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06a77-143">System.Boolean</span></span>

## <span data-ttu-id="06a77-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="06a77-144">NOTES</span></span>

## <span data-ttu-id="06a77-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06a77-145">RELATED LINKS</span></span>
