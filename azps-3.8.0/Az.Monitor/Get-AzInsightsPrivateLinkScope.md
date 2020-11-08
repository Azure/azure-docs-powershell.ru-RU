---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074087"
---
# <span data-ttu-id="38484-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="38484-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="38484-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38484-102">SYNOPSIS</span></span>
<span data-ttu-id="38484-103">Получение области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="38484-103">Get private link scope</span></span>

## <span data-ttu-id="38484-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38484-104">SYNTAX</span></span>

### <span data-ttu-id="38484-105">ByResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38484-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38484-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="38484-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38484-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38484-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38484-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38484-108">DESCRIPTION</span></span>
<span data-ttu-id="38484-109">Список или получение области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="38484-109">List or get private link scope</span></span> 

## <span data-ttu-id="38484-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38484-110">EXAMPLES</span></span>

### <span data-ttu-id="38484-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="38484-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="38484-112">Список областей личных ссылок в группе ресурсов "rg_name"</span><span class="sxs-lookup"><span data-stu-id="38484-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="38484-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="38484-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="38484-114">Получение области личных ссылок с именем "scope_name" в разделе "Группа ресурсов" rg_name "</span><span class="sxs-lookup"><span data-stu-id="38484-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="38484-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38484-115">PARAMETERS</span></span>

### <span data-ttu-id="38484-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38484-116">-DefaultProfile</span></span>
<span data-ttu-id="38484-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38484-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38484-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="38484-118">-Name</span></span>
<span data-ttu-id="38484-119">Имя области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="38484-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="38484-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38484-120">-ResourceGroupName</span></span>
<span data-ttu-id="38484-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="38484-121">Resource Group Name</span></span>

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

### <span data-ttu-id="38484-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38484-122">-ResourceId</span></span>
<span data-ttu-id="38484-123">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="38484-123">Resource Id</span></span>

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

### <span data-ttu-id="38484-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38484-124">CommonParameters</span></span>
<span data-ttu-id="38484-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38484-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38484-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38484-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38484-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38484-127">INPUTS</span></span>

### <span data-ttu-id="38484-128">System. String</span><span class="sxs-lookup"><span data-stu-id="38484-128">System.String</span></span>

## <span data-ttu-id="38484-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38484-129">OUTPUTS</span></span>

### <span data-ttu-id="38484-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="38484-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="38484-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="38484-131">NOTES</span></span>

## <span data-ttu-id="38484-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38484-132">RELATED LINKS</span></span>
