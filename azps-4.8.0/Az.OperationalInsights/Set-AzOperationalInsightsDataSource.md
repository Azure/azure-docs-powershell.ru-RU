---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079407"
---
# <span data-ttu-id="873a5-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="873a5-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="873a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="873a5-102">SYNOPSIS</span></span>
<span data-ttu-id="873a5-103">Обновляет источник данных.</span><span class="sxs-lookup"><span data-stu-id="873a5-103">Updates a data source.</span></span>

## <span data-ttu-id="873a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="873a5-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="873a5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="873a5-105">DESCRIPTION</span></span>
<span data-ttu-id="873a5-106">Командлет **Set-AzOperationalInsightsDataSource** обновляет источник данных.</span><span class="sxs-lookup"><span data-stu-id="873a5-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="873a5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="873a5-107">EXAMPLES</span></span>

## <span data-ttu-id="873a5-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="873a5-108">PARAMETERS</span></span>

### <span data-ttu-id="873a5-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="873a5-109">-DataSource</span></span>
<span data-ttu-id="873a5-110">Указывает источник данных, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="873a5-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="873a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="873a5-111">-DefaultProfile</span></span>
<span data-ttu-id="873a5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="873a5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="873a5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="873a5-113">CommonParameters</span></span>
<span data-ttu-id="873a5-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="873a5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="873a5-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="873a5-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="873a5-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="873a5-116">INPUTS</span></span>

### <span data-ttu-id="873a5-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="873a5-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="873a5-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="873a5-118">OUTPUTS</span></span>

### <span data-ttu-id="873a5-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="873a5-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="873a5-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="873a5-120">NOTES</span></span>
* <span data-ttu-id="873a5-121">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="873a5-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="873a5-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="873a5-122">RELATED LINKS</span></span>

[<span data-ttu-id="873a5-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="873a5-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="873a5-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="873a5-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


