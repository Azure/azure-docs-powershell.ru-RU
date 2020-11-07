---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: d609ee8910a1dc016365d126b61bc1f4820e977c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911710"
---
# <span data-ttu-id="19085-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="19085-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="19085-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19085-102">SYNOPSIS</span></span>
<span data-ttu-id="19085-103">Запускает сбор данных syslog с компьютеров Linux.</span><span class="sxs-lookup"><span data-stu-id="19085-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="19085-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19085-104">SYNTAX</span></span>

### <span data-ttu-id="19085-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19085-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19085-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="19085-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19085-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19085-107">DESCRIPTION</span></span>
<span data-ttu-id="19085-108">Командлет **Enable-AzOperationalInsightsLinuxSyslogCollection** запускает сбор данных syslog из подключенных компьютеров Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="19085-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="19085-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19085-109">EXAMPLES</span></span>

## <span data-ttu-id="19085-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19085-110">PARAMETERS</span></span>

### <span data-ttu-id="19085-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19085-111">-DefaultProfile</span></span>
<span data-ttu-id="19085-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="19085-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19085-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19085-113">-ResourceGroupName</span></span>
<span data-ttu-id="19085-114">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="19085-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="19085-115">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="19085-115">-Workspace</span></span>
<span data-ttu-id="19085-116">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="19085-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="19085-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="19085-117">-WorkspaceName</span></span>
<span data-ttu-id="19085-118">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="19085-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="19085-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19085-119">-Confirm</span></span>
<span data-ttu-id="19085-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19085-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19085-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19085-121">-WhatIf</span></span>
<span data-ttu-id="19085-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19085-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19085-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19085-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19085-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19085-124">CommonParameters</span></span>
<span data-ttu-id="19085-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19085-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19085-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19085-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19085-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19085-127">INPUTS</span></span>

### <span data-ttu-id="19085-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="19085-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="19085-129">System. String</span><span class="sxs-lookup"><span data-stu-id="19085-129">System.String</span></span>

## <span data-ttu-id="19085-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19085-130">OUTPUTS</span></span>

### <span data-ttu-id="19085-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="19085-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="19085-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="19085-132">NOTES</span></span>
* <span data-ttu-id="19085-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="19085-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="19085-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19085-134">RELATED LINKS</span></span>

[<span data-ttu-id="19085-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="19085-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="19085-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="19085-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


