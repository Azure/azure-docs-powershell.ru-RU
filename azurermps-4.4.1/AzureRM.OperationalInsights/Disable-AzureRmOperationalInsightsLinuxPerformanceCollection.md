---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 0af85097efb1b8383caf41d9f5bb5328957585fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734255"
---
# <span data-ttu-id="339ee-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="339ee-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="339ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="339ee-102">SYNOPSIS</span></span>
<span data-ttu-id="339ee-103">Останавливает сбор счетчиков производительности на компьютерах с ОС Linux.</span><span class="sxs-lookup"><span data-stu-id="339ee-103">Stops collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="339ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="339ee-104">SYNTAX</span></span>

### <span data-ttu-id="339ee-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="339ee-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="339ee-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="339ee-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="339ee-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="339ee-107">DESCRIPTION</span></span>
<span data-ttu-id="339ee-108">Командлет **Disable-AzureRmOperationalInsightsLinuxPerformanceCollection** останавливает сбор счетчиков производительности на подключенных компьютерах Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="339ee-108">The **Disable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="339ee-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="339ee-109">EXAMPLES</span></span>

## <span data-ttu-id="339ee-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="339ee-110">PARAMETERS</span></span>

### <span data-ttu-id="339ee-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339ee-111">-ResourceGroupName</span></span>
<span data-ttu-id="339ee-112">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="339ee-112">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="339ee-113">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="339ee-113">-Workspace</span></span>
<span data-ttu-id="339ee-114">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="339ee-114">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="339ee-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="339ee-115">-WorkspaceName</span></span>
<span data-ttu-id="339ee-116">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="339ee-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="339ee-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="339ee-117">-Confirm</span></span>
<span data-ttu-id="339ee-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="339ee-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="339ee-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="339ee-119">-WhatIf</span></span>
<span data-ttu-id="339ee-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="339ee-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="339ee-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="339ee-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="339ee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339ee-122">-DefaultProfile</span></span>
<span data-ttu-id="339ee-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="339ee-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="339ee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339ee-124">CommonParameters</span></span>
<span data-ttu-id="339ee-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="339ee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339ee-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="339ee-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339ee-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="339ee-127">INPUTS</span></span>

### <span data-ttu-id="339ee-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="339ee-128">PSWorkspace</span></span>
<span data-ttu-id="339ee-129">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="339ee-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="339ee-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="339ee-130">OUTPUTS</span></span>

### <span data-ttu-id="339ee-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="339ee-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="339ee-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="339ee-132">NOTES</span></span>
* <span data-ttu-id="339ee-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="339ee-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="339ee-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="339ee-134">RELATED LINKS</span></span>

[<span data-ttu-id="339ee-135">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="339ee-135">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="339ee-136">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="339ee-136">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


