---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
ms.openlocfilehash: 4ef54651b5490161d7fc28c4a0c068f7b4a1ed76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566761"
---
# <span data-ttu-id="88263-101">Get-AzureRmExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="88263-101">Get-AzureRmExternalSecuritySolution</span></span>

## <span data-ttu-id="88263-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88263-102">SYNOPSIS</span></span>
<span data-ttu-id="88263-103">Получение решения для внешней безопасности</span><span class="sxs-lookup"><span data-stu-id="88263-103">Get external security solution</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88263-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88263-104">SYNTAX</span></span>

### <span data-ttu-id="88263-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88263-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88263-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="88263-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88263-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="88263-107">SubscriptionLevelResource</span></span>
```
Get-AzureRmExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88263-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="88263-108">ResourceId</span></span>
```
Get-AzureRmExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88263-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88263-109">DESCRIPTION</span></span>
<span data-ttu-id="88263-110">Получение решения для внешней безопасности</span><span class="sxs-lookup"><span data-stu-id="88263-110">Get external security solution</span></span>

## <span data-ttu-id="88263-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88263-111">EXAMPLES</span></span>

### <span data-ttu-id="88263-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88263-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExternalSecuritySolution
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

<span data-ttu-id="88263-113">Получение всех внешних решений безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="88263-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="88263-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="88263-114">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="88263-115">Получение определенного внешнего решения для обеспечения безопасности</span><span class="sxs-lookup"><span data-stu-id="88263-115">Get a specific external security solution</span></span>

## <span data-ttu-id="88263-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88263-116">PARAMETERS</span></span>

### <span data-ttu-id="88263-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88263-117">-DefaultProfile</span></span>
<span data-ttu-id="88263-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88263-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88263-119">-Location</span><span class="sxs-lookup"><span data-stu-id="88263-119">-Location</span></span>
<span data-ttu-id="88263-120">Поиска.</span><span class="sxs-lookup"><span data-stu-id="88263-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88263-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88263-121">-Name</span></span>
<span data-ttu-id="88263-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="88263-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88263-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88263-123">-ResourceGroupName</span></span>
<span data-ttu-id="88263-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88263-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88263-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88263-125">-ResourceId</span></span>
<span data-ttu-id="88263-126">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="88263-126">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88263-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88263-127">CommonParameters</span></span>
<span data-ttu-id="88263-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88263-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88263-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88263-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88263-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88263-130">INPUTS</span></span>

### <span data-ttu-id="88263-131">System. String</span><span class="sxs-lookup"><span data-stu-id="88263-131">System.String</span></span>

## <span data-ttu-id="88263-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88263-132">OUTPUTS</span></span>

### <span data-ttu-id="88263-133">Microsoft. Azure. Commands. Security. Models. ExternalSecuritySolutions. PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="88263-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="88263-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="88263-134">NOTES</span></span>

## <span data-ttu-id="88263-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88263-135">RELATED LINKS</span></span>
