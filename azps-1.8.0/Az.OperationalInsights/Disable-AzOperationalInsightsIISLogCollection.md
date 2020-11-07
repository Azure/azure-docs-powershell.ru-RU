---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: d808f7287a8ae3c03d86867f409d28820325e858
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729876"
---
# <span data-ttu-id="77d3e-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="77d3e-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="77d3e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="77d3e-103">Останавливает сбор журналов IIS с компьютеров.</span><span class="sxs-lookup"><span data-stu-id="77d3e-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="77d3e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77d3e-104">SYNTAX</span></span>

### <span data-ttu-id="77d3e-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77d3e-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77d3e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="77d3e-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77d3e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77d3e-107">DESCRIPTION</span></span>
<span data-ttu-id="77d3e-108">Командлет **Disable-AzOperationalInsightsIISLogCollection** останавливает сбор журналов служб IIS на подключенных компьютерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="77d3e-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="77d3e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77d3e-109">EXAMPLES</span></span>

## <span data-ttu-id="77d3e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77d3e-110">PARAMETERS</span></span>

### <span data-ttu-id="77d3e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77d3e-111">-DefaultProfile</span></span>
<span data-ttu-id="77d3e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="77d3e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77d3e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77d3e-113">-ResourceGroupName</span></span>
<span data-ttu-id="77d3e-114">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="77d3e-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="77d3e-115">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="77d3e-115">-Workspace</span></span>
<span data-ttu-id="77d3e-116">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="77d3e-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="77d3e-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="77d3e-117">-WorkspaceName</span></span>
<span data-ttu-id="77d3e-118">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="77d3e-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="77d3e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77d3e-119">-Confirm</span></span>
<span data-ttu-id="77d3e-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="77d3e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77d3e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77d3e-121">-WhatIf</span></span>
<span data-ttu-id="77d3e-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="77d3e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77d3e-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="77d3e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77d3e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d3e-124">CommonParameters</span></span>
<span data-ttu-id="77d3e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77d3e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d3e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77d3e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d3e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77d3e-127">INPUTS</span></span>

### <span data-ttu-id="77d3e-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="77d3e-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="77d3e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="77d3e-129">System.String</span></span>

## <span data-ttu-id="77d3e-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77d3e-130">OUTPUTS</span></span>

### <span data-ttu-id="77d3e-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="77d3e-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="77d3e-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="77d3e-132">NOTES</span></span>
* <span data-ttu-id="77d3e-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="77d3e-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="77d3e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77d3e-134">RELATED LINKS</span></span>

[<span data-ttu-id="77d3e-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="77d3e-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)


