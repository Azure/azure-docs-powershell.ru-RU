---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 3d43407c9f7e58d7a5d29ef56412f6d38c5c957b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243328"
---
# <span data-ttu-id="6c06f-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6c06f-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="6c06f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c06f-102">SYNOPSIS</span></span>
<span data-ttu-id="6c06f-103">Получение группы безопасности устройства (безопасность в центре IoT)</span><span class="sxs-lookup"><span data-stu-id="6c06f-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="6c06f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c06f-104">SYNTAX</span></span>

### <span data-ttu-id="6c06f-105">ResourceIdScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c06f-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c06f-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="6c06f-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c06f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c06f-107">DESCRIPTION</span></span>
<span data-ttu-id="6c06f-108">Командлет Get-AzDeviceSecurityGroup возвращает группу безопасности устройства, определенную в решении системы безопасности IOT</span><span class="sxs-lookup"><span data-stu-id="6c06f-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="6c06f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c06f-109">EXAMPLES</span></span>

### <span data-ttu-id="6c06f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6c06f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" -Name "MySecurityGroup" 

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }
            {
              RuleType: "AmqpC2DMessagesNotInAllowedRange"
              DisplayName: "Number of cloud to device messages (AMQP protocol) is not in allowed range"
              Description: "Get an alert when the number of cloud to device messages (AMQP protocol) in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="6c06f-111">Получение группы безопасности устройства "MySecurityGroup" в центре IoT с reasource ID "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="6c06f-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="6c06f-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6c06f-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="6c06f-113">Получение списка группы безопасности устройства в центре IoT с reasource ID "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="6c06f-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="6c06f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c06f-114">PARAMETERS</span></span>

### <span data-ttu-id="6c06f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c06f-115">-DefaultProfile</span></span>
<span data-ttu-id="6c06f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c06f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c06f-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="6c06f-117">-HubResourceId</span></span>
<span data-ttu-id="6c06f-118">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="6c06f-118">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="6c06f-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6c06f-119">-Name</span></span>
<span data-ttu-id="6c06f-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="6c06f-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c06f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c06f-121">CommonParameters</span></span>
<span data-ttu-id="6c06f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c06f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c06f-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c06f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c06f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c06f-124">INPUTS</span></span>

### <span data-ttu-id="6c06f-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="6c06f-125">None</span></span>

## <span data-ttu-id="6c06f-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c06f-126">OUTPUTS</span></span>

### <span data-ttu-id="6c06f-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6c06f-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="6c06f-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c06f-128">NOTES</span></span>

## <span data-ttu-id="6c06f-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c06f-129">RELATED LINKS</span></span>
