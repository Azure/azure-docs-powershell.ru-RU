---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 09a4201d8add325c068358615a48a86c5e60911a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997825"
---
# <span data-ttu-id="da3df-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="da3df-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="da3df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da3df-102">SYNOPSIS</span></span>
<span data-ttu-id="da3df-103">Создайте модуль на целевом устройстве ioT в концентраторе IoT.</span><span class="sxs-lookup"><span data-stu-id="da3df-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="da3df-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da3df-104">SYNTAX</span></span>

### <span data-ttu-id="da3df-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da3df-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da3df-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="da3df-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da3df-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="da3df-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da3df-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da3df-108">DESCRIPTION</span></span>
<span data-ttu-id="da3df-109">Создайте модуль на целевом устройстве ioT с другим типом авторизации в центре IoT.</span><span class="sxs-lookup"><span data-stu-id="da3df-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="da3df-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da3df-110">EXAMPLES</span></span>

### <span data-ttu-id="da3df-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="da3df-111">Example 1</span></span>
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

<span data-ttu-id="da3df-112">Создайте модуль на целевом устройстве IoT с авторизацией по умолчанию (общий закрытый ключ).</span><span class="sxs-lookup"><span data-stu-id="da3df-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="da3df-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da3df-113">PARAMETERS</span></span>

### <span data-ttu-id="da3df-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="da3df-114">-AuthMethod</span></span>
<span data-ttu-id="da3df-115">Тип авторизации для создания сущности.</span><span class="sxs-lookup"><span data-stu-id="da3df-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="da3df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da3df-116">-DefaultProfile</span></span>
<span data-ttu-id="da3df-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da3df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da3df-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="da3df-118">-DeviceId</span></span>
<span data-ttu-id="da3df-119">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="da3df-119">Target Device Id.</span></span>

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

### <span data-ttu-id="da3df-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da3df-120">-InputObject</span></span>
<span data-ttu-id="da3df-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="da3df-121">IotHub object</span></span>

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

### <span data-ttu-id="da3df-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="da3df-122">-IotHubName</span></span>
<span data-ttu-id="da3df-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="da3df-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="da3df-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="da3df-124">-ModuleId</span></span>
<span data-ttu-id="da3df-125">ИД целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="da3df-125">Target Module Id.</span></span>

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

### <span data-ttu-id="da3df-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="da3df-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="da3df-127">Явный самозаверяный эскиз сертификата, который нужно использовать в качестве первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="da3df-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="da3df-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da3df-128">-ResourceGroupName</span></span>
<span data-ttu-id="da3df-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="da3df-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="da3df-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da3df-130">-ResourceId</span></span>
<span data-ttu-id="da3df-131">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="da3df-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="da3df-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="da3df-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="da3df-133">Явный самозаверяный эскиз сертификата, который нужно использовать для дополнительного ключа.</span><span class="sxs-lookup"><span data-stu-id="da3df-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="da3df-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da3df-134">-Confirm</span></span>
<span data-ttu-id="da3df-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da3df-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da3df-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da3df-136">-WhatIf</span></span>
<span data-ttu-id="da3df-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da3df-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da3df-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="da3df-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da3df-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da3df-139">CommonParameters</span></span>
<span data-ttu-id="da3df-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da3df-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da3df-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da3df-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da3df-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da3df-142">INPUTS</span></span>

### <span data-ttu-id="da3df-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="da3df-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="da3df-144">System.String</span><span class="sxs-lookup"><span data-stu-id="da3df-144">System.String</span></span>

## <span data-ttu-id="da3df-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da3df-145">OUTPUTS</span></span>

### <span data-ttu-id="da3df-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="da3df-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="da3df-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da3df-147">NOTES</span></span>

## <span data-ttu-id="da3df-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da3df-148">RELATED LINKS</span></span>