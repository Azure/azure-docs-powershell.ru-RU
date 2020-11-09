---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: f48007be3e1209cff65e46c669bce46298182247
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318974"
---
# <span data-ttu-id="062b4-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="062b4-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="062b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="062b4-102">SYNOPSIS</span></span>
<span data-ttu-id="062b4-103">Запускает сбор журналов IIS на компьютерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="062b4-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="062b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="062b4-104">SYNTAX</span></span>

### <span data-ttu-id="062b4-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="062b4-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="062b4-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="062b4-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="062b4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="062b4-107">DESCRIPTION</span></span>
<span data-ttu-id="062b4-108">Командлет **Enable-AzOperationalInsightsIISLogCollection** запускает сбор журналов служб IIS с подключенных компьютеров в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="062b4-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="062b4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="062b4-109">EXAMPLES</span></span>

## <span data-ttu-id="062b4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="062b4-110">PARAMETERS</span></span>

### <span data-ttu-id="062b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="062b4-111">-DefaultProfile</span></span>
<span data-ttu-id="062b4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="062b4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="062b4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="062b4-113">-ResourceGroupName</span></span>
<span data-ttu-id="062b4-114">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="062b4-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="062b4-115">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="062b4-115">-Workspace</span></span>
<span data-ttu-id="062b4-116">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="062b4-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="062b4-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="062b4-117">-WorkspaceName</span></span>
<span data-ttu-id="062b4-118">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="062b4-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="062b4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="062b4-119">-Confirm</span></span>
<span data-ttu-id="062b4-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="062b4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="062b4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="062b4-121">-WhatIf</span></span>
<span data-ttu-id="062b4-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="062b4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="062b4-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="062b4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="062b4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="062b4-124">CommonParameters</span></span>
<span data-ttu-id="062b4-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="062b4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="062b4-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="062b4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="062b4-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="062b4-127">INPUTS</span></span>

### <span data-ttu-id="062b4-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="062b4-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="062b4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="062b4-129">System.String</span></span>

## <span data-ttu-id="062b4-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="062b4-130">OUTPUTS</span></span>

### <span data-ttu-id="062b4-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="062b4-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="062b4-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="062b4-132">NOTES</span></span>

## <span data-ttu-id="062b4-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="062b4-133">RELATED LINKS</span></span>

[<span data-ttu-id="062b4-134">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="062b4-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)

