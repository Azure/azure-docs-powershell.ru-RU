---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsintelligencepacks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: d5877e29db7c678122af93d3e5d2d6281183e410
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732306"
---
# <span data-ttu-id="b79d5-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="b79d5-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="b79d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b79d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b79d5-103">Получает доступные пакеты поддержки интеллектуального анализа.</span><span class="sxs-lookup"><span data-stu-id="b79d5-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b79d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b79d5-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b79d5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b79d5-105">DESCRIPTION</span></span>
<span data-ttu-id="b79d5-106">Командлет **Get-AzureRmOperationalInsightsIntelligencePacks** получает доступные пакеты поддержки интеллектуального анализа.</span><span class="sxs-lookup"><span data-stu-id="b79d5-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="b79d5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b79d5-107">EXAMPLES</span></span>

### <span data-ttu-id="b79d5-108">Пример 1: получение пакетов для аналитики</span><span class="sxs-lookup"><span data-stu-id="b79d5-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="b79d5-109">Эта команда получает доступные пакеты поддержки интеллектуального анализа.</span><span class="sxs-lookup"><span data-stu-id="b79d5-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="b79d5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b79d5-110">PARAMETERS</span></span>

### <span data-ttu-id="b79d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b79d5-111">-DefaultProfile</span></span>
<span data-ttu-id="b79d5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b79d5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b79d5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b79d5-113">-ResourceGroupName</span></span>
<span data-ttu-id="b79d5-114">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="b79d5-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="b79d5-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b79d5-115">-WorkspaceName</span></span>
<span data-ttu-id="b79d5-116">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b79d5-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="b79d5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b79d5-117">CommonParameters</span></span>
<span data-ttu-id="b79d5-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b79d5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b79d5-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b79d5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b79d5-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b79d5-120">INPUTS</span></span>

### <span data-ttu-id="b79d5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b79d5-121">System.String</span></span>

## <span data-ttu-id="b79d5-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b79d5-122">OUTPUTS</span></span>

### <span data-ttu-id="b79d5-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="b79d5-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="b79d5-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="b79d5-124">NOTES</span></span>

## <span data-ttu-id="b79d5-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b79d5-125">RELATED LINKS</span></span>

[<span data-ttu-id="b79d5-126">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="b79d5-126">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


