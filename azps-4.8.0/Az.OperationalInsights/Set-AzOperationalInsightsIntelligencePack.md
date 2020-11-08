---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a8d799cec6278149cb4c08faf68584fb7968f85e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234839"
---
# <span data-ttu-id="16fc3-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="16fc3-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="16fc3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="16fc3-103">Включение или отключение указанного пакета для аналитики.</span><span class="sxs-lookup"><span data-stu-id="16fc3-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="16fc3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16fc3-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16fc3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="16fc3-106">Командлет **Set-AzOperationalInsightsIntelligencePack** включает указанный пакет интеллектуального анализа, если этот параметр $true *включен* , и отключается *, если для* него установлено значение $false.</span><span class="sxs-lookup"><span data-stu-id="16fc3-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="16fc3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16fc3-107">EXAMPLES</span></span>

### <span data-ttu-id="16fc3-108">Пример 1: Настройка пакетов интеллекта</span><span class="sxs-lookup"><span data-stu-id="16fc3-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="16fc3-109">Эта команда включает указанный пакет для аналитики.</span><span class="sxs-lookup"><span data-stu-id="16fc3-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="16fc3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16fc3-110">PARAMETERS</span></span>

### <span data-ttu-id="16fc3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16fc3-111">-DefaultProfile</span></span>
<span data-ttu-id="16fc3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="16fc3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16fc3-113">-Включено</span><span class="sxs-lookup"><span data-stu-id="16fc3-113">-Enabled</span></span>
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

### <span data-ttu-id="16fc3-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="16fc3-114">-IntelligencePackName</span></span>
<span data-ttu-id="16fc3-115">Указывает имя пакета аналитики.</span><span class="sxs-lookup"><span data-stu-id="16fc3-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="16fc3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16fc3-116">-ResourceGroupName</span></span>
<span data-ttu-id="16fc3-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16fc3-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="16fc3-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="16fc3-118">-WorkspaceName</span></span>
<span data-ttu-id="16fc3-119">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="16fc3-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="16fc3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16fc3-120">CommonParameters</span></span>
<span data-ttu-id="16fc3-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16fc3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16fc3-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16fc3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16fc3-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16fc3-123">INPUTS</span></span>

### <span data-ttu-id="16fc3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="16fc3-124">System.String</span></span>

### <span data-ttu-id="16fc3-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="16fc3-125">System.Boolean</span></span>

## <span data-ttu-id="16fc3-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16fc3-126">OUTPUTS</span></span>

### <span data-ttu-id="16fc3-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="16fc3-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="16fc3-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="16fc3-128">NOTES</span></span>

## <span data-ttu-id="16fc3-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16fc3-129">RELATED LINKS</span></span>

[<span data-ttu-id="16fc3-130">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="16fc3-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


