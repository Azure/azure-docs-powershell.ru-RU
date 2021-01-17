---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: 0314a7e6b661b0b007ffe2cf59f5618247e4b282
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396100"
---
# <span data-ttu-id="d16a0-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d16a0-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="d16a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d16a0-102">SYNOPSIS</span></span>
<span data-ttu-id="d16a0-103">"Получить решение для внешней безопасности"</span><span class="sxs-lookup"><span data-stu-id="d16a0-103">Get external security solution</span></span> 

## <span data-ttu-id="d16a0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d16a0-104">SYNTAX</span></span>

### <span data-ttu-id="d16a0-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d16a0-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d16a0-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="d16a0-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d16a0-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d16a0-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d16a0-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d16a0-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d16a0-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d16a0-109">DESCRIPTION</span></span>
<span data-ttu-id="d16a0-110">"Получить решение для внешней безопасности"</span><span class="sxs-lookup"><span data-stu-id="d16a0-110">Get external security solution</span></span>

## <span data-ttu-id="d16a0-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d16a0-111">EXAMPLES</span></span>

### <span data-ttu-id="d16a0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d16a0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-e
                    us
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-eus/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-eus
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-eus
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-weu/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-w
                    eu
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-weu/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-weu
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-weu
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.opera
                    tionalinsights/workspaces/securityuserws
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/mainws/providers/Microsoft.Secur
                    ity/locations/centralus/externalSecuritySolutions/aad_securityuserws
Name              : aad_securityuserws
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.o
                    perationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.S
                    ecurity/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="d16a0-113">Получите все внешние решения безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="d16a0-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="d16a0-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d16a0-114">Example 2</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="d16a0-115">Получите определенное внешнее решение для обеспечения безопасности</span><span class="sxs-lookup"><span data-stu-id="d16a0-115">Get a specific external security solution</span></span>

## <span data-ttu-id="d16a0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d16a0-116">PARAMETERS</span></span>

### <span data-ttu-id="d16a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d16a0-117">-DefaultProfile</span></span>
<span data-ttu-id="d16a0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d16a0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d16a0-119">-Location</span><span class="sxs-lookup"><span data-stu-id="d16a0-119">-Location</span></span>
<span data-ttu-id="d16a0-120">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="d16a0-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16a0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d16a0-121">-Name</span></span>
<span data-ttu-id="d16a0-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d16a0-122">Resource name.</span></span>

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

### <span data-ttu-id="d16a0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d16a0-123">-ResourceGroupName</span></span>
<span data-ttu-id="d16a0-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d16a0-124">Resource group name.</span></span>

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

### <span data-ttu-id="d16a0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d16a0-125">-ResourceId</span></span>
<span data-ttu-id="d16a0-126">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="d16a0-126">Resource ID.</span></span>

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

### <span data-ttu-id="d16a0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d16a0-127">CommonParameters</span></span>
<span data-ttu-id="d16a0-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d16a0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d16a0-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d16a0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d16a0-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d16a0-130">INPUTS</span></span>

### <span data-ttu-id="d16a0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d16a0-131">System.String</span></span>

## <span data-ttu-id="d16a0-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d16a0-132">OUTPUTS</span></span>

### <span data-ttu-id="d16a0-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d16a0-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="d16a0-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d16a0-134">NOTES</span></span>

## <span data-ttu-id="d16a0-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d16a0-135">RELATED LINKS</span></span>
