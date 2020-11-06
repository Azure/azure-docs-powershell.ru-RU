---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 0e8335476fc1cb511aaddb5294ea508832a04003
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560800"
---
# <span data-ttu-id="2994b-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="2994b-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="2994b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2994b-102">SYNOPSIS</span></span>
<span data-ttu-id="2994b-103">Включение или отключение указанного пакета для аналитики.</span><span class="sxs-lookup"><span data-stu-id="2994b-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2994b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2994b-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2994b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2994b-105">DESCRIPTION</span></span>
<span data-ttu-id="2994b-106">Командлет **Set-AzureRmOperationalInsightsIntelligencePack** включает указанный пакет интеллектуального анализа, если этот параметр $true *включен* , и отключается *, если для* него установлено значение $false.</span><span class="sxs-lookup"><span data-stu-id="2994b-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="2994b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2994b-107">EXAMPLES</span></span>

### <span data-ttu-id="2994b-108">Пример 1: Настройка пакетов интеллекта</span><span class="sxs-lookup"><span data-stu-id="2994b-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="2994b-109">Эта команда включает указанный пакет для аналитики.</span><span class="sxs-lookup"><span data-stu-id="2994b-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="2994b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2994b-110">PARAMETERS</span></span>

### <span data-ttu-id="2994b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2994b-111">-DefaultProfile</span></span>
<span data-ttu-id="2994b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2994b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2994b-113">-Включено</span><span class="sxs-lookup"><span data-stu-id="2994b-113">-Enabled</span></span>
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

### <span data-ttu-id="2994b-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="2994b-114">-IntelligencePackName</span></span>
<span data-ttu-id="2994b-115">Указывает имя пакета аналитики.</span><span class="sxs-lookup"><span data-stu-id="2994b-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="2994b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2994b-116">-ResourceGroupName</span></span>
<span data-ttu-id="2994b-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2994b-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="2994b-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2994b-118">-WorkspaceName</span></span>
<span data-ttu-id="2994b-119">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2994b-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="2994b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2994b-120">CommonParameters</span></span>
<span data-ttu-id="2994b-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2994b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2994b-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2994b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2994b-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2994b-123">INPUTS</span></span>

### <span data-ttu-id="2994b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2994b-124">System.String</span></span>

### <span data-ttu-id="2994b-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2994b-125">System.Boolean</span></span>

## <span data-ttu-id="2994b-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2994b-126">OUTPUTS</span></span>

### <span data-ttu-id="2994b-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="2994b-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="2994b-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="2994b-128">NOTES</span></span>

## <span data-ttu-id="2994b-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2994b-129">RELATED LINKS</span></span>

[<span data-ttu-id="2994b-130">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="2994b-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


