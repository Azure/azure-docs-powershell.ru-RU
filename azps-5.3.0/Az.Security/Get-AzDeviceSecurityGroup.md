---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 3d43407c9f7e58d7a5d29ef56412f6d38c5c957b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517778"
---
# <span data-ttu-id="2365a-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2365a-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="2365a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2365a-102">SYNOPSIS</span></span>
<span data-ttu-id="2365a-103">Получить группу безопасности устройств (безопасность IoT Hub)</span><span class="sxs-lookup"><span data-stu-id="2365a-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="2365a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2365a-104">SYNTAX</span></span>

### <span data-ttu-id="2365a-105">ResourceIdScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2365a-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2365a-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="2365a-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2365a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2365a-107">DESCRIPTION</span></span>
<span data-ttu-id="2365a-108">Этот Get-AzDeviceSecurityGroup возвращает группу безопасности устройств, определенное в решении для защиты iot.</span><span class="sxs-lookup"><span data-stu-id="2365a-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="2365a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2365a-109">EXAMPLES</span></span>

### <span data-ttu-id="2365a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2365a-110">Example 1</span></span>
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

<span data-ttu-id="2365a-111">Получить группу безопасности устройств "MySecurityGroup" в центре IoT с reasource Id "/subscriptions/XXXXXXXX-XXXXX-XXXXX-XXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="2365a-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="2365a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2365a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="2365a-113">Получить список группы безопасности устройств в центре IoT с новым идом "/subscriptions/XXXXXXXX-XXXXX-XXXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="2365a-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="2365a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2365a-114">PARAMETERS</span></span>

### <span data-ttu-id="2365a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2365a-115">-DefaultProfile</span></span>
<span data-ttu-id="2365a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2365a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2365a-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="2365a-117">-HubResourceId</span></span>
<span data-ttu-id="2365a-118">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="2365a-118">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2365a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2365a-119">-Name</span></span>
<span data-ttu-id="2365a-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2365a-120">Resource name.</span></span>

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

### <span data-ttu-id="2365a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2365a-121">CommonParameters</span></span>
<span data-ttu-id="2365a-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2365a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2365a-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2365a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2365a-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2365a-124">INPUTS</span></span>

### <span data-ttu-id="2365a-125">Нет</span><span class="sxs-lookup"><span data-stu-id="2365a-125">None</span></span>

## <span data-ttu-id="2365a-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2365a-126">OUTPUTS</span></span>

### <span data-ttu-id="2365a-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2365a-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="2365a-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2365a-128">NOTES</span></span>

## <span data-ttu-id="2365a-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2365a-129">RELATED LINKS</span></span>
