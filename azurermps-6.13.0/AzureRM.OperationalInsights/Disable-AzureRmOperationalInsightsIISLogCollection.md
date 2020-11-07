---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 085aa91321f9e263e4fa5620f982beb01eab2b16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732240"
---
# <span data-ttu-id="3f648-101">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="3f648-101">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="3f648-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f648-102">SYNOPSIS</span></span>
<span data-ttu-id="3f648-103">Останавливает сбор журналов IIS с компьютеров.</span><span class="sxs-lookup"><span data-stu-id="3f648-103">Stops collection of IIS logs from computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f648-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f648-104">SYNTAX</span></span>

### <span data-ttu-id="3f648-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f648-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f648-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3f648-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f648-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f648-107">DESCRIPTION</span></span>
<span data-ttu-id="3f648-108">Командлет **Disable-AzureRmOperationalInsightsIISLogCollection** останавливает сбор журналов служб IIS на подключенных компьютерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3f648-108">The **Disable-AzureRmOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="3f648-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f648-109">EXAMPLES</span></span>

## <span data-ttu-id="3f648-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f648-110">PARAMETERS</span></span>

### <span data-ttu-id="3f648-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f648-111">-DefaultProfile</span></span>
<span data-ttu-id="3f648-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3f648-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f648-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f648-113">-ResourceGroupName</span></span>
<span data-ttu-id="3f648-114">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="3f648-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="3f648-115">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="3f648-115">-Workspace</span></span>
<span data-ttu-id="3f648-116">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3f648-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3f648-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3f648-117">-WorkspaceName</span></span>
<span data-ttu-id="3f648-118">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3f648-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3f648-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f648-119">-Confirm</span></span>
<span data-ttu-id="3f648-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3f648-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f648-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f648-121">-WhatIf</span></span>
<span data-ttu-id="3f648-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3f648-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f648-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3f648-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f648-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f648-124">CommonParameters</span></span>
<span data-ttu-id="3f648-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f648-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f648-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f648-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f648-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f648-127">INPUTS</span></span>

### <span data-ttu-id="3f648-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3f648-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="3f648-129">Параметры: Workspace (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3f648-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="3f648-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3f648-130">System.String</span></span>

## <span data-ttu-id="3f648-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f648-131">OUTPUTS</span></span>

### <span data-ttu-id="3f648-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3f648-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3f648-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f648-133">NOTES</span></span>
* <span data-ttu-id="3f648-134">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="3f648-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="3f648-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f648-135">RELATED LINKS</span></span>

[<span data-ttu-id="3f648-136">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="3f648-136">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Enable-AzureRmOperationalInsightsIISLogCollection.md)


