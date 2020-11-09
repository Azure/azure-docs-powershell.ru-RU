---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248599"
---
# <span data-ttu-id="9ecc2-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9ecc2-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="9ecc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ecc2-102">SYNOPSIS</span></span>
<span data-ttu-id="9ecc2-103">Получение области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="9ecc2-103">Get private link scope</span></span>

## <span data-ttu-id="9ecc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ecc2-104">SYNTAX</span></span>

### <span data-ttu-id="9ecc2-105">ByResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ecc2-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ecc2-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ecc2-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ecc2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ecc2-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ecc2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ecc2-108">DESCRIPTION</span></span>
<span data-ttu-id="9ecc2-109">Список или получение области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="9ecc2-109">List or get private link scope</span></span> 

## <span data-ttu-id="9ecc2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ecc2-110">EXAMPLES</span></span>

### <span data-ttu-id="9ecc2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9ecc2-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="9ecc2-112">Список областей личных ссылок в группе ресурсов "rg_name"</span><span class="sxs-lookup"><span data-stu-id="9ecc2-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="9ecc2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9ecc2-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="9ecc2-114">Получение области личных ссылок с именем "scope_name" в разделе "Группа ресурсов" rg_name "</span><span class="sxs-lookup"><span data-stu-id="9ecc2-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="9ecc2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ecc2-115">PARAMETERS</span></span>

### <span data-ttu-id="9ecc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ecc2-116">-DefaultProfile</span></span>
<span data-ttu-id="9ecc2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ecc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ecc2-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ecc2-118">-Name</span></span>
<span data-ttu-id="9ecc2-119">Имя области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="9ecc2-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="9ecc2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ecc2-120">-ResourceGroupName</span></span>
<span data-ttu-id="9ecc2-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9ecc2-121">Resource Group Name</span></span>

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

### <span data-ttu-id="9ecc2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ecc2-122">-ResourceId</span></span>
<span data-ttu-id="9ecc2-123">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="9ecc2-123">Resource Id</span></span>

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

### <span data-ttu-id="9ecc2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ecc2-124">CommonParameters</span></span>
<span data-ttu-id="9ecc2-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ecc2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ecc2-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ecc2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ecc2-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ecc2-127">INPUTS</span></span>

### <span data-ttu-id="9ecc2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9ecc2-128">System.String</span></span>

## <span data-ttu-id="9ecc2-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ecc2-129">OUTPUTS</span></span>

### <span data-ttu-id="9ecc2-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9ecc2-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="9ecc2-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ecc2-131">NOTES</span></span>

## <span data-ttu-id="9ecc2-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ecc2-132">RELATED LINKS</span></span>