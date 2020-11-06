---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 3fdd6b407753e8edd9ba7faa074e287062f15fb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560840"
---
# <span data-ttu-id="559e1-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="559e1-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="559e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="559e1-102">SYNOPSIS</span></span>
<span data-ttu-id="559e1-103">Останавливает сбор данных syslog с компьютеров Linux.</span><span class="sxs-lookup"><span data-stu-id="559e1-103">Stops collection of syslog data from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="559e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="559e1-104">SYNTAX</span></span>

### <span data-ttu-id="559e1-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="559e1-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="559e1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="559e1-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="559e1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="559e1-107">DESCRIPTION</span></span>
<span data-ttu-id="559e1-108">Командлет **Disable-AzureRmOperationalInsightsLinuxSyslogCollection** останавливает сбор данных syslog из подключенных компьютеров Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="559e1-108">The **Disable-AzureRmOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="559e1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="559e1-109">EXAMPLES</span></span>

## <span data-ttu-id="559e1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="559e1-110">PARAMETERS</span></span>

### <span data-ttu-id="559e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="559e1-111">-DefaultProfile</span></span>
<span data-ttu-id="559e1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="559e1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559e1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="559e1-113">-ResourceGroupName</span></span>
<span data-ttu-id="559e1-114">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="559e1-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="559e1-115">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="559e1-115">-Workspace</span></span>
<span data-ttu-id="559e1-116">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="559e1-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="559e1-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="559e1-117">-WorkspaceName</span></span>
<span data-ttu-id="559e1-118">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="559e1-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="559e1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="559e1-119">-Confirm</span></span>
<span data-ttu-id="559e1-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="559e1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="559e1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="559e1-121">-WhatIf</span></span>
<span data-ttu-id="559e1-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="559e1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="559e1-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="559e1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="559e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="559e1-124">CommonParameters</span></span>
<span data-ttu-id="559e1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="559e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="559e1-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="559e1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="559e1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="559e1-127">INPUTS</span></span>

### <span data-ttu-id="559e1-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="559e1-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="559e1-129">Параметры: Workspace (ByValue)</span><span class="sxs-lookup"><span data-stu-id="559e1-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="559e1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="559e1-130">System.String</span></span>

## <span data-ttu-id="559e1-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="559e1-131">OUTPUTS</span></span>

### <span data-ttu-id="559e1-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="559e1-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="559e1-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="559e1-133">NOTES</span></span>
* <span data-ttu-id="559e1-134">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="559e1-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="559e1-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="559e1-135">RELATED LINKS</span></span>

[<span data-ttu-id="559e1-136">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="559e1-136">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="559e1-137">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="559e1-137">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


