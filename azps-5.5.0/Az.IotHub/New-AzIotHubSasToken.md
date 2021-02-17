---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234164"
---
# <span data-ttu-id="272a7-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="272a7-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="272a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="272a7-102">SYNOPSIS</span></span>
<span data-ttu-id="272a7-103">Создание маркера SAS для целевого концентратора IoT, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="272a7-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="272a7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="272a7-104">SYNTAX</span></span>

### <span data-ttu-id="272a7-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="272a7-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="272a7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="272a7-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="272a7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="272a7-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="272a7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="272a7-108">DESCRIPTION</span></span>
<span data-ttu-id="272a7-109">Для токенов SAS устройств параметр политики используется только для доступа к реестру устройств.</span><span class="sxs-lookup"><span data-stu-id="272a7-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="272a7-110">Поэтому политика должна иметь доступ с чтением к реестру.</span><span class="sxs-lookup"><span data-stu-id="272a7-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="272a7-111">Для токенов IoT Hub политика является частью SAS.</span><span class="sxs-lookup"><span data-stu-id="272a7-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="272a7-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="272a7-112">EXAMPLES</span></span>

### <span data-ttu-id="272a7-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="272a7-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="272a7-114">Создание маркера SAS концентратора IoT с помощью политики iothubowner и первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="272a7-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="272a7-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="272a7-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="272a7-116">Создание маркера SAS концентратора IoT с помощью политики registryRead и дополнительного ключа.</span><span class="sxs-lookup"><span data-stu-id="272a7-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="272a7-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="272a7-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="272a7-118">Создание маркера SAS устройства с помощью политики iothubowner для доступа к реестру устройств {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="272a7-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="272a7-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="272a7-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="272a7-120">Создание маркера SAS модуля с помощью политики iothubowner для доступа к реестру устройств {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="272a7-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="272a7-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="272a7-121">PARAMETERS</span></span>

### <span data-ttu-id="272a7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272a7-122">-DefaultProfile</span></span>
<span data-ttu-id="272a7-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="272a7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="272a7-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="272a7-124">-DeviceId</span></span>
<span data-ttu-id="272a7-125">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="272a7-125">Target Device Id.</span></span>

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

### <span data-ttu-id="272a7-126">-Duration</span><span class="sxs-lookup"><span data-stu-id="272a7-126">-Duration</span></span>
<span data-ttu-id="272a7-127">Срок действия маркера, который будет сгенерирован в будущем (в секундах).</span><span class="sxs-lookup"><span data-stu-id="272a7-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="272a7-128">Значение по умолчанию — 3600.</span><span class="sxs-lookup"><span data-stu-id="272a7-128">Default is 3600.</span></span>

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

### <span data-ttu-id="272a7-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="272a7-129">-InputObject</span></span>
<span data-ttu-id="272a7-130">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="272a7-130">IotHub object</span></span>

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

### <span data-ttu-id="272a7-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="272a7-131">-IotHubName</span></span>
<span data-ttu-id="272a7-132">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="272a7-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="272a7-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="272a7-133">-KeyName</span></span>
<span data-ttu-id="272a7-134">Имя ключа Access.</span><span class="sxs-lookup"><span data-stu-id="272a7-134">Access key name.</span></span>

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

### <span data-ttu-id="272a7-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="272a7-135">-KeyType</span></span>
<span data-ttu-id="272a7-136">Тип клавиши Access.</span><span class="sxs-lookup"><span data-stu-id="272a7-136">Access key type.</span></span>

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

### <span data-ttu-id="272a7-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="272a7-137">-ModuleId</span></span>
<span data-ttu-id="272a7-138">ИД целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="272a7-138">Target Module Id.</span></span>

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

### <span data-ttu-id="272a7-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="272a7-139">-ResourceGroupName</span></span>
<span data-ttu-id="272a7-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="272a7-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="272a7-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="272a7-141">-ResourceId</span></span>
<span data-ttu-id="272a7-142">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="272a7-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="272a7-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="272a7-143">-Confirm</span></span>
<span data-ttu-id="272a7-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="272a7-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="272a7-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="272a7-145">-WhatIf</span></span>
<span data-ttu-id="272a7-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="272a7-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="272a7-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="272a7-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="272a7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272a7-148">CommonParameters</span></span>
<span data-ttu-id="272a7-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="272a7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272a7-150">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="272a7-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272a7-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="272a7-151">INPUTS</span></span>

### <span data-ttu-id="272a7-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="272a7-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="272a7-153">System.String</span><span class="sxs-lookup"><span data-stu-id="272a7-153">System.String</span></span>

## <span data-ttu-id="272a7-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="272a7-154">OUTPUTS</span></span>

### <span data-ttu-id="272a7-155">System.String</span><span class="sxs-lookup"><span data-stu-id="272a7-155">System.String</span></span>

## <span data-ttu-id="272a7-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="272a7-156">NOTES</span></span>

## <span data-ttu-id="272a7-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="272a7-157">RELATED LINKS</span></span>
