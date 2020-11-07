---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: 2d018bd704d776b506035f365fc5045a51202d13
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912127"
---
# <span data-ttu-id="b3f4b-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="b3f4b-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="b3f4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f4b-103">Получение решения для внешней безопасности</span><span class="sxs-lookup"><span data-stu-id="b3f4b-103">Get external security solution</span></span> 

## <span data-ttu-id="b3f4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3f4b-104">SYNTAX</span></span>

### <span data-ttu-id="b3f4b-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3f4b-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3f4b-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="b3f4b-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3f4b-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b3f4b-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3f4b-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3f4b-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3f4b-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3f4b-109">DESCRIPTION</span></span>
<span data-ttu-id="b3f4b-110">Получение решения для внешней безопасности</span><span class="sxs-lookup"><span data-stu-id="b3f4b-110">Get external security solution</span></span>

## <span data-ttu-id="b3f4b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3f4b-111">EXAMPLES</span></span>

### <span data-ttu-id="b3f4b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3f4b-112">Example 1</span></span>
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

<span data-ttu-id="b3f4b-113">Получение всех внешних решений безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="b3f4b-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="b3f4b-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b3f4b-114">Example 2</span></span>
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

<span data-ttu-id="b3f4b-115">Получение определенного внешнего решения для обеспечения безопасности</span><span class="sxs-lookup"><span data-stu-id="b3f4b-115">Get a specific external security solution</span></span>

## <span data-ttu-id="b3f4b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3f4b-116">PARAMETERS</span></span>

### <span data-ttu-id="b3f4b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f4b-117">-DefaultProfile</span></span>
<span data-ttu-id="b3f4b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f4b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3f4b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b3f4b-119">-Location</span></span>
<span data-ttu-id="b3f4b-120">Поиска.</span><span class="sxs-lookup"><span data-stu-id="b3f4b-120">Location.</span></span>

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

### <span data-ttu-id="b3f4b-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b3f4b-121">-Name</span></span>
<span data-ttu-id="b3f4b-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b3f4b-122">Resource name.</span></span>

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

### <span data-ttu-id="b3f4b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f4b-123">-ResourceGroupName</span></span>
<span data-ttu-id="b3f4b-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b3f4b-124">Resource group name.</span></span>

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

### <span data-ttu-id="b3f4b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3f4b-125">-ResourceId</span></span>
<span data-ttu-id="b3f4b-126">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b3f4b-126">Resource ID.</span></span>

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

### <span data-ttu-id="b3f4b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f4b-127">CommonParameters</span></span>
<span data-ttu-id="b3f4b-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3f4b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f4b-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3f4b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f4b-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3f4b-130">INPUTS</span></span>

### <span data-ttu-id="b3f4b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b3f4b-131">System.String</span></span>

## <span data-ttu-id="b3f4b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3f4b-132">OUTPUTS</span></span>

### <span data-ttu-id="b3f4b-133">Microsoft. Azure. Commands. Security. Models. ExternalSecuritySolutions. PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="b3f4b-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="b3f4b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3f4b-134">NOTES</span></span>

## <span data-ttu-id="b3f4b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3f4b-135">RELATED LINKS</span></span>
