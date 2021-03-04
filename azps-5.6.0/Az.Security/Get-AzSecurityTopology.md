---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: 0f6cbe88eaabb49a07bb0704f0d6ea547449a229
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990755"
---
# <span data-ttu-id="cf1d9-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="cf1d9-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="cf1d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf1d9-102">SYNOPSIS</span></span>
<span data-ttu-id="cf1d9-103">Получает список топорологий безопасности для подписки</span><span class="sxs-lookup"><span data-stu-id="cf1d9-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="cf1d9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cf1d9-104">SYNTAX</span></span>

### <span data-ttu-id="cf1d9-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf1d9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf1d9-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="cf1d9-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf1d9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf1d9-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf1d9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf1d9-108">DESCRIPTION</span></span>
<span data-ttu-id="cf1d9-109">Центр безопасности Azure автоматически обнаруживает topologies системы безопасности. Используйте этот cmdlet для просмотра опечаток безопасности.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="cf1d9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cf1d9-110">EXAMPLES</span></span>

### <span data-ttu-id="cf1d9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cf1d9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="cf1d9-112">Просмотр всех опечаток безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="cf1d9-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="cf1d9-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cf1d9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="cf1d9-114">Получите конкретные опологи для системы безопасности</span><span class="sxs-lookup"><span data-stu-id="cf1d9-114">Get a specific security topologies</span></span>

## <span data-ttu-id="cf1d9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf1d9-115">PARAMETERS</span></span>

### <span data-ttu-id="cf1d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf1d9-116">-DefaultProfile</span></span>
<span data-ttu-id="cf1d9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf1d9-118">-Location</span><span class="sxs-lookup"><span data-stu-id="cf1d9-118">-Location</span></span>
<span data-ttu-id="cf1d9-119">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="cf1d9-119">Location.</span></span>

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

### <span data-ttu-id="cf1d9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cf1d9-120">-Name</span></span>
<span data-ttu-id="cf1d9-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-121">Resource name.</span></span>

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

### <span data-ttu-id="cf1d9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf1d9-122">-ResourceGroupName</span></span>
<span data-ttu-id="cf1d9-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-123">Resource group name.</span></span>

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

### <span data-ttu-id="cf1d9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf1d9-124">-ResourceId</span></span>
<span data-ttu-id="cf1d9-125">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-125">Resource ID.</span></span>

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

### <span data-ttu-id="cf1d9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf1d9-126">CommonParameters</span></span>
<span data-ttu-id="cf1d9-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf1d9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf1d9-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf1d9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf1d9-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf1d9-129">INPUTS</span></span>

### <span data-ttu-id="cf1d9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cf1d9-130">System.String</span></span>

## <span data-ttu-id="cf1d9-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf1d9-131">OUTPUTS</span></span>

### <span data-ttu-id="cf1d9-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="cf1d9-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="cf1d9-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cf1d9-133">NOTES</span></span>

## <span data-ttu-id="cf1d9-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf1d9-134">RELATED LINKS</span></span>
