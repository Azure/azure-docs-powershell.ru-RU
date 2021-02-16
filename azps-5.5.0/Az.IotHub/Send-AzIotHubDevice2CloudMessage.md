---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226481"
---
# <span data-ttu-id="4604c-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="4604c-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="4604c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4604c-102">SYNOPSIS</span></span>
<span data-ttu-id="4604c-103">Отправка сообщения об устройстве в облако.</span><span class="sxs-lookup"><span data-stu-id="4604c-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="4604c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4604c-104">SYNTAX</span></span>

### <span data-ttu-id="4604c-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4604c-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4604c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4604c-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4604c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4604c-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4604c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4604c-108">DESCRIPTION</span></span>
<span data-ttu-id="4604c-109">Эта команда поддерживает отправку сообщений со свойствами приложения и системы.</span><span class="sxs-lookup"><span data-stu-id="4604c-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="4604c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4604c-110">EXAMPLES</span></span>

### <span data-ttu-id="4604c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4604c-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="4604c-112">Отправка устройства в облачное сообщение с использованием типа транспорта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4604c-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="4604c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4604c-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="4604c-114">Отправка MQTT-устройства в облачное сообщение.</span><span class="sxs-lookup"><span data-stu-id="4604c-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="4604c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4604c-115">PARAMETERS</span></span>

### <span data-ttu-id="4604c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4604c-116">-DefaultProfile</span></span>
<span data-ttu-id="4604c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4604c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4604c-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4604c-118">-DeviceId</span></span>
<span data-ttu-id="4604c-119">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="4604c-119">Target Device Id.</span></span>

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

### <span data-ttu-id="4604c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4604c-120">-InputObject</span></span>
<span data-ttu-id="4604c-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="4604c-121">IotHub object</span></span>

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

### <span data-ttu-id="4604c-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4604c-122">-IotHubName</span></span>
<span data-ttu-id="4604c-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="4604c-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4604c-124">-Message</span><span class="sxs-lookup"><span data-stu-id="4604c-124">-Message</span></span>
<span data-ttu-id="4604c-125">Текст сообщения для отправки в Центр IoT.</span><span class="sxs-lookup"><span data-stu-id="4604c-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="4604c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4604c-126">-PassThru</span></span>
<span data-ttu-id="4604c-127">Возвращает объект boolean.</span><span class="sxs-lookup"><span data-stu-id="4604c-127">Allows to return the boolean object.</span></span> <span data-ttu-id="4604c-128">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4604c-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4604c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4604c-129">-ResourceGroupName</span></span>
<span data-ttu-id="4604c-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4604c-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4604c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4604c-131">-ResourceId</span></span>
<span data-ttu-id="4604c-132">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="4604c-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4604c-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="4604c-133">-TransportType</span></span>
<span data-ttu-id="4604c-134">Тип используемого транспорта.</span><span class="sxs-lookup"><span data-stu-id="4604c-134">Transport type to use.</span></span>
<span data-ttu-id="4604c-135">Значение по умолчанию — Amqp.</span><span class="sxs-lookup"><span data-stu-id="4604c-135">Default is Amqp.</span></span>

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

### <span data-ttu-id="4604c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4604c-136">-Confirm</span></span>
<span data-ttu-id="4604c-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4604c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4604c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4604c-138">-WhatIf</span></span>
<span data-ttu-id="4604c-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4604c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4604c-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4604c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4604c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4604c-141">CommonParameters</span></span>
<span data-ttu-id="4604c-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4604c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4604c-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4604c-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4604c-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4604c-144">INPUTS</span></span>

### <span data-ttu-id="4604c-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4604c-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4604c-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4604c-146">System.String</span></span>

## <span data-ttu-id="4604c-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4604c-147">OUTPUTS</span></span>

### <span data-ttu-id="4604c-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4604c-148">System.Boolean</span></span>

## <span data-ttu-id="4604c-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4604c-149">NOTES</span></span>

## <span data-ttu-id="4604c-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4604c-150">RELATED LINKS</span></span>
