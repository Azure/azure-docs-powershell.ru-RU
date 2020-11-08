---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: ba33d02ec8c47c91865cc2d0f5549e5f446ca2c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065105"
---
# <span data-ttu-id="94e28-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="94e28-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="94e28-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94e28-102">SYNOPSIS</span></span>
<span data-ttu-id="94e28-103">Определяет политику настраиваемого сбора журналов.</span><span class="sxs-lookup"><span data-stu-id="94e28-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="94e28-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94e28-104">SYNTAX</span></span>

### <span data-ttu-id="94e28-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94e28-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e28-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="94e28-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94e28-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94e28-107">DESCRIPTION</span></span>
<span data-ttu-id="94e28-108">Командлет **New-AzOperationalInsightsCustomLogDataSource** определяет политику настраиваемого сбора журналов.</span><span class="sxs-lookup"><span data-stu-id="94e28-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="94e28-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94e28-109">EXAMPLES</span></span>

## <span data-ttu-id="94e28-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94e28-110">PARAMETERS</span></span>

### <span data-ttu-id="94e28-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="94e28-111">-CustomLogRawJson</span></span>
<span data-ttu-id="94e28-112">Определяет настраиваемую политику коллекции как необработанную строку в формате JSON (объектная нотация JavaScript).</span><span class="sxs-lookup"><span data-stu-id="94e28-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94e28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e28-113">-DefaultProfile</span></span>
<span data-ttu-id="94e28-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="94e28-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94e28-115">-Force</span><span class="sxs-lookup"><span data-stu-id="94e28-115">-Force</span></span>
<span data-ttu-id="94e28-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="94e28-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94e28-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="94e28-117">-Name</span></span>
<span data-ttu-id="94e28-118">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="94e28-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="94e28-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94e28-119">-ResourceGroupName</span></span>
<span data-ttu-id="94e28-120">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="94e28-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="94e28-121">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="94e28-121">-Workspace</span></span>
<span data-ttu-id="94e28-122">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="94e28-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="94e28-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="94e28-123">-WorkspaceName</span></span>
<span data-ttu-id="94e28-124">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="94e28-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="94e28-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94e28-125">-Confirm</span></span>
<span data-ttu-id="94e28-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="94e28-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e28-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e28-127">-WhatIf</span></span>
<span data-ttu-id="94e28-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="94e28-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94e28-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="94e28-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94e28-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e28-130">CommonParameters</span></span>
<span data-ttu-id="94e28-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94e28-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e28-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94e28-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e28-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94e28-133">INPUTS</span></span>

### <span data-ttu-id="94e28-134">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="94e28-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="94e28-135">System. String</span><span class="sxs-lookup"><span data-stu-id="94e28-135">System.String</span></span>

## <span data-ttu-id="94e28-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94e28-136">OUTPUTS</span></span>

### <span data-ttu-id="94e28-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="94e28-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="94e28-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="94e28-138">NOTES</span></span>

## <span data-ttu-id="94e28-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94e28-139">RELATED LINKS</span></span>

[<span data-ttu-id="94e28-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="94e28-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="94e28-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="94e28-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


