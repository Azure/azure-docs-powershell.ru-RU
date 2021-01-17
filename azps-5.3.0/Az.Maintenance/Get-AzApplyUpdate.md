---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425564"
---
# <span data-ttu-id="6a90f-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="6a90f-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="6a90f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a90f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a90f-103">Отслеживание обновлений обслуживания для ресурса</span><span class="sxs-lookup"><span data-stu-id="6a90f-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="6a90f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6a90f-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a90f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a90f-105">DESCRIPTION</span></span>
<span data-ttu-id="6a90f-106">Отслеживание обновлений обслуживания для ресурса</span><span class="sxs-lookup"><span data-stu-id="6a90f-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="6a90f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6a90f-107">EXAMPLES</span></span>

### <span data-ttu-id="6a90f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6a90f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="6a90f-109">Отслеживание обновлений обслуживания для ресурса</span><span class="sxs-lookup"><span data-stu-id="6a90f-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="6a90f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a90f-110">PARAMETERS</span></span>

### <span data-ttu-id="6a90f-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="6a90f-111">-ApplyUpdateName</span></span>
<span data-ttu-id="6a90f-112">Имя ресурса применить обновление.</span><span class="sxs-lookup"><span data-stu-id="6a90f-112">The apply update resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a90f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a90f-113">-DefaultProfile</span></span>
<span data-ttu-id="6a90f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a90f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a90f-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="6a90f-115">-ProviderName</span></span>
<span data-ttu-id="6a90f-116">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a90f-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="6a90f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a90f-117">-ResourceGroupName</span></span>
<span data-ttu-id="6a90f-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a90f-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="6a90f-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6a90f-119">-ResourceName</span></span>
<span data-ttu-id="6a90f-120">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="6a90f-120">The resource name.</span></span>

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

### <span data-ttu-id="6a90f-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="6a90f-121">-ResourceParentName</span></span>
<span data-ttu-id="6a90f-122">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="6a90f-122">The parent resource name.</span></span>

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

### <span data-ttu-id="6a90f-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="6a90f-123">-ResourceParentType</span></span>
<span data-ttu-id="6a90f-124">Родительский тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="6a90f-124">The parent resource type.</span></span>

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

### <span data-ttu-id="6a90f-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6a90f-125">-ResourceType</span></span>
<span data-ttu-id="6a90f-126">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="6a90f-126">The resource type.</span></span>

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

### <span data-ttu-id="6a90f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a90f-127">CommonParameters</span></span>
<span data-ttu-id="6a90f-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a90f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a90f-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a90f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a90f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a90f-130">INPUTS</span></span>

### <span data-ttu-id="6a90f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6a90f-131">System.String</span></span>

## <span data-ttu-id="6a90f-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a90f-132">OUTPUTS</span></span>

### <span data-ttu-id="6a90f-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="6a90f-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="6a90f-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6a90f-134">NOTES</span></span>

## <span data-ttu-id="6a90f-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a90f-135">RELATED LINKS</span></span>
