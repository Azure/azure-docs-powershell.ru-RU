---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 607da2e6478d72915497f1476e04ae11f9a69b9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904650"
---
# <span data-ttu-id="14f5d-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="14f5d-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="14f5d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="14f5d-103">Обновляет источник данных.</span><span class="sxs-lookup"><span data-stu-id="14f5d-103">Updates a data source.</span></span>

## <span data-ttu-id="14f5d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14f5d-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14f5d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14f5d-105">DESCRIPTION</span></span>
<span data-ttu-id="14f5d-106">Командлет **Set-AzOperationalInsightsDataSource** обновляет источник данных.</span><span class="sxs-lookup"><span data-stu-id="14f5d-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="14f5d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14f5d-107">EXAMPLES</span></span>

## <span data-ttu-id="14f5d-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14f5d-108">PARAMETERS</span></span>

### <span data-ttu-id="14f5d-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="14f5d-109">-DataSource</span></span>
<span data-ttu-id="14f5d-110">Указывает источник данных, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="14f5d-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14f5d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f5d-111">-DefaultProfile</span></span>
<span data-ttu-id="14f5d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="14f5d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14f5d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f5d-113">CommonParameters</span></span>
<span data-ttu-id="14f5d-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14f5d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f5d-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14f5d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f5d-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14f5d-116">INPUTS</span></span>

### <span data-ttu-id="14f5d-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="14f5d-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="14f5d-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14f5d-118">OUTPUTS</span></span>

### <span data-ttu-id="14f5d-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="14f5d-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="14f5d-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="14f5d-120">NOTES</span></span>
* <span data-ttu-id="14f5d-121">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="14f5d-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="14f5d-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14f5d-122">RELATED LINKS</span></span>

[<span data-ttu-id="14f5d-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="14f5d-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="14f5d-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="14f5d-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


