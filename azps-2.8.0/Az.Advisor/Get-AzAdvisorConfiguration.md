---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: d17384b47e4a722631b5d3003bdb4b7eb430836d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728214"
---
# <span data-ttu-id="3151d-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="3151d-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="3151d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3151d-102">SYNOPSIS</span></span>
<span data-ttu-id="3151d-103">Получение конфигураций консультанта Azure для заданной подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3151d-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="3151d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3151d-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3151d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3151d-105">DESCRIPTION</span></span>
<span data-ttu-id="3151d-106">Конфигурации, связанные с подпиской, имеют два типа.</span><span class="sxs-lookup"><span data-stu-id="3151d-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="3151d-107">Настройка уровня подписки: для подписки может быть только одна конфигурация этого типа.</span><span class="sxs-lookup"><span data-stu-id="3151d-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="3151d-108">LowCpuThreshold и Exclude являются единственным свойством данного типа конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3151d-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="3151d-109">Конфигурация уровня ResourceGroup: в подписке может быть только одна конфигурация для каждой из ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3151d-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="3151d-110">"Исключить" является единственным свойством этого типа конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3151d-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="3151d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3151d-111">EXAMPLES</span></span>

### <span data-ttu-id="3151d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3151d-112">Example 1</span></span>
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
<span data-ttu-id="3151d-113">Извлекает список конфигураций Advisor (-ов) для Azure.</span><span class="sxs-lookup"><span data-stu-id="3151d-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="3151d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3151d-114">PARAMETERS</span></span>

### <span data-ttu-id="3151d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3151d-115">-DefaultProfile</span></span>
<span data-ttu-id="3151d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3151d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3151d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3151d-117">-ResourceGroupName</span></span>
<span data-ttu-id="3151d-118">Имя группы ресурсов конфигурации</span><span class="sxs-lookup"><span data-stu-id="3151d-118">Resource Group name of the configuration</span></span>

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

### <span data-ttu-id="3151d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3151d-119">CommonParameters</span></span>
<span data-ttu-id="3151d-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3151d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3151d-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3151d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3151d-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3151d-122">INPUTS</span></span>

### <span data-ttu-id="3151d-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="3151d-123">None</span></span>

## <span data-ttu-id="3151d-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3151d-124">OUTPUTS</span></span>

### <span data-ttu-id="3151d-125">Microsoft. Azure. Commands. Advisor. командлеты. Models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="3151d-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="3151d-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="3151d-126">NOTES</span></span>

## <span data-ttu-id="3151d-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3151d-127">RELATED LINKS</span></span>
