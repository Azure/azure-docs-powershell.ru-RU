---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416311"
---
# <span data-ttu-id="e455b-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="e455b-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="e455b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e455b-102">SYNOPSIS</span></span>
<span data-ttu-id="e455b-103">Получить решение для безопасности IoT</span><span class="sxs-lookup"><span data-stu-id="e455b-103">Get IoT security solution</span></span>

## <span data-ttu-id="e455b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e455b-104">SYNTAX</span></span>

### <span data-ttu-id="e455b-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e455b-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e455b-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="e455b-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e455b-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="e455b-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e455b-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e455b-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e455b-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e455b-109">DESCRIPTION</span></span>
<span data-ttu-id="e455b-110">Этот Get-AzIotSecuritySolution возвращает одно или несколько решений безопасности iOT.</span><span class="sxs-lookup"><span data-stu-id="e455b-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="e455b-111">Решение для защиты IoT собирает данные безопасности и события с устройств iot и iot-концентратора для предотвращения и обнаружения угроз.</span><span class="sxs-lookup"><span data-stu-id="e455b-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="e455b-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e455b-112">EXAMPLES</span></span>

### <span data-ttu-id="e455b-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e455b-113">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "centraluseuap"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="e455b-114">Получить решение "MySample" в группе ресурсов "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="e455b-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="e455b-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e455b-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="e455b-116">Получить список всех решений безопасности в группе ресурсов "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="e455b-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="e455b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e455b-117">PARAMETERS</span></span>

### <span data-ttu-id="e455b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e455b-118">-DefaultProfile</span></span>
<span data-ttu-id="e455b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e455b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e455b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e455b-120">-Name</span></span>
<span data-ttu-id="e455b-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e455b-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e455b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e455b-122">-ResourceGroupName</span></span>
<span data-ttu-id="e455b-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e455b-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e455b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e455b-124">-ResourceId</span></span>
<span data-ttu-id="e455b-125">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="e455b-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e455b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e455b-126">CommonParameters</span></span>
<span data-ttu-id="e455b-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e455b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e455b-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e455b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e455b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e455b-129">INPUTS</span></span>

### <span data-ttu-id="e455b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e455b-130">System.String</span></span>

## <span data-ttu-id="e455b-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e455b-131">OUTPUTS</span></span>

### <span data-ttu-id="e455b-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="e455b-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="e455b-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e455b-133">NOTES</span></span>

## <span data-ttu-id="e455b-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e455b-134">RELATED LINKS</span></span>
