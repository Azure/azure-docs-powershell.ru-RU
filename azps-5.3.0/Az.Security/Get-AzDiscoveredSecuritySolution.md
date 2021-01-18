---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: 1fbe9e790966a92c38ba79b56221e5e6083b649c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517781"
---
# <span data-ttu-id="3306c-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="3306c-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="3306c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3306c-102">SYNOPSIS</span></span>
<span data-ttu-id="3306c-103">Получает решения безопасности, которые были выявлены Центром безопасности Azure</span><span class="sxs-lookup"><span data-stu-id="3306c-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="3306c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3306c-104">SYNTAX</span></span>

### <span data-ttu-id="3306c-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3306c-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3306c-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="3306c-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3306c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3306c-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3306c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3306c-108">DESCRIPTION</span></span>
<span data-ttu-id="3306c-109">Решения безопасности автоматически обнаруживает Центр безопасности Azure. Используйте этот cmdlet для просмотра обнаруженных решений безопасности.</span><span class="sxs-lookup"><span data-stu-id="3306c-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="3306c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3306c-110">EXAMPLES</span></span>

### <span data-ttu-id="3306c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3306c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="3306c-112">Поиск всех обнаруженных решений безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="3306c-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="3306c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3306c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="3306c-114">Получите определенное найденное решение для обеспечения безопасности</span><span class="sxs-lookup"><span data-stu-id="3306c-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="3306c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3306c-115">PARAMETERS</span></span>

### <span data-ttu-id="3306c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3306c-116">-DefaultProfile</span></span>
<span data-ttu-id="3306c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3306c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3306c-118">-Location</span><span class="sxs-lookup"><span data-stu-id="3306c-118">-Location</span></span>
<span data-ttu-id="3306c-119">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="3306c-119">Location.</span></span>

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

### <span data-ttu-id="3306c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3306c-120">-Name</span></span>
<span data-ttu-id="3306c-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="3306c-121">Resource name.</span></span>

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

### <span data-ttu-id="3306c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3306c-122">-ResourceGroupName</span></span>
<span data-ttu-id="3306c-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3306c-123">Resource group name.</span></span>

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

### <span data-ttu-id="3306c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3306c-124">-ResourceId</span></span>
<span data-ttu-id="3306c-125">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="3306c-125">Resource ID.</span></span>

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

### <span data-ttu-id="3306c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3306c-126">CommonParameters</span></span>
<span data-ttu-id="3306c-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3306c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3306c-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3306c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3306c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3306c-129">INPUTS</span></span>

### <span data-ttu-id="3306c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3306c-130">System.String</span></span>

## <span data-ttu-id="3306c-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3306c-131">OUTPUTS</span></span>

### <span data-ttu-id="3306c-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="3306c-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="3306c-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3306c-133">NOTES</span></span>

## <span data-ttu-id="3306c-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3306c-134">RELATED LINKS</span></span>
