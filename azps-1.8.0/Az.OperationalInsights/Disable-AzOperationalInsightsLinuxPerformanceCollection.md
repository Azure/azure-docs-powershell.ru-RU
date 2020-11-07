---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 0a39dae7ebdc6cc2c1fcc1b77ceb9b5d8e330d66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729868"
---
# <span data-ttu-id="b3298-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="b3298-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="b3298-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3298-102">SYNOPSIS</span></span>
<span data-ttu-id="b3298-103">Останавливает сбор счетчиков производительности на компьютерах с ОС Linux.</span><span class="sxs-lookup"><span data-stu-id="b3298-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="b3298-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3298-104">SYNTAX</span></span>

### <span data-ttu-id="b3298-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3298-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3298-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b3298-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3298-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3298-107">DESCRIPTION</span></span>
<span data-ttu-id="b3298-108">Командлет **Disable-AzOperationalInsightsLinuxPerformanceCollection** останавливает сбор счетчиков производительности на подключенных компьютерах Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b3298-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="b3298-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3298-109">EXAMPLES</span></span>

## <span data-ttu-id="b3298-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3298-110">PARAMETERS</span></span>

### <span data-ttu-id="b3298-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3298-111">-DefaultProfile</span></span>
<span data-ttu-id="b3298-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b3298-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3298-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3298-113">-ResourceGroupName</span></span>
<span data-ttu-id="b3298-114">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="b3298-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3298-115">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="b3298-115">-Workspace</span></span>
<span data-ttu-id="b3298-116">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b3298-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3298-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b3298-117">-WorkspaceName</span></span>
<span data-ttu-id="b3298-118">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b3298-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3298-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3298-119">-Confirm</span></span>
<span data-ttu-id="b3298-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b3298-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3298-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3298-121">-WhatIf</span></span>
<span data-ttu-id="b3298-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b3298-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3298-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b3298-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3298-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3298-124">CommonParameters</span></span>
<span data-ttu-id="b3298-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3298-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3298-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3298-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3298-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3298-127">INPUTS</span></span>

### <span data-ttu-id="b3298-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b3298-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="b3298-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b3298-129">System.String</span></span>

## <span data-ttu-id="b3298-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3298-130">OUTPUTS</span></span>

### <span data-ttu-id="b3298-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="b3298-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="b3298-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3298-132">NOTES</span></span>
* <span data-ttu-id="b3298-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="b3298-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="b3298-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3298-134">RELATED LINKS</span></span>

[<span data-ttu-id="b3298-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="b3298-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="b3298-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="b3298-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


