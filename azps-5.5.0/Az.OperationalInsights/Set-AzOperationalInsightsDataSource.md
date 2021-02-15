---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218124"
---
# <span data-ttu-id="8950c-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="8950c-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="8950c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8950c-102">SYNOPSIS</span></span>
<span data-ttu-id="8950c-103">Обновляет источник данных.</span><span class="sxs-lookup"><span data-stu-id="8950c-103">Updates a data source.</span></span>

## <span data-ttu-id="8950c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8950c-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8950c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8950c-105">DESCRIPTION</span></span>
<span data-ttu-id="8950c-106">**Cmdlet Set-AzOperationalInsightsDataSource** обновляет источник данных.</span><span class="sxs-lookup"><span data-stu-id="8950c-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="8950c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8950c-107">EXAMPLES</span></span>

## <span data-ttu-id="8950c-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8950c-108">PARAMETERS</span></span>

### <span data-ttu-id="8950c-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="8950c-109">-DataSource</span></span>
<span data-ttu-id="8950c-110">Источник данных, который обновляется этим cmdletом.</span><span class="sxs-lookup"><span data-stu-id="8950c-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="8950c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8950c-111">-DefaultProfile</span></span>
<span data-ttu-id="8950c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8950c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8950c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8950c-113">CommonParameters</span></span>
<span data-ttu-id="8950c-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8950c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8950c-115">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8950c-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8950c-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8950c-116">INPUTS</span></span>

### <span data-ttu-id="8950c-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="8950c-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="8950c-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8950c-118">OUTPUTS</span></span>

### <span data-ttu-id="8950c-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="8950c-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="8950c-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8950c-120">NOTES</span></span>
* <span data-ttu-id="8950c-121">Ключевые слова: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="8950c-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="8950c-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8950c-122">RELATED LINKS</span></span>

[<span data-ttu-id="8950c-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="8950c-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="8950c-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="8950c-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


