---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236372"
---
# <span data-ttu-id="8b449-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="8b449-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="8b449-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b449-102">SYNOPSIS</span></span>
<span data-ttu-id="8b449-103">Отправка сообщения от устройства к облаку.</span><span class="sxs-lookup"><span data-stu-id="8b449-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="8b449-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b449-104">SYNTAX</span></span>

### <span data-ttu-id="8b449-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b449-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b449-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8b449-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b449-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8b449-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b449-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b449-108">DESCRIPTION</span></span>
<span data-ttu-id="8b449-109">Эта команда поддерживает отправку сообщений с помощью свойств приложения и системы.</span><span class="sxs-lookup"><span data-stu-id="8b449-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="8b449-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b449-110">EXAMPLES</span></span>

### <span data-ttu-id="8b449-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b449-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="8b449-112">Отправка устройства в облачное сообщение с использованием типа транспорта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8b449-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="8b449-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8b449-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="8b449-114">Отправка mqttного устройства в облачное сообщение.</span><span class="sxs-lookup"><span data-stu-id="8b449-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="8b449-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b449-115">PARAMETERS</span></span>

### <span data-ttu-id="8b449-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b449-116">-DefaultProfile</span></span>
<span data-ttu-id="8b449-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b449-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b449-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8b449-118">-DeviceId</span></span>
<span data-ttu-id="8b449-119">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="8b449-119">Target Device Id.</span></span>

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

### <span data-ttu-id="8b449-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b449-120">-InputObject</span></span>
<span data-ttu-id="8b449-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="8b449-121">IotHub object</span></span>

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

### <span data-ttu-id="8b449-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8b449-122">-IotHubName</span></span>
<span data-ttu-id="8b449-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="8b449-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8b449-124">-Сообщение</span><span class="sxs-lookup"><span data-stu-id="8b449-124">-Message</span></span>
<span data-ttu-id="8b449-125">Текст сообщения для отправки в центр Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="8b449-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="8b449-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b449-126">-PassThru</span></span>
<span data-ttu-id="8b449-127">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="8b449-127">Allows to return the boolean object.</span></span> <span data-ttu-id="8b449-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8b449-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8b449-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b449-129">-ResourceGroupName</span></span>
<span data-ttu-id="8b449-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8b449-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8b449-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b449-131">-ResourceId</span></span>
<span data-ttu-id="8b449-132">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="8b449-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8b449-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="8b449-133">-TransportType</span></span>
<span data-ttu-id="8b449-134">Тип транспорта, который нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="8b449-134">Transport type to use.</span></span>
<span data-ttu-id="8b449-135">По умолчанию используется AMQP.</span><span class="sxs-lookup"><span data-stu-id="8b449-135">Default is Amqp.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSTransportType
Parameter Sets: (All)
Aliases:
Accepted values: Amqp, Http1, Amqp_WebSocket_Only, Amqp_Tcp_Only, Mqtt, Mqtt_WebSocket_Only, Mqtt_Tcp_Only

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b449-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b449-136">-Confirm</span></span>
<span data-ttu-id="8b449-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b449-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b449-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b449-138">-WhatIf</span></span>
<span data-ttu-id="8b449-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b449-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b449-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b449-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b449-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b449-141">CommonParameters</span></span>
<span data-ttu-id="8b449-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b449-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b449-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b449-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b449-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b449-144">INPUTS</span></span>

### <span data-ttu-id="8b449-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8b449-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8b449-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8b449-146">System.String</span></span>

## <span data-ttu-id="8b449-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b449-147">OUTPUTS</span></span>

### <span data-ttu-id="8b449-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b449-148">System.Boolean</span></span>

## <span data-ttu-id="8b449-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b449-149">NOTES</span></span>

## <span data-ttu-id="8b449-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b449-150">RELATED LINKS</span></span>
