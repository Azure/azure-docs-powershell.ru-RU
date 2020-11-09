---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244438"
---
# <span data-ttu-id="63827-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="63827-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="63827-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63827-102">SYNOPSIS</span></span>
<span data-ttu-id="63827-103">Получить ресурс с областью личных ссылок</span><span class="sxs-lookup"><span data-stu-id="63827-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="63827-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63827-104">SYNTAX</span></span>

### <span data-ttu-id="63827-105">ByScopeParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="63827-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63827-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63827-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63827-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63827-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63827-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63827-108">DESCRIPTION</span></span>
<span data-ttu-id="63827-109">Получить или просмотреть список ресурсов с областью действия "частный канал", ресурс с областью действия может быть рабочей областью Analytics log или компонент Application Insights</span><span class="sxs-lookup"><span data-stu-id="63827-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="63827-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63827-110">EXAMPLES</span></span>

### <span data-ttu-id="63827-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63827-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="63827-112">Список ресурсов с областью действия "scope_name" в области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="63827-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="63827-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="63827-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="63827-114">Получение ресурса с областью в области личных ссылок "scope_name" с именем "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="63827-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="63827-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63827-115">PARAMETERS</span></span>

### <span data-ttu-id="63827-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63827-116">-DefaultProfile</span></span>
<span data-ttu-id="63827-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63827-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63827-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63827-118">-InputObject</span></span>
<span data-ttu-id="63827-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="63827-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="63827-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63827-120">-Name</span></span>
<span data-ttu-id="63827-121">Название ресурса с областью действия</span><span class="sxs-lookup"><span data-stu-id="63827-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="63827-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63827-122">-ResourceGroupName</span></span>
<span data-ttu-id="63827-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="63827-123">Resource Group Name</span></span>

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

### <span data-ttu-id="63827-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63827-124">-ResourceId</span></span>
<span data-ttu-id="63827-125">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="63827-125">Resource Id</span></span>

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

### <span data-ttu-id="63827-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="63827-126">-ScopeName</span></span>
<span data-ttu-id="63827-127">Имя области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="63827-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="63827-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63827-128">CommonParameters</span></span>
<span data-ttu-id="63827-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63827-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63827-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63827-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63827-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63827-131">INPUTS</span></span>

### <span data-ttu-id="63827-132">System. String</span><span class="sxs-lookup"><span data-stu-id="63827-132">System.String</span></span>

## <span data-ttu-id="63827-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63827-133">OUTPUTS</span></span>

### <span data-ttu-id="63827-134">icrosoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="63827-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="63827-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="63827-135">NOTES</span></span>

## <span data-ttu-id="63827-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63827-136">RELATED LINKS</span></span>