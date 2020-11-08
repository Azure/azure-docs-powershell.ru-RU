---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 44e6451542a75e97a57890261a9a5f312e5ec466
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247775"
---
# <span data-ttu-id="6aab3-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="6aab3-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="6aab3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6aab3-102">SYNOPSIS</span></span>
<span data-ttu-id="6aab3-103">Создание модуля на целевом устройстве IoT в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="6aab3-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="6aab3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6aab3-104">SYNTAX</span></span>

### <span data-ttu-id="6aab3-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6aab3-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6aab3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6aab3-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6aab3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6aab3-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6aab3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6aab3-108">DESCRIPTION</span></span>
<span data-ttu-id="6aab3-109">Создание модуля на целевом устройстве IoT с различными типами авторизации в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="6aab3-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="6aab3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6aab3-110">EXAMPLES</span></span>

### <span data-ttu-id="6aab3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6aab3-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod shared_private_key

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  : 
```

<span data-ttu-id="6aab3-112">Создание модуля на целевом устройстве IoT для проверки подлинности по умолчанию (общего закрытого ключа).</span><span class="sxs-lookup"><span data-stu-id="6aab3-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="6aab3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6aab3-113">PARAMETERS</span></span>

### <span data-ttu-id="6aab3-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="6aab3-114">-AuthMethod</span></span>
<span data-ttu-id="6aab3-115">Тип авторизации, с которым будет создана сущность.</span><span class="sxs-lookup"><span data-stu-id="6aab3-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="6aab3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aab3-116">-DefaultProfile</span></span>
<span data-ttu-id="6aab3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6aab3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aab3-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6aab3-118">-DeviceId</span></span>
<span data-ttu-id="6aab3-119">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="6aab3-119">Target Device Id.</span></span>

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

### <span data-ttu-id="6aab3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6aab3-120">-InputObject</span></span>
<span data-ttu-id="6aab3-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="6aab3-121">IotHub object</span></span>

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

### <span data-ttu-id="6aab3-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6aab3-122">-IotHubName</span></span>
<span data-ttu-id="6aab3-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="6aab3-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6aab3-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="6aab3-124">-ModuleId</span></span>
<span data-ttu-id="6aab3-125">Идентификатор целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="6aab3-125">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aab3-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="6aab3-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="6aab3-127">Явный заверенный отпечаток сертификата для использования в качестве первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="6aab3-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="6aab3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aab3-128">-ResourceGroupName</span></span>
<span data-ttu-id="6aab3-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6aab3-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6aab3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6aab3-130">-ResourceId</span></span>
<span data-ttu-id="6aab3-131">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="6aab3-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6aab3-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="6aab3-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="6aab3-133">Явный заверенный отпечаток сертификата, который будет использоваться для вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="6aab3-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aab3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6aab3-134">-Confirm</span></span>
<span data-ttu-id="6aab3-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6aab3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aab3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aab3-136">-WhatIf</span></span>
<span data-ttu-id="6aab3-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6aab3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aab3-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6aab3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aab3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aab3-139">CommonParameters</span></span>
<span data-ttu-id="6aab3-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6aab3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aab3-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aab3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aab3-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6aab3-142">INPUTS</span></span>

### <span data-ttu-id="6aab3-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6aab3-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6aab3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6aab3-144">System.String</span></span>

## <span data-ttu-id="6aab3-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6aab3-145">OUTPUTS</span></span>

### <span data-ttu-id="6aab3-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSModule</span><span class="sxs-lookup"><span data-stu-id="6aab3-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="6aab3-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="6aab3-147">NOTES</span></span>

## <span data-ttu-id="6aab3-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6aab3-148">RELATED LINKS</span></span>