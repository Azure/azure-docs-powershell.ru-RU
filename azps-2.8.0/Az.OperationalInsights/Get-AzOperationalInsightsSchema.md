---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 077272f15d37645de86f144424fddd7e5f026908
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913112"
---
# <span data-ttu-id="d4c34-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="d4c34-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="d4c34-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4c34-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c34-103">Возвращает схему, связанную с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="d4c34-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="d4c34-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4c34-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4c34-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4c34-105">DESCRIPTION</span></span>
<span data-ttu-id="d4c34-106">Командлет **Get-AzOperationalInsightsSchema** Возвращает схему, связанную с указанной рабочей областью в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4c34-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="d4c34-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4c34-107">EXAMPLES</span></span>

### <span data-ttu-id="d4c34-108">Пример 1: получение схем для рабочей области</span><span class="sxs-lookup"><span data-stu-id="d4c34-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="d4c34-109">Эта команда получает схемы, связанные с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="d4c34-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="d4c34-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4c34-110">PARAMETERS</span></span>

### <span data-ttu-id="d4c34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c34-111">-DefaultProfile</span></span>
<span data-ttu-id="d4c34-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d4c34-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4c34-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c34-113">-ResourceGroupName</span></span>
<span data-ttu-id="d4c34-114">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="d4c34-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="d4c34-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d4c34-115">-WorkspaceName</span></span>
<span data-ttu-id="d4c34-116">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d4c34-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="d4c34-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c34-117">CommonParameters</span></span>
<span data-ttu-id="d4c34-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4c34-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c34-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4c34-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c34-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4c34-120">INPUTS</span></span>

### <span data-ttu-id="d4c34-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d4c34-121">System.String</span></span>

## <span data-ttu-id="d4c34-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4c34-122">OUTPUTS</span></span>

### <span data-ttu-id="d4c34-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="d4c34-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="d4c34-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4c34-124">NOTES</span></span>

## <span data-ttu-id="d4c34-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4c34-125">RELATED LINKS</span></span>

[<span data-ttu-id="d4c34-126">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="d4c34-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


