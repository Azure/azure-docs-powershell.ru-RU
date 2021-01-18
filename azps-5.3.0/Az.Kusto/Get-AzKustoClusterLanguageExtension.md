---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 8ad074cf40074032fbab46cab6ee6c6c290eb2ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505132"
---
# <span data-ttu-id="6d87d-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="6d87d-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="6d87d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d87d-102">SYNOPSIS</span></span>
<span data-ttu-id="6d87d-103">Возвращает список языковых расширений, которые можно использовать в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="6d87d-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="6d87d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6d87d-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6d87d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d87d-105">DESCRIPTION</span></span>
<span data-ttu-id="6d87d-106">Возвращает список языковых расширений, которые можно использовать в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="6d87d-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="6d87d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6d87d-107">EXAMPLES</span></span>

### <span data-ttu-id="6d87d-108">Пример 1. Список всех языковых расширений, установленных для кластера</span><span class="sxs-lookup"><span data-stu-id="6d87d-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="6d87d-109">Эта команда возвращает список языковых расширений, которые можно выполнить в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="6d87d-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="6d87d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d87d-110">PARAMETERS</span></span>

### <span data-ttu-id="6d87d-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6d87d-111">-ClusterName</span></span>
<span data-ttu-id="6d87d-112">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="6d87d-112">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d87d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d87d-113">-DefaultProfile</span></span>
<span data-ttu-id="6d87d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d87d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d87d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d87d-115">-ResourceGroupName</span></span>
<span data-ttu-id="6d87d-116">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="6d87d-116">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d87d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d87d-117">-SubscriptionId</span></span>
<span data-ttu-id="6d87d-118">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6d87d-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d87d-119">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="6d87d-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d87d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d87d-120">-Confirm</span></span>
<span data-ttu-id="6d87d-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d87d-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d87d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d87d-122">-WhatIf</span></span>
<span data-ttu-id="6d87d-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d87d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d87d-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6d87d-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d87d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d87d-125">CommonParameters</span></span>
<span data-ttu-id="6d87d-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d87d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d87d-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d87d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d87d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d87d-128">INPUTS</span></span>

## <span data-ttu-id="6d87d-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6d87d-129">OUTPUTS</span></span>

### <span data-ttu-id="6d87d-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="6d87d-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension</span></span>

## <span data-ttu-id="6d87d-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6d87d-131">NOTES</span></span>

<span data-ttu-id="6d87d-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6d87d-132">ALIASES</span></span>

## <span data-ttu-id="6d87d-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d87d-133">RELATED LINKS</span></span>

