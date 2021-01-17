---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: d8d3e4df3349acb1340a24362043d32d528fc284
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425519"
---
# <span data-ttu-id="eaf51-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="eaf51-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="eaf51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaf51-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf51-103">Получать ожидающих обновления обслуживания для ресурса.</span><span class="sxs-lookup"><span data-stu-id="eaf51-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="eaf51-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eaf51-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaf51-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaf51-105">DESCRIPTION</span></span>
<span data-ttu-id="eaf51-106">Получать ожидающих обновления обслуживания для ресурса.</span><span class="sxs-lookup"><span data-stu-id="eaf51-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="eaf51-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eaf51-107">EXAMPLES</span></span>

### <span data-ttu-id="eaf51-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eaf51-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="eaf51-109">Получать ожидающих обновления обслуживания для ресурса.</span><span class="sxs-lookup"><span data-stu-id="eaf51-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="eaf51-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eaf51-110">PARAMETERS</span></span>

### <span data-ttu-id="eaf51-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf51-111">-DefaultProfile</span></span>
<span data-ttu-id="eaf51-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf51-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaf51-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="eaf51-113">-ProviderName</span></span>
<span data-ttu-id="eaf51-114">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eaf51-114">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf51-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaf51-115">-ResourceGroupName</span></span>
<span data-ttu-id="eaf51-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eaf51-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf51-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="eaf51-117">-ResourceName</span></span>
<span data-ttu-id="eaf51-118">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="eaf51-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf51-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="eaf51-119">-ResourceParentName</span></span>
<span data-ttu-id="eaf51-120">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="eaf51-120">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf51-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="eaf51-121">-ResourceParentType</span></span>
<span data-ttu-id="eaf51-122">Родительский тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="eaf51-122">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf51-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="eaf51-123">-ResourceType</span></span>
<span data-ttu-id="eaf51-124">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="eaf51-124">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf51-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf51-125">CommonParameters</span></span>
<span data-ttu-id="eaf51-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaf51-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf51-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eaf51-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf51-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eaf51-128">INPUTS</span></span>

### <span data-ttu-id="eaf51-129">System.String</span><span class="sxs-lookup"><span data-stu-id="eaf51-129">System.String</span></span>

## <span data-ttu-id="eaf51-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eaf51-130">OUTPUTS</span></span>

### <span data-ttu-id="eaf51-131">Microsoft.Azure.Management.Maintenance.Models.Update</span><span class="sxs-lookup"><span data-stu-id="eaf51-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="eaf51-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eaf51-132">NOTES</span></span>

## <span data-ttu-id="eaf51-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eaf51-133">RELATED LINKS</span></span>
