---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 71a0089b4f593032404b71f17ba432486f5498d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248084"
---
# <span data-ttu-id="ac818-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="ac818-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="ac818-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac818-102">SYNOPSIS</span></span>
<span data-ttu-id="ac818-103">Останавливает сбор журналов IIS с компьютеров.</span><span class="sxs-lookup"><span data-stu-id="ac818-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="ac818-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac818-104">SYNTAX</span></span>

### <span data-ttu-id="ac818-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac818-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac818-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ac818-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac818-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac818-107">DESCRIPTION</span></span>
<span data-ttu-id="ac818-108">Командлет **Disable-AzOperationalInsightsIISLogCollection** останавливает сбор журналов служб IIS на подключенных компьютерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ac818-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="ac818-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac818-109">EXAMPLES</span></span>

## <span data-ttu-id="ac818-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac818-110">PARAMETERS</span></span>

### <span data-ttu-id="ac818-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac818-111">-DefaultProfile</span></span>
<span data-ttu-id="ac818-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ac818-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac818-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac818-113">-ResourceGroupName</span></span>
<span data-ttu-id="ac818-114">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="ac818-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="ac818-115">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="ac818-115">-Workspace</span></span>
<span data-ttu-id="ac818-116">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ac818-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ac818-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ac818-117">-WorkspaceName</span></span>
<span data-ttu-id="ac818-118">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ac818-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ac818-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac818-119">-Confirm</span></span>
<span data-ttu-id="ac818-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac818-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac818-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac818-121">-WhatIf</span></span>
<span data-ttu-id="ac818-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac818-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac818-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac818-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac818-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac818-124">CommonParameters</span></span>
<span data-ttu-id="ac818-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac818-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac818-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac818-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac818-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac818-127">INPUTS</span></span>

### <span data-ttu-id="ac818-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ac818-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ac818-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ac818-129">System.String</span></span>

## <span data-ttu-id="ac818-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac818-130">OUTPUTS</span></span>

### <span data-ttu-id="ac818-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ac818-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ac818-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac818-132">NOTES</span></span>
* <span data-ttu-id="ac818-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="ac818-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="ac818-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac818-134">RELATED LINKS</span></span>

[<span data-ttu-id="ac818-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="ac818-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)


