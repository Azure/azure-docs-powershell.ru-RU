---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: dd5ca513c327a1ed5d045c3b0283a8b220f6a062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967027"
---
# <span data-ttu-id="27b53-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="27b53-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="27b53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27b53-102">SYNOPSIS</span></span>
<span data-ttu-id="27b53-103">Получите конфигурации помощника Azure для данной подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27b53-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="27b53-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="27b53-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27b53-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27b53-105">DESCRIPTION</span></span>
<span data-ttu-id="27b53-106">Конфигурации, связанные с подпиской, имеют два типа:</span><span class="sxs-lookup"><span data-stu-id="27b53-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="27b53-107">Конфигурация на уровне подписки: для подписки может быть только одна конфигурация этого типа.</span><span class="sxs-lookup"><span data-stu-id="27b53-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="27b53-108">LowCpuThreshold и Exclude являются единственным свойством этого типа конфигурации.</span><span class="sxs-lookup"><span data-stu-id="27b53-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="27b53-109">Конфигурация уровня ResourceGroup: для каждой группы ресурсов в подписке может быть только одна конфигурация.</span><span class="sxs-lookup"><span data-stu-id="27b53-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="27b53-110">Единственным свойством такого типа конфигурации является exclude.</span><span class="sxs-lookup"><span data-stu-id="27b53-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="27b53-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="27b53-111">EXAMPLES</span></span>

### <span data-ttu-id="27b53-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="27b53-112">Example 1</span></span>
```powershell
PS C:\>$data = Get-AzAdvisorConfiguration
Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}-{resourceGroupName}
Name       : {user_subscription}-{resourceGroupName}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

PS C:\>$data[0].Properties
AdditionalProperties :
Exclude              : False
LowCpuThreshold      : 20

PS C:\>$data[1].Properties
AdditionalProperties :
Exclude              : True
LowCpuThreshold      : null

```
<span data-ttu-id="27b53-113">Извлекает список конфигураций помощников Azure.</span><span class="sxs-lookup"><span data-stu-id="27b53-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="27b53-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27b53-114">PARAMETERS</span></span>

### <span data-ttu-id="27b53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b53-115">-DefaultProfile</span></span>
<span data-ttu-id="27b53-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27b53-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27b53-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27b53-117">-ResourceGroupName</span></span>
<span data-ttu-id="27b53-118">Имя конфигурации для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="27b53-118">Resource Group name of the configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b53-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b53-119">CommonParameters</span></span>
<span data-ttu-id="27b53-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27b53-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="27b53-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27b53-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b53-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27b53-122">INPUTS</span></span>

### <span data-ttu-id="27b53-123">Нет</span><span class="sxs-lookup"><span data-stu-id="27b53-123">None</span></span>

## <span data-ttu-id="27b53-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="27b53-124">OUTPUTS</span></span>

### <span data-ttu-id="27b53-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="27b53-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="27b53-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="27b53-126">NOTES</span></span>

## <span data-ttu-id="27b53-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27b53-127">RELATED LINKS</span></span>
