---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: f33d644e9726d09f9f2314e74a6b5fb80b788952
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079969"
---
# <span data-ttu-id="44faa-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="44faa-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="44faa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44faa-102">SYNOPSIS</span></span>
<span data-ttu-id="44faa-103">Возвращает список расширений языка, которые могут выполняться в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="44faa-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="44faa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44faa-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44faa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44faa-105">DESCRIPTION</span></span>
<span data-ttu-id="44faa-106">Возвращает список расширений языка, которые могут выполняться в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="44faa-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="44faa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44faa-107">EXAMPLES</span></span>

### <span data-ttu-id="44faa-108">Пример 1: список всех расширений языка, заданных для кластера</span><span class="sxs-lookup"><span data-stu-id="44faa-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="44faa-109">Приведенная выше команда возвращает список расширений языка, которые могут выполняться в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="44faa-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="44faa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44faa-110">PARAMETERS</span></span>

### <span data-ttu-id="44faa-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="44faa-111">-ClusterName</span></span>
<span data-ttu-id="44faa-112">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="44faa-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="44faa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44faa-113">-DefaultProfile</span></span>
<span data-ttu-id="44faa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44faa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44faa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44faa-115">-ResourceGroupName</span></span>
<span data-ttu-id="44faa-116">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="44faa-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="44faa-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44faa-117">-SubscriptionId</span></span>
<span data-ttu-id="44faa-118">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="44faa-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="44faa-119">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="44faa-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="44faa-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44faa-120">-Confirm</span></span>
<span data-ttu-id="44faa-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="44faa-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44faa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44faa-122">-WhatIf</span></span>
<span data-ttu-id="44faa-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="44faa-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44faa-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="44faa-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44faa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44faa-125">CommonParameters</span></span>
<span data-ttu-id="44faa-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44faa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44faa-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44faa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44faa-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44faa-128">INPUTS</span></span>

## <span data-ttu-id="44faa-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44faa-129">OUTPUTS</span></span>

### <span data-ttu-id="44faa-130">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="44faa-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span></span>

## <span data-ttu-id="44faa-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="44faa-131">NOTES</span></span>

<span data-ttu-id="44faa-132">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="44faa-132">ALIASES</span></span>

## <span data-ttu-id="44faa-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44faa-133">RELATED LINKS</span></span>
