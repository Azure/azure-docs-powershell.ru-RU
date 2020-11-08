---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247735"
---
# <span data-ttu-id="cbfbe-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="cbfbe-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="cbfbe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cbfbe-102">SYNOPSIS</span></span>
<span data-ttu-id="cbfbe-103">Создание маркера SAS для целевого центра Интернета IoT, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="cbfbe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cbfbe-104">SYNTAX</span></span>

### <span data-ttu-id="cbfbe-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cbfbe-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbfbe-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cbfbe-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbfbe-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cbfbe-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbfbe-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbfbe-108">DESCRIPTION</span></span>
<span data-ttu-id="cbfbe-109">Для маркеров SAS устройства параметр политики используется для доступа только к реестру устройства.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="cbfbe-110">Таким образом, политика должна иметь доступ к реестру для чтения.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="cbfbe-111">Для маркеров центра Интернета вещей политика входит в состав SAS.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="cbfbe-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cbfbe-112">EXAMPLES</span></span>

### <span data-ttu-id="cbfbe-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cbfbe-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="cbfbe-114">Создание маркера SAS центра Интернета вещей с помощью политики iothubowner и первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="cbfbe-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cbfbe-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="cbfbe-116">Создание маркера SAS центра Интернета вещей с помощью политики registryRead и вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="cbfbe-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cbfbe-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="cbfbe-118">Создание маркера SAS устройства с помощью политики iothubowner для доступа к реестру устройства {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="cbfbe-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="cbfbe-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="cbfbe-120">Создание маркера SAS модуля с помощью политики iothubowner для доступа к реестру устройства {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="cbfbe-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cbfbe-121">PARAMETERS</span></span>

### <span data-ttu-id="cbfbe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbfbe-122">-DefaultProfile</span></span>
<span data-ttu-id="cbfbe-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbfbe-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="cbfbe-124">-DeviceId</span></span>
<span data-ttu-id="cbfbe-125">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-125">Target Device Id.</span></span>

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

### <span data-ttu-id="cbfbe-126">-Duration</span><span class="sxs-lookup"><span data-stu-id="cbfbe-126">-Duration</span></span>
<span data-ttu-id="cbfbe-127">Будущая дата окончания срока действия маркера (в секундах).</span><span class="sxs-lookup"><span data-stu-id="cbfbe-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="cbfbe-128">Значение по умолчанию — 3600.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-128">Default is 3600.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbfbe-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbfbe-129">-InputObject</span></span>
<span data-ttu-id="cbfbe-130">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="cbfbe-130">IotHub object</span></span>

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

### <span data-ttu-id="cbfbe-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="cbfbe-131">-IotHubName</span></span>
<span data-ttu-id="cbfbe-132">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="cbfbe-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cbfbe-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="cbfbe-133">-KeyName</span></span>
<span data-ttu-id="cbfbe-134">Имя ключа доступа.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-134">Access key name.</span></span>

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

### <span data-ttu-id="cbfbe-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="cbfbe-135">-KeyType</span></span>
<span data-ttu-id="cbfbe-136">Тип ключа доступа.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-136">Access key type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbfbe-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="cbfbe-137">-ModuleId</span></span>
<span data-ttu-id="cbfbe-138">Идентификатор целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-138">Target Module Id.</span></span>

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

### <span data-ttu-id="cbfbe-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbfbe-139">-ResourceGroupName</span></span>
<span data-ttu-id="cbfbe-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cbfbe-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cbfbe-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbfbe-141">-ResourceId</span></span>
<span data-ttu-id="cbfbe-142">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="cbfbe-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cbfbe-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbfbe-143">-Confirm</span></span>
<span data-ttu-id="cbfbe-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbfbe-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbfbe-145">-WhatIf</span></span>
<span data-ttu-id="cbfbe-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbfbe-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbfbe-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbfbe-148">CommonParameters</span></span>
<span data-ttu-id="cbfbe-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cbfbe-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbfbe-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbfbe-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbfbe-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cbfbe-151">INPUTS</span></span>

### <span data-ttu-id="cbfbe-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cbfbe-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cbfbe-153">System. String</span><span class="sxs-lookup"><span data-stu-id="cbfbe-153">System.String</span></span>

## <span data-ttu-id="cbfbe-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbfbe-154">OUTPUTS</span></span>

### <span data-ttu-id="cbfbe-155">System. String</span><span class="sxs-lookup"><span data-stu-id="cbfbe-155">System.String</span></span>

## <span data-ttu-id="cbfbe-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="cbfbe-156">NOTES</span></span>

## <span data-ttu-id="cbfbe-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbfbe-157">RELATED LINKS</span></span>
