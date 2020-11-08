---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078248"
---
# <span data-ttu-id="3c67f-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="3c67f-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="3c67f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c67f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c67f-103">Создание маркера SAS для целевого центра Интернета IoT, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="3c67f-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="3c67f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c67f-104">SYNTAX</span></span>

### <span data-ttu-id="3c67f-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c67f-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c67f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3c67f-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c67f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3c67f-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c67f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c67f-108">DESCRIPTION</span></span>
<span data-ttu-id="3c67f-109">Для маркеров SAS устройства параметр политики используется для доступа только к реестру устройства.</span><span class="sxs-lookup"><span data-stu-id="3c67f-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="3c67f-110">Таким образом, политика должна иметь доступ к реестру для чтения.</span><span class="sxs-lookup"><span data-stu-id="3c67f-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="3c67f-111">Для маркеров центра Интернета вещей политика входит в состав SAS.</span><span class="sxs-lookup"><span data-stu-id="3c67f-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="3c67f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c67f-112">EXAMPLES</span></span>

### <span data-ttu-id="3c67f-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3c67f-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="3c67f-114">Создание маркера SAS центра Интернета вещей с помощью политики iothubowner и первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="3c67f-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="3c67f-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3c67f-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="3c67f-116">Создание маркера SAS центра Интернета вещей с помощью политики registryRead и вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="3c67f-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="3c67f-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3c67f-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="3c67f-118">Создание маркера SAS устройства с помощью политики iothubowner для доступа к реестру устройства {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="3c67f-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="3c67f-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="3c67f-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="3c67f-120">Создание маркера SAS модуля с помощью политики iothubowner для доступа к реестру устройства {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="3c67f-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="3c67f-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c67f-121">PARAMETERS</span></span>

### <span data-ttu-id="3c67f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c67f-122">-DefaultProfile</span></span>
<span data-ttu-id="3c67f-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c67f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c67f-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="3c67f-124">-DeviceId</span></span>
<span data-ttu-id="3c67f-125">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="3c67f-125">Target Device Id.</span></span>

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

### <span data-ttu-id="3c67f-126">-Duration</span><span class="sxs-lookup"><span data-stu-id="3c67f-126">-Duration</span></span>
<span data-ttu-id="3c67f-127">Будущая дата окончания срока действия маркера (в секундах).</span><span class="sxs-lookup"><span data-stu-id="3c67f-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="3c67f-128">Значение по умолчанию — 3600.</span><span class="sxs-lookup"><span data-stu-id="3c67f-128">Default is 3600.</span></span>

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

### <span data-ttu-id="3c67f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c67f-129">-InputObject</span></span>
<span data-ttu-id="3c67f-130">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="3c67f-130">IotHub object</span></span>

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

### <span data-ttu-id="3c67f-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3c67f-131">-IotHubName</span></span>
<span data-ttu-id="3c67f-132">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="3c67f-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3c67f-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3c67f-133">-KeyName</span></span>
<span data-ttu-id="3c67f-134">Имя ключа доступа.</span><span class="sxs-lookup"><span data-stu-id="3c67f-134">Access key name.</span></span>

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

### <span data-ttu-id="3c67f-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3c67f-135">-KeyType</span></span>
<span data-ttu-id="3c67f-136">Тип ключа доступа.</span><span class="sxs-lookup"><span data-stu-id="3c67f-136">Access key type.</span></span>

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

### <span data-ttu-id="3c67f-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="3c67f-137">-ModuleId</span></span>
<span data-ttu-id="3c67f-138">Идентификатор целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="3c67f-138">Target Module Id.</span></span>

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

### <span data-ttu-id="3c67f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c67f-139">-ResourceGroupName</span></span>
<span data-ttu-id="3c67f-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3c67f-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3c67f-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c67f-141">-ResourceId</span></span>
<span data-ttu-id="3c67f-142">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="3c67f-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3c67f-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c67f-143">-Confirm</span></span>
<span data-ttu-id="3c67f-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c67f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c67f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c67f-145">-WhatIf</span></span>
<span data-ttu-id="3c67f-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c67f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c67f-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c67f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c67f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c67f-148">CommonParameters</span></span>
<span data-ttu-id="3c67f-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c67f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c67f-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c67f-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c67f-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c67f-151">INPUTS</span></span>

### <span data-ttu-id="3c67f-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3c67f-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3c67f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="3c67f-153">System.String</span></span>

## <span data-ttu-id="3c67f-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c67f-154">OUTPUTS</span></span>

### <span data-ttu-id="3c67f-155">System. String</span><span class="sxs-lookup"><span data-stu-id="3c67f-155">System.String</span></span>

## <span data-ttu-id="3c67f-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c67f-156">NOTES</span></span>

## <span data-ttu-id="3c67f-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c67f-157">RELATED LINKS</span></span>
