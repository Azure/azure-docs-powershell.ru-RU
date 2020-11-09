---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 92fbc7e67bb81422e021a23810f3045b5cf32cba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318986"
---
# <span data-ttu-id="11b9b-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="11b9b-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="11b9b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="11b9b-103">Останавливает сбор счетчиков производительности на компьютерах с ОС Linux.</span><span class="sxs-lookup"><span data-stu-id="11b9b-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="11b9b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11b9b-104">SYNTAX</span></span>

### <span data-ttu-id="11b9b-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11b9b-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11b9b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="11b9b-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11b9b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11b9b-107">DESCRIPTION</span></span>
<span data-ttu-id="11b9b-108">Командлет **Disable-AzOperationalInsightsLinuxPerformanceCollection** останавливает сбор счетчиков производительности на подключенных компьютерах Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="11b9b-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="11b9b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11b9b-109">EXAMPLES</span></span>

## <span data-ttu-id="11b9b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11b9b-110">PARAMETERS</span></span>

### <span data-ttu-id="11b9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b9b-111">-DefaultProfile</span></span>
<span data-ttu-id="11b9b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="11b9b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11b9b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b9b-113">-ResourceGroupName</span></span>
<span data-ttu-id="11b9b-114">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="11b9b-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="11b9b-115">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="11b9b-115">-Workspace</span></span>
<span data-ttu-id="11b9b-116">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="11b9b-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="11b9b-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="11b9b-117">-WorkspaceName</span></span>
<span data-ttu-id="11b9b-118">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="11b9b-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="11b9b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11b9b-119">-Confirm</span></span>
<span data-ttu-id="11b9b-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11b9b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11b9b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b9b-121">-WhatIf</span></span>
<span data-ttu-id="11b9b-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11b9b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11b9b-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11b9b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11b9b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b9b-124">CommonParameters</span></span>
<span data-ttu-id="11b9b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11b9b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b9b-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b9b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b9b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11b9b-127">INPUTS</span></span>

### <span data-ttu-id="11b9b-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="11b9b-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="11b9b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="11b9b-129">System.String</span></span>

## <span data-ttu-id="11b9b-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11b9b-130">OUTPUTS</span></span>

### <span data-ttu-id="11b9b-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="11b9b-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="11b9b-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="11b9b-132">NOTES</span></span>
* <span data-ttu-id="11b9b-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="11b9b-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="11b9b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11b9b-134">RELATED LINKS</span></span>

[<span data-ttu-id="11b9b-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="11b9b-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="11b9b-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="11b9b-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


