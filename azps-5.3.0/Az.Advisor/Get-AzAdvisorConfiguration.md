---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: 1e2f1daa222714c23f394d362222f9ef1fd1bde4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506999"
---
# <span data-ttu-id="80b71-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="80b71-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="80b71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80b71-102">SYNOPSIS</span></span>
<span data-ttu-id="80b71-103">Получите конфигурации помощника Azure для данной подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80b71-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="80b71-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="80b71-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80b71-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80b71-105">DESCRIPTION</span></span>
<span data-ttu-id="80b71-106">Конфигурации, связанные с подпиской, имеют два типа:</span><span class="sxs-lookup"><span data-stu-id="80b71-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="80b71-107">Конфигурация на уровне подписки: для подписки может быть только одна конфигурация этого типа.</span><span class="sxs-lookup"><span data-stu-id="80b71-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="80b71-108">LowCpuThreshold и Exclude являются единственным свойством этого типа конфигурации.</span><span class="sxs-lookup"><span data-stu-id="80b71-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="80b71-109">Настройка уровня resourceGroup: для каждой группы ресурсов в подписке может быть только одна конфигурация.</span><span class="sxs-lookup"><span data-stu-id="80b71-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="80b71-110">Единственным свойством такого типа конфигурации является exclude.</span><span class="sxs-lookup"><span data-stu-id="80b71-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="80b71-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="80b71-111">EXAMPLES</span></span>

### <span data-ttu-id="80b71-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="80b71-112">Example 1</span></span>
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
<span data-ttu-id="80b71-113">Извлекает список конфигураций помощников Azure.</span><span class="sxs-lookup"><span data-stu-id="80b71-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="80b71-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80b71-114">PARAMETERS</span></span>

### <span data-ttu-id="80b71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b71-115">-DefaultProfile</span></span>
<span data-ttu-id="80b71-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80b71-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80b71-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b71-117">-ResourceGroupName</span></span>
<span data-ttu-id="80b71-118">Имя конфигурации для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="80b71-118">Resource Group name of the configuration</span></span>

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

### <span data-ttu-id="80b71-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b71-119">CommonParameters</span></span>
<span data-ttu-id="80b71-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b71-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="80b71-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80b71-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b71-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80b71-122">INPUTS</span></span>

### <span data-ttu-id="80b71-123">Нет</span><span class="sxs-lookup"><span data-stu-id="80b71-123">None</span></span>

## <span data-ttu-id="80b71-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="80b71-124">OUTPUTS</span></span>

### <span data-ttu-id="80b71-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="80b71-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="80b71-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="80b71-126">NOTES</span></span>

## <span data-ttu-id="80b71-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80b71-127">RELATED LINKS</span></span>
