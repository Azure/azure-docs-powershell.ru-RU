---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912336"
---
# <span data-ttu-id="06fe4-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="06fe4-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="06fe4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="06fe4-103">Отслеживание обновлений обслуживания для ресурса</span><span class="sxs-lookup"><span data-stu-id="06fe4-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="06fe4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06fe4-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06fe4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06fe4-105">DESCRIPTION</span></span>
<span data-ttu-id="06fe4-106">Отслеживание обновлений обслуживания для ресурса</span><span class="sxs-lookup"><span data-stu-id="06fe4-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="06fe4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06fe4-107">EXAMPLES</span></span>

### <span data-ttu-id="06fe4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="06fe4-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="06fe4-109">Отслеживание обновлений обслуживания для ресурса</span><span class="sxs-lookup"><span data-stu-id="06fe4-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="06fe4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06fe4-110">PARAMETERS</span></span>

### <span data-ttu-id="06fe4-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="06fe4-111">-ApplyUpdateName</span></span>
<span data-ttu-id="06fe4-112">Имя ресурса "применить обновление".</span><span class="sxs-lookup"><span data-stu-id="06fe4-112">The apply update resource name.</span></span>

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

### <span data-ttu-id="06fe4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06fe4-113">-DefaultProfile</span></span>
<span data-ttu-id="06fe4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06fe4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06fe4-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="06fe4-115">-ProviderName</span></span>
<span data-ttu-id="06fe4-116">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06fe4-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="06fe4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06fe4-117">-ResourceGroupName</span></span>
<span data-ttu-id="06fe4-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06fe4-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="06fe4-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="06fe4-119">-ResourceName</span></span>
<span data-ttu-id="06fe4-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="06fe4-120">The resource name.</span></span>

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

### <span data-ttu-id="06fe4-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="06fe4-121">-ResourceParentName</span></span>
<span data-ttu-id="06fe4-122">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="06fe4-122">The parent resource name.</span></span>

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

### <span data-ttu-id="06fe4-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="06fe4-123">-ResourceParentType</span></span>
<span data-ttu-id="06fe4-124">Родительский тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="06fe4-124">The parent resource type.</span></span>

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

### <span data-ttu-id="06fe4-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="06fe4-125">-ResourceType</span></span>
<span data-ttu-id="06fe4-126">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="06fe4-126">The resource type.</span></span>

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

### <span data-ttu-id="06fe4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06fe4-127">CommonParameters</span></span>
<span data-ttu-id="06fe4-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06fe4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06fe4-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06fe4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06fe4-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06fe4-130">INPUTS</span></span>

### <span data-ttu-id="06fe4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="06fe4-131">System.String</span></span>

## <span data-ttu-id="06fe4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06fe4-132">OUTPUTS</span></span>

### <span data-ttu-id="06fe4-133">Microsoft. Azure. Commands. Maintenance. Models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="06fe4-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="06fe4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="06fe4-134">NOTES</span></span>

## <span data-ttu-id="06fe4-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06fe4-135">RELATED LINKS</span></span>
