---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241309"
---
# <span data-ttu-id="f2a6a-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="f2a6a-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="f2a6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a6a-103">List configurationAssignments for resource.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="f2a6a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f2a6a-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2a6a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2a6a-105">DESCRIPTION</span></span>
<span data-ttu-id="f2a6a-106">List configurationAssignments for resource.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="f2a6a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f2a6a-107">EXAMPLES</span></span>

### <span data-ttu-id="f2a6a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f2a6a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="f2a6a-109">List configurationAssignments for dedicated host.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="f2a6a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2a6a-110">PARAMETERS</span></span>

### <span data-ttu-id="f2a6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a6a-111">-DefaultProfile</span></span>
<span data-ttu-id="f2a6a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2a6a-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="f2a6a-113">-ProviderName</span></span>
<span data-ttu-id="f2a6a-114">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="f2a6a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2a6a-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2a6a-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="f2a6a-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f2a6a-117">-ResourceName</span></span>
<span data-ttu-id="f2a6a-118">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-118">The resource name.</span></span>

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

### <span data-ttu-id="f2a6a-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="f2a6a-119">-ResourceParentName</span></span>
<span data-ttu-id="f2a6a-120">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-120">The parent resource name.</span></span>

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

### <span data-ttu-id="f2a6a-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="f2a6a-121">-ResourceParentType</span></span>
<span data-ttu-id="f2a6a-122">Родительский тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-122">The parent resource type.</span></span>

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

### <span data-ttu-id="f2a6a-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f2a6a-123">-ResourceType</span></span>
<span data-ttu-id="f2a6a-124">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-124">The resource type.</span></span>

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

### <span data-ttu-id="f2a6a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a6a-125">CommonParameters</span></span>
<span data-ttu-id="f2a6a-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a6a-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2a6a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a6a-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2a6a-128">INPUTS</span></span>

### <span data-ttu-id="f2a6a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f2a6a-129">System.String</span></span>

## <span data-ttu-id="f2a6a-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2a6a-130">OUTPUTS</span></span>

### <span data-ttu-id="f2a6a-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="f2a6a-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="f2a6a-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f2a6a-132">NOTES</span></span>

## <span data-ttu-id="f2a6a-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2a6a-133">RELATED LINKS</span></span>
