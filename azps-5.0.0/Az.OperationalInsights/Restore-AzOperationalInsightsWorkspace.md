---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245925"
---
# <span data-ttu-id="de623-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="de623-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="de623-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de623-102">SYNOPSIS</span></span>
<span data-ttu-id="de623-103">Восстановление удаленной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="de623-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="de623-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de623-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de623-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de623-105">DESCRIPTION</span></span>
<span data-ttu-id="de623-106">Восстановление удаленной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="de623-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="de623-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de623-107">EXAMPLES</span></span>

### <span data-ttu-id="de623-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="de623-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="de623-109">Восстановить удаленную рабочую область.</span><span class="sxs-lookup"><span data-stu-id="de623-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="de623-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de623-110">PARAMETERS</span></span>

### <span data-ttu-id="de623-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de623-111">-DefaultProfile</span></span>
<span data-ttu-id="de623-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de623-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de623-113">-Force</span><span class="sxs-lookup"><span data-stu-id="de623-113">-Force</span></span>
<span data-ttu-id="de623-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="de623-114">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de623-115">-Location</span><span class="sxs-lookup"><span data-stu-id="de623-115">-Location</span></span>
<span data-ttu-id="de623-116">Географическая область, в которой будет создана Рабочая область.</span><span class="sxs-lookup"><span data-stu-id="de623-116">The geographic region that the workspace will be created in.</span></span>

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

### <span data-ttu-id="de623-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="de623-117">-Name</span></span>
<span data-ttu-id="de623-118">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="de623-118">The workspace name.</span></span>

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

### <span data-ttu-id="de623-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de623-119">-ResourceGroupName</span></span>
<span data-ttu-id="de623-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de623-120">The resource group name.</span></span>

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

### <span data-ttu-id="de623-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de623-121">-Confirm</span></span>
<span data-ttu-id="de623-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="de623-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de623-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de623-123">-WhatIf</span></span>
<span data-ttu-id="de623-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="de623-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de623-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="de623-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de623-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de623-126">CommonParameters</span></span>
<span data-ttu-id="de623-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de623-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de623-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de623-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de623-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de623-129">INPUTS</span></span>

### <span data-ttu-id="de623-130">System. String</span><span class="sxs-lookup"><span data-stu-id="de623-130">System.String</span></span>

## <span data-ttu-id="de623-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de623-131">OUTPUTS</span></span>

### <span data-ttu-id="de623-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="de623-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="de623-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="de623-133">NOTES</span></span>

## <span data-ttu-id="de623-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de623-134">RELATED LINKS</span></span>
