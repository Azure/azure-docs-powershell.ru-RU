---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 39b936f6b9ec4bb133ecc6510963207c5e7d96a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977043"
---
# <span data-ttu-id="fc34d-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="fc34d-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="fc34d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc34d-102">SYNOPSIS</span></span>
<span data-ttu-id="fc34d-103">Создание маркера SAS для целевого концентратора IoT, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="fc34d-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="fc34d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fc34d-104">SYNTAX</span></span>

### <span data-ttu-id="fc34d-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc34d-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc34d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fc34d-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc34d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fc34d-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc34d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc34d-108">DESCRIPTION</span></span>
<span data-ttu-id="fc34d-109">Для токенов SAS устройств параметр политики используется только для доступа к реестру устройств.</span><span class="sxs-lookup"><span data-stu-id="fc34d-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="fc34d-110">Поэтому политика должна иметь доступ с чтением к реестру.</span><span class="sxs-lookup"><span data-stu-id="fc34d-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="fc34d-111">Для токенов IoT Hub политика является частью SAS.</span><span class="sxs-lookup"><span data-stu-id="fc34d-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="fc34d-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fc34d-112">EXAMPLES</span></span>

### <span data-ttu-id="fc34d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc34d-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="fc34d-114">Создание токена SAS концентратора IoT с помощью политики iothubowner и первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="fc34d-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="fc34d-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fc34d-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="fc34d-116">Создание маркера SAS концентратора IoT с помощью политики registryRead и дополнительного ключа.</span><span class="sxs-lookup"><span data-stu-id="fc34d-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="fc34d-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="fc34d-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="fc34d-118">Создание маркера SAS устройства с помощью политики iothubowner для доступа к реестру устройств {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="fc34d-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="fc34d-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="fc34d-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="fc34d-120">Создание маркера SAS модуля с помощью политики iothubowner для доступа к реестру устройств {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="fc34d-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="fc34d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc34d-121">PARAMETERS</span></span>

### <span data-ttu-id="fc34d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc34d-122">-DefaultProfile</span></span>
<span data-ttu-id="fc34d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc34d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc34d-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fc34d-124">-DeviceId</span></span>
<span data-ttu-id="fc34d-125">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="fc34d-125">Target Device Id.</span></span>

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

### <span data-ttu-id="fc34d-126">-Duration</span><span class="sxs-lookup"><span data-stu-id="fc34d-126">-Duration</span></span>
<span data-ttu-id="fc34d-127">Срок действия маркера, который будет сгенерирован в будущем (в секундах).</span><span class="sxs-lookup"><span data-stu-id="fc34d-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="fc34d-128">Значение по умолчанию — 3600.</span><span class="sxs-lookup"><span data-stu-id="fc34d-128">Default is 3600.</span></span>

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

### <span data-ttu-id="fc34d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc34d-129">-InputObject</span></span>
<span data-ttu-id="fc34d-130">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="fc34d-130">IotHub object</span></span>

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

### <span data-ttu-id="fc34d-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fc34d-131">-IotHubName</span></span>
<span data-ttu-id="fc34d-132">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="fc34d-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fc34d-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fc34d-133">-KeyName</span></span>
<span data-ttu-id="fc34d-134">Имя ключа Access.</span><span class="sxs-lookup"><span data-stu-id="fc34d-134">Access key name.</span></span>

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

### <span data-ttu-id="fc34d-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="fc34d-135">-KeyType</span></span>
<span data-ttu-id="fc34d-136">Тип клавиши Access.</span><span class="sxs-lookup"><span data-stu-id="fc34d-136">Access key type.</span></span>

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

### <span data-ttu-id="fc34d-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="fc34d-137">-ModuleId</span></span>
<span data-ttu-id="fc34d-138">ИД целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="fc34d-138">Target Module Id.</span></span>

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

### <span data-ttu-id="fc34d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc34d-139">-ResourceGroupName</span></span>
<span data-ttu-id="fc34d-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fc34d-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fc34d-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc34d-141">-ResourceId</span></span>
<span data-ttu-id="fc34d-142">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="fc34d-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fc34d-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc34d-143">-Confirm</span></span>
<span data-ttu-id="fc34d-144">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fc34d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc34d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc34d-145">-WhatIf</span></span>
<span data-ttu-id="fc34d-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc34d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc34d-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fc34d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc34d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc34d-148">CommonParameters</span></span>
<span data-ttu-id="fc34d-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc34d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc34d-150">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc34d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc34d-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc34d-151">INPUTS</span></span>

### <span data-ttu-id="fc34d-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fc34d-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fc34d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="fc34d-153">System.String</span></span>

## <span data-ttu-id="fc34d-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fc34d-154">OUTPUTS</span></span>

### <span data-ttu-id="fc34d-155">System.String</span><span class="sxs-lookup"><span data-stu-id="fc34d-155">System.String</span></span>

## <span data-ttu-id="fc34d-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fc34d-156">NOTES</span></span>

## <span data-ttu-id="fc34d-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc34d-157">RELATED LINKS</span></span>
