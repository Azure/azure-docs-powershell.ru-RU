---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 67858083ed648e2965ea6fad2900ab63ef453901
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904706"
---
# <span data-ttu-id="61f29-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="61f29-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="61f29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61f29-102">SYNOPSIS</span></span>
<span data-ttu-id="61f29-103">Запускает сбор настраиваемых журналов на компьютерах с ОС Linux.</span><span class="sxs-lookup"><span data-stu-id="61f29-103">Starts collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="61f29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61f29-104">SYNTAX</span></span>

### <span data-ttu-id="61f29-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61f29-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f29-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="61f29-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61f29-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61f29-107">DESCRIPTION</span></span>
<span data-ttu-id="61f29-108">Командлет **Enable-AzOperationalInsightsLinuxCustomLogCollection** запускает сбор настраиваемых журналов из подключенных компьютеров Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="61f29-108">The **Enable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="61f29-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61f29-109">EXAMPLES</span></span>

## <span data-ttu-id="61f29-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61f29-110">PARAMETERS</span></span>

### <span data-ttu-id="61f29-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f29-111">-DefaultProfile</span></span>
<span data-ttu-id="61f29-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="61f29-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61f29-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f29-113">-ResourceGroupName</span></span>
<span data-ttu-id="61f29-114">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="61f29-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="61f29-115">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="61f29-115">-Workspace</span></span>
<span data-ttu-id="61f29-116">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="61f29-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="61f29-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="61f29-117">-WorkspaceName</span></span>
<span data-ttu-id="61f29-118">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="61f29-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="61f29-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61f29-119">-Confirm</span></span>
<span data-ttu-id="61f29-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="61f29-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61f29-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f29-121">-WhatIf</span></span>
<span data-ttu-id="61f29-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="61f29-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61f29-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="61f29-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61f29-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f29-124">CommonParameters</span></span>
<span data-ttu-id="61f29-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61f29-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f29-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f29-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f29-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61f29-127">INPUTS</span></span>

### <span data-ttu-id="61f29-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="61f29-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="61f29-129">System. String</span><span class="sxs-lookup"><span data-stu-id="61f29-129">System.String</span></span>

## <span data-ttu-id="61f29-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61f29-130">OUTPUTS</span></span>

### <span data-ttu-id="61f29-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="61f29-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="61f29-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="61f29-132">NOTES</span></span>
* <span data-ttu-id="61f29-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="61f29-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="61f29-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61f29-134">RELATED LINKS</span></span>

[<span data-ttu-id="61f29-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="61f29-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)


