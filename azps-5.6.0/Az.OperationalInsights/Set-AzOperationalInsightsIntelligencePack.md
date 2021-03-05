---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: ee65492adc8c2756a2d19871e4c673668d471c84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989736"
---
# <span data-ttu-id="b4e44-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="b4e44-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="b4e44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4e44-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e44-103">Включает или отключает указанный пакет аналитики.</span><span class="sxs-lookup"><span data-stu-id="b4e44-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="b4e44-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4e44-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4e44-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4e44-105">DESCRIPTION</span></span>
<span data-ttu-id="b4e44-106">С помощью cmdlet **Set-AzOperationalInsightsIntelligencePack** можно включить  указанный пакет аналитики, если  для него задано $True, и отключить его, если включено $False.</span><span class="sxs-lookup"><span data-stu-id="b4e44-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="b4e44-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4e44-107">EXAMPLES</span></span>

### <span data-ttu-id="b4e44-108">Пример 1. Настройка пакетов аналитики</span><span class="sxs-lookup"><span data-stu-id="b4e44-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="b4e44-109">Эта команда включает указанный пакет аналитики.</span><span class="sxs-lookup"><span data-stu-id="b4e44-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="b4e44-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4e44-110">PARAMETERS</span></span>

### <span data-ttu-id="b4e44-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e44-111">-DefaultProfile</span></span>
<span data-ttu-id="b4e44-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b4e44-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4e44-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="b4e44-113">-Enabled</span></span>
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

### <span data-ttu-id="b4e44-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="b4e44-114">-IntelligencePackName</span></span>
<span data-ttu-id="b4e44-115">Указывает имя пакета аналитики.</span><span class="sxs-lookup"><span data-stu-id="b4e44-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="b4e44-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e44-116">-ResourceGroupName</span></span>
<span data-ttu-id="b4e44-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4e44-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="b4e44-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b4e44-118">-WorkspaceName</span></span>
<span data-ttu-id="b4e44-119">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b4e44-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="b4e44-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e44-120">CommonParameters</span></span>
<span data-ttu-id="b4e44-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e44-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e44-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4e44-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e44-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4e44-123">INPUTS</span></span>

### <span data-ttu-id="b4e44-124">System.String</span><span class="sxs-lookup"><span data-stu-id="b4e44-124">System.String</span></span>

### <span data-ttu-id="b4e44-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4e44-125">System.Boolean</span></span>

## <span data-ttu-id="b4e44-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4e44-126">OUTPUTS</span></span>

### <span data-ttu-id="b4e44-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="b4e44-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="b4e44-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4e44-128">NOTES</span></span>

## <span data-ttu-id="b4e44-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4e44-129">RELATED LINKS</span></span>

[<span data-ttu-id="b4e44-130">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b4e44-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


