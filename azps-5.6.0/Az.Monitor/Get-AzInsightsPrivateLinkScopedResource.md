---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: ff4e75e2301ef9ae2ccd6f2e5064e06aedc2dbd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980040"
---
# <span data-ttu-id="f9d94-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f9d94-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="f9d94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9d94-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d94-103">Получить для ресурса с областью личных ссылок</span><span class="sxs-lookup"><span data-stu-id="f9d94-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="f9d94-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f9d94-104">SYNTAX</span></span>

### <span data-ttu-id="f9d94-105">ByScopeParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f9d94-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9d94-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d94-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9d94-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d94-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9d94-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9d94-108">DESCRIPTION</span></span>
<span data-ttu-id="f9d94-109">Получить или список для частного ресурса с областью действия ссылки для ресурса с областью действия может быть рабочей областью журнала или компонентом Application Insights</span><span class="sxs-lookup"><span data-stu-id="f9d94-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="f9d94-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f9d94-110">EXAMPLES</span></span>

### <span data-ttu-id="f9d94-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f9d94-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="f9d94-112">Ресурс с областью списка в области частных связей "scope_name"</span><span class="sxs-lookup"><span data-stu-id="f9d94-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="f9d94-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f9d94-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="f9d94-114">Задать область ресурса в области частных связей "scope_name" с именем "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="f9d94-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="f9d94-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9d94-115">PARAMETERS</span></span>

### <span data-ttu-id="f9d94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9d94-116">-DefaultProfile</span></span>
<span data-ttu-id="f9d94-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9d94-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9d94-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9d94-118">-InputObject</span></span>
<span data-ttu-id="f9d94-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f9d94-119">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d94-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f9d94-120">-Name</span></span>
<span data-ttu-id="f9d94-121">Имя ресурса с областью</span><span class="sxs-lookup"><span data-stu-id="f9d94-121">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d94-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d94-122">-ResourceGroupName</span></span>
<span data-ttu-id="f9d94-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f9d94-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d94-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9d94-124">-ResourceId</span></span>
<span data-ttu-id="f9d94-125">ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f9d94-125">Resource Id</span></span>

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

### <span data-ttu-id="f9d94-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="f9d94-126">-ScopeName</span></span>
<span data-ttu-id="f9d94-127">Имя области приватных ссылок</span><span class="sxs-lookup"><span data-stu-id="f9d94-127">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d94-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d94-128">CommonParameters</span></span>
<span data-ttu-id="f9d94-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9d94-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d94-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9d94-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d94-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9d94-131">INPUTS</span></span>

### <span data-ttu-id="f9d94-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f9d94-132">System.String</span></span>

## <span data-ttu-id="f9d94-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f9d94-133">OUTPUTS</span></span>

### <span data-ttu-id="f9d94-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f9d94-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="f9d94-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f9d94-135">NOTES</span></span>

## <span data-ttu-id="f9d94-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9d94-136">RELATED LINKS</span></span>
