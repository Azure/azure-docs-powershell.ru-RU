---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 76499570abb458987b79f4cd707a6845b43cfe24
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729867"
---
# <span data-ttu-id="b5dc0-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="b5dc0-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="b5dc0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="b5dc0-103">Останавливает сбор данных syslog с компьютеров Linux.</span><span class="sxs-lookup"><span data-stu-id="b5dc0-103">Stops collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="b5dc0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5dc0-104">SYNTAX</span></span>

### <span data-ttu-id="b5dc0-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5dc0-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5dc0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b5dc0-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5dc0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5dc0-107">DESCRIPTION</span></span>
<span data-ttu-id="b5dc0-108">Командлет **Disable-AzOperationalInsightsLinuxSyslogCollection** останавливает сбор данных syslog из подключенных компьютеров Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b5dc0-108">The **Disable-AzOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="b5dc0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5dc0-109">EXAMPLES</span></span>

## <span data-ttu-id="b5dc0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5dc0-110">PARAMETERS</span></span>

### <span data-ttu-id="b5dc0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5dc0-111">-DefaultProfile</span></span>
<span data-ttu-id="b5dc0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b5dc0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5dc0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5dc0-113">-ResourceGroupName</span></span>
<span data-ttu-id="b5dc0-114">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="b5dc0-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="b5dc0-115">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="b5dc0-115">-Workspace</span></span>
<span data-ttu-id="b5dc0-116">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b5dc0-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b5dc0-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b5dc0-117">-WorkspaceName</span></span>
<span data-ttu-id="b5dc0-118">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b5dc0-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b5dc0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5dc0-119">-Confirm</span></span>
<span data-ttu-id="b5dc0-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b5dc0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5dc0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5dc0-121">-WhatIf</span></span>
<span data-ttu-id="b5dc0-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b5dc0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5dc0-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b5dc0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5dc0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5dc0-124">CommonParameters</span></span>
<span data-ttu-id="b5dc0-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5dc0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5dc0-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5dc0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5dc0-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5dc0-127">INPUTS</span></span>

### <span data-ttu-id="b5dc0-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b5dc0-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="b5dc0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b5dc0-129">System.String</span></span>

## <span data-ttu-id="b5dc0-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5dc0-130">OUTPUTS</span></span>

### <span data-ttu-id="b5dc0-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="b5dc0-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="b5dc0-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5dc0-132">NOTES</span></span>
* <span data-ttu-id="b5dc0-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="b5dc0-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="b5dc0-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5dc0-134">RELATED LINKS</span></span>

[<span data-ttu-id="b5dc0-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="b5dc0-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="b5dc0-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="b5dc0-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


