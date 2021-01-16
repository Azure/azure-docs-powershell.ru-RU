---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a8d799cec6278149cb4c08faf68584fb7968f85e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507742"
---
# <span data-ttu-id="39b85-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="39b85-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="39b85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39b85-102">SYNOPSIS</span></span>
<span data-ttu-id="39b85-103">Включает или отключает указанный пакет аналитики.</span><span class="sxs-lookup"><span data-stu-id="39b85-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="39b85-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39b85-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39b85-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39b85-105">DESCRIPTION</span></span>
<span data-ttu-id="39b85-106">С помощью cmdlet **Set-AzOperationalInsightsIntelligencePack** можно включить  указанный пакет аналитики, если  для него задано $True, и отключить его, если включено $False.</span><span class="sxs-lookup"><span data-stu-id="39b85-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="39b85-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39b85-107">EXAMPLES</span></span>

### <span data-ttu-id="39b85-108">Пример 1. Настройка пакетов аналитики</span><span class="sxs-lookup"><span data-stu-id="39b85-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="39b85-109">Эта команда включает указанный пакет аналитики.</span><span class="sxs-lookup"><span data-stu-id="39b85-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="39b85-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39b85-110">PARAMETERS</span></span>

### <span data-ttu-id="39b85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b85-111">-DefaultProfile</span></span>
<span data-ttu-id="39b85-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="39b85-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39b85-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="39b85-113">-Enabled</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39b85-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="39b85-114">-IntelligencePackName</span></span>
<span data-ttu-id="39b85-115">Указывает имя пакета аналитики.</span><span class="sxs-lookup"><span data-stu-id="39b85-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39b85-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39b85-116">-ResourceGroupName</span></span>
<span data-ttu-id="39b85-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="39b85-117">Specifies the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39b85-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="39b85-118">-WorkspaceName</span></span>
<span data-ttu-id="39b85-119">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="39b85-119">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39b85-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b85-120">CommonParameters</span></span>
<span data-ttu-id="39b85-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39b85-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b85-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39b85-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b85-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39b85-123">INPUTS</span></span>

### <span data-ttu-id="39b85-124">System.String</span><span class="sxs-lookup"><span data-stu-id="39b85-124">System.String</span></span>

### <span data-ttu-id="39b85-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39b85-125">System.Boolean</span></span>

## <span data-ttu-id="39b85-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39b85-126">OUTPUTS</span></span>

### <span data-ttu-id="39b85-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="39b85-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="39b85-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39b85-128">NOTES</span></span>

## <span data-ttu-id="39b85-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39b85-129">RELATED LINKS</span></span>

[<span data-ttu-id="39b85-130">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="39b85-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


