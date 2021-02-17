---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: ef984a1cbb1cf922ddc931a7924a5d39ba6c6a0b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232801"
---
# <span data-ttu-id="5900c-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="5900c-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="5900c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5900c-102">SYNOPSIS</span></span>
<span data-ttu-id="5900c-103">Получает список топорологий системы безопасности для подписки</span><span class="sxs-lookup"><span data-stu-id="5900c-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="5900c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5900c-104">SYNTAX</span></span>

### <span data-ttu-id="5900c-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5900c-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5900c-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="5900c-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5900c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5900c-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5900c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5900c-108">DESCRIPTION</span></span>
<span data-ttu-id="5900c-109">Центр безопасности Azure автоматически обнаруживает topologies системы безопасности. Используйте этот cmdlet для просмотра опечаток безопасности.</span><span class="sxs-lookup"><span data-stu-id="5900c-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="5900c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5900c-110">EXAMPLES</span></span>

### <span data-ttu-id="5900c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5900c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="5900c-112">Просмотр всех топорологий безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="5900c-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="5900c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5900c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="5900c-114">Получите конкретные опологи для системы безопасности</span><span class="sxs-lookup"><span data-stu-id="5900c-114">Get a specific security topologies</span></span>

## <span data-ttu-id="5900c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5900c-115">PARAMETERS</span></span>

### <span data-ttu-id="5900c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5900c-116">-DefaultProfile</span></span>
<span data-ttu-id="5900c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5900c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5900c-118">-Location</span><span class="sxs-lookup"><span data-stu-id="5900c-118">-Location</span></span>
<span data-ttu-id="5900c-119">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="5900c-119">Location.</span></span>

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

### <span data-ttu-id="5900c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5900c-120">-Name</span></span>
<span data-ttu-id="5900c-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="5900c-121">Resource name.</span></span>

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

### <span data-ttu-id="5900c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5900c-122">-ResourceGroupName</span></span>
<span data-ttu-id="5900c-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5900c-123">Resource group name.</span></span>

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

### <span data-ttu-id="5900c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5900c-124">-ResourceId</span></span>
<span data-ttu-id="5900c-125">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="5900c-125">Resource ID.</span></span>

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

### <span data-ttu-id="5900c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5900c-126">CommonParameters</span></span>
<span data-ttu-id="5900c-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5900c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5900c-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5900c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5900c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5900c-129">INPUTS</span></span>

### <span data-ttu-id="5900c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5900c-130">System.String</span></span>

## <span data-ttu-id="5900c-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5900c-131">OUTPUTS</span></span>

### <span data-ttu-id="5900c-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="5900c-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="5900c-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5900c-133">NOTES</span></span>

## <span data-ttu-id="5900c-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5900c-134">RELATED LINKS</span></span>
