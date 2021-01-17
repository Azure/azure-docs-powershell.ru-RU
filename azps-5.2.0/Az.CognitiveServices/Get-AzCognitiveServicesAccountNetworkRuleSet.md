---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416036"
---
# <span data-ttu-id="35ef7-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="35ef7-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="35ef7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35ef7-102">SYNOPSIS</span></span>
<span data-ttu-id="35ef7-103">Получить свойство NetworkRule учетной записи "Когнитивные услуги"</span><span class="sxs-lookup"><span data-stu-id="35ef7-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="35ef7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35ef7-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35ef7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35ef7-105">DESCRIPTION</span></span>
<span data-ttu-id="35ef7-106">Командлет **Get-AzCognitiveServicesAccountNetworkRuleSet** получает свойство NetworkRule учетной записи Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="35ef7-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="35ef7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35ef7-107">EXAMPLES</span></span>

### <span data-ttu-id="35ef7-108">Пример 1. Получить свойство NetworkRule указанной учетной записи Службы восприятия</span><span class="sxs-lookup"><span data-stu-id="35ef7-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="35ef7-109">Эта команда получает свойство NetworkRule указанной учетной записи Службы восприятия</span><span class="sxs-lookup"><span data-stu-id="35ef7-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="35ef7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35ef7-110">PARAMETERS</span></span>

### <span data-ttu-id="35ef7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ef7-111">-DefaultProfile</span></span>
<span data-ttu-id="35ef7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35ef7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35ef7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="35ef7-113">-Name</span></span>
<span data-ttu-id="35ef7-114">Имя учетной записи службы восприятия.</span><span class="sxs-lookup"><span data-stu-id="35ef7-114">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35ef7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ef7-115">-ResourceGroupName</span></span>
<span data-ttu-id="35ef7-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35ef7-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="35ef7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ef7-117">CommonParameters</span></span>
<span data-ttu-id="35ef7-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ef7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ef7-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35ef7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ef7-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35ef7-120">INPUTS</span></span>

### <span data-ttu-id="35ef7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="35ef7-121">System.String</span></span>

## <span data-ttu-id="35ef7-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35ef7-122">OUTPUTS</span></span>

### <span data-ttu-id="35ef7-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="35ef7-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="35ef7-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35ef7-124">NOTES</span></span>

## <span data-ttu-id="35ef7-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35ef7-125">RELATED LINKS</span></span>
