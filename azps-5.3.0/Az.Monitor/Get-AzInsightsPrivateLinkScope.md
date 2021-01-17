---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425460"
---
# <span data-ttu-id="33a64-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="33a64-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="33a64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33a64-102">SYNOPSIS</span></span>
<span data-ttu-id="33a64-103">Личные ссылки</span><span class="sxs-lookup"><span data-stu-id="33a64-103">Get private link scope</span></span>

## <span data-ttu-id="33a64-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="33a64-104">SYNTAX</span></span>

### <span data-ttu-id="33a64-105">ByResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="33a64-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33a64-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="33a64-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33a64-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33a64-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33a64-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33a64-108">DESCRIPTION</span></span>
<span data-ttu-id="33a64-109">Список или личная область связываний</span><span class="sxs-lookup"><span data-stu-id="33a64-109">List or get private link scope</span></span> 

## <span data-ttu-id="33a64-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="33a64-110">EXAMPLES</span></span>

### <span data-ttu-id="33a64-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33a64-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="33a64-112">Список областей частных связей в группе ресурсов "rg_name"</span><span class="sxs-lookup"><span data-stu-id="33a64-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="33a64-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="33a64-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="33a64-114">Получите личную область ссылок с именем "scope_name" в группе ресурсов "rg_name"</span><span class="sxs-lookup"><span data-stu-id="33a64-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="33a64-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33a64-115">PARAMETERS</span></span>

### <span data-ttu-id="33a64-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a64-116">-DefaultProfile</span></span>
<span data-ttu-id="33a64-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33a64-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33a64-118">-Name</span><span class="sxs-lookup"><span data-stu-id="33a64-118">-Name</span></span>
<span data-ttu-id="33a64-119">Имя области приватных ссылок</span><span class="sxs-lookup"><span data-stu-id="33a64-119">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a64-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33a64-120">-ResourceGroupName</span></span>
<span data-ttu-id="33a64-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="33a64-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a64-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33a64-122">-ResourceId</span></span>
<span data-ttu-id="33a64-123">ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="33a64-123">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a64-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a64-124">CommonParameters</span></span>
<span data-ttu-id="33a64-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a64-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a64-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33a64-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a64-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33a64-127">INPUTS</span></span>

### <span data-ttu-id="33a64-128">System.String</span><span class="sxs-lookup"><span data-stu-id="33a64-128">System.String</span></span>

## <span data-ttu-id="33a64-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="33a64-129">OUTPUTS</span></span>

### <span data-ttu-id="33a64-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="33a64-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="33a64-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="33a64-131">NOTES</span></span>

## <span data-ttu-id="33a64-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33a64-132">RELATED LINKS</span></span>
