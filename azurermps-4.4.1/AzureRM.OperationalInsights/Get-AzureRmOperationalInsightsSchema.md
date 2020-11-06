---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
ms.openlocfilehash: a4e4f1d86822a6c4ecd793576b1a5b68f2b2534f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565207"
---
# <span data-ttu-id="3c307-101">Get-AzureRmOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="3c307-101">Get-AzureRmOperationalInsightsSchema</span></span>

## <span data-ttu-id="3c307-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c307-102">SYNOPSIS</span></span>
<span data-ttu-id="3c307-103">Возвращает схему, связанную с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="3c307-103">Returns the schema associated with a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c307-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c307-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c307-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c307-105">DESCRIPTION</span></span>
<span data-ttu-id="3c307-106">Командлет **Get-AzureRmOperationalInsightsSchema** Возвращает схему, связанную с указанной рабочей областью в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3c307-106">The **Get-AzureRmOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="3c307-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c307-107">EXAMPLES</span></span>

### <span data-ttu-id="3c307-108">Пример 1: получение схем для рабочей области</span><span class="sxs-lookup"><span data-stu-id="3c307-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="3c307-109">Эта команда получает схемы, связанные с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="3c307-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="3c307-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c307-110">PARAMETERS</span></span>

### <span data-ttu-id="3c307-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c307-111">-ResourceGroupName</span></span>
<span data-ttu-id="3c307-112">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="3c307-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="3c307-113">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3c307-113">-WorkspaceName</span></span>
<span data-ttu-id="3c307-114">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3c307-114">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="3c307-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c307-115">-DefaultProfile</span></span>
<span data-ttu-id="3c307-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c307-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c307-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c307-117">CommonParameters</span></span>
<span data-ttu-id="3c307-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c307-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c307-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c307-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c307-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c307-120">INPUTS</span></span>

## <span data-ttu-id="3c307-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c307-121">OUTPUTS</span></span>

### <span data-ttu-id="3c307-122">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="3c307-122">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="3c307-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c307-123">NOTES</span></span>

## <span data-ttu-id="3c307-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c307-124">RELATED LINKS</span></span>

[<span data-ttu-id="3c307-125">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="3c307-125">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


