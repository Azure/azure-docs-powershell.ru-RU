---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: f5bc73ee6fc2f3c20b92f8780bcddec99bc46fee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318983"
---
# <span data-ttu-id="85c62-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="85c62-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="85c62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85c62-102">SYNOPSIS</span></span>
<span data-ttu-id="85c62-103">Останавливает сбор данных syslog с компьютеров Linux.</span><span class="sxs-lookup"><span data-stu-id="85c62-103">Stops collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="85c62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85c62-104">SYNTAX</span></span>

### <span data-ttu-id="85c62-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85c62-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85c62-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="85c62-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85c62-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85c62-107">DESCRIPTION</span></span>
<span data-ttu-id="85c62-108">Командлет **Disable-AzOperationalInsightsLinuxSyslogCollection** останавливает сбор данных syslog из подключенных компьютеров Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="85c62-108">The **Disable-AzOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="85c62-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85c62-109">EXAMPLES</span></span>

## <span data-ttu-id="85c62-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85c62-110">PARAMETERS</span></span>

### <span data-ttu-id="85c62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c62-111">-DefaultProfile</span></span>
<span data-ttu-id="85c62-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="85c62-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85c62-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85c62-113">-ResourceGroupName</span></span>
<span data-ttu-id="85c62-114">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="85c62-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="85c62-115">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="85c62-115">-Workspace</span></span>
<span data-ttu-id="85c62-116">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="85c62-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="85c62-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="85c62-117">-WorkspaceName</span></span>
<span data-ttu-id="85c62-118">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="85c62-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="85c62-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85c62-119">-Confirm</span></span>
<span data-ttu-id="85c62-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="85c62-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85c62-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85c62-121">-WhatIf</span></span>
<span data-ttu-id="85c62-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="85c62-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85c62-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="85c62-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85c62-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c62-124">CommonParameters</span></span>
<span data-ttu-id="85c62-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85c62-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c62-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85c62-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c62-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85c62-127">INPUTS</span></span>

### <span data-ttu-id="85c62-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="85c62-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="85c62-129">System. String</span><span class="sxs-lookup"><span data-stu-id="85c62-129">System.String</span></span>

## <span data-ttu-id="85c62-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85c62-130">OUTPUTS</span></span>

### <span data-ttu-id="85c62-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="85c62-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="85c62-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="85c62-132">NOTES</span></span>
* <span data-ttu-id="85c62-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="85c62-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="85c62-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85c62-134">RELATED LINKS</span></span>

[<span data-ttu-id="85c62-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="85c62-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="85c62-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="85c62-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)

