---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248412"
---
# <span data-ttu-id="d5a23-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d5a23-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="d5a23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5a23-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a23-103">Получение свойства NetworkRule учетной записи службы для персонализированных служб</span><span class="sxs-lookup"><span data-stu-id="d5a23-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="d5a23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5a23-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5a23-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5a23-105">DESCRIPTION</span></span>
<span data-ttu-id="d5a23-106">Командлет **Get-AzCognitiveServicesAccountNetworkRuleSet** получает свойство NetworkRule учетной записи службы для персонализированных служб.</span><span class="sxs-lookup"><span data-stu-id="d5a23-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="d5a23-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5a23-107">EXAMPLES</span></span>

### <span data-ttu-id="d5a23-108">Пример 1: получение свойства NetworkRule для указанной учетной записи самообслуживания</span><span class="sxs-lookup"><span data-stu-id="d5a23-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="d5a23-109">Эта команда получает свойство NetworkRule для указанной учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="d5a23-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="d5a23-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5a23-110">PARAMETERS</span></span>

### <span data-ttu-id="d5a23-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a23-111">-DefaultProfile</span></span>
<span data-ttu-id="d5a23-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a23-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5a23-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5a23-113">-Name</span></span>
<span data-ttu-id="d5a23-114">Имя учетной записи для самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="d5a23-114">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="d5a23-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a23-115">-ResourceGroupName</span></span>
<span data-ttu-id="d5a23-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5a23-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="d5a23-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a23-117">CommonParameters</span></span>
<span data-ttu-id="d5a23-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5a23-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a23-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5a23-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a23-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5a23-120">INPUTS</span></span>

### <span data-ttu-id="d5a23-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d5a23-121">System.String</span></span>

## <span data-ttu-id="d5a23-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5a23-122">OUTPUTS</span></span>

### <span data-ttu-id="d5a23-123">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d5a23-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="d5a23-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5a23-124">NOTES</span></span>

## <span data-ttu-id="d5a23-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5a23-125">RELATED LINKS</span></span>
