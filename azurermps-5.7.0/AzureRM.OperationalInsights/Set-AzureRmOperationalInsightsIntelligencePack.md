---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: c7a4a34e3969f209bcd6fcaae46ed93cd316aba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560215"
---
# <span data-ttu-id="9aef0-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="9aef0-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="9aef0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9aef0-102">SYNOPSIS</span></span>
<span data-ttu-id="9aef0-103">Включение или отключение указанного пакета для аналитики.</span><span class="sxs-lookup"><span data-stu-id="9aef0-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aef0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9aef0-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9aef0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aef0-105">DESCRIPTION</span></span>
<span data-ttu-id="9aef0-106">Командлет **Set-AzureRmOperationalInsightsIntelligencePack** включает указанный пакет интеллектуального анализа, если этот параметр $true *включен* , и отключается *, если для* него установлено значение $false.</span><span class="sxs-lookup"><span data-stu-id="9aef0-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="9aef0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9aef0-107">EXAMPLES</span></span>

### <span data-ttu-id="9aef0-108">Пример 1: Настройка пакетов интеллекта</span><span class="sxs-lookup"><span data-stu-id="9aef0-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="9aef0-109">Эта команда включает указанный пакет для аналитики.</span><span class="sxs-lookup"><span data-stu-id="9aef0-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="9aef0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9aef0-110">PARAMETERS</span></span>

### <span data-ttu-id="9aef0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aef0-111">-DefaultProfile</span></span>
<span data-ttu-id="9aef0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9aef0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aef0-113">-Включено</span><span class="sxs-lookup"><span data-stu-id="9aef0-113">-Enabled</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aef0-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="9aef0-114">-IntelligencePackName</span></span>
<span data-ttu-id="9aef0-115">Указывает имя пакета аналитики.</span><span class="sxs-lookup"><span data-stu-id="9aef0-115">Specifies the Intelligence Pack name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aef0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aef0-116">-ResourceGroupName</span></span>
<span data-ttu-id="9aef0-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9aef0-117">Specifies the resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aef0-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9aef0-118">-WorkspaceName</span></span>
<span data-ttu-id="9aef0-119">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9aef0-119">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aef0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aef0-120">CommonParameters</span></span>
<span data-ttu-id="9aef0-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9aef0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aef0-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aef0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aef0-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9aef0-123">INPUTS</span></span>

### <span data-ttu-id="9aef0-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="9aef0-124">None</span></span>
<span data-ttu-id="9aef0-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9aef0-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9aef0-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aef0-126">OUTPUTS</span></span>

## <span data-ttu-id="9aef0-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="9aef0-127">NOTES</span></span>

## <span data-ttu-id="9aef0-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9aef0-128">RELATED LINKS</span></span>

[<span data-ttu-id="9aef0-129">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="9aef0-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


