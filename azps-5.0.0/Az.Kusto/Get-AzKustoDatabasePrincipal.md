---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c9b25327d170d05a4c2ad97b3cb7ce7626fbfec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249012"
---
# <span data-ttu-id="27ecb-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="27ecb-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="27ecb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="27ecb-103">Возвращает список участников базы данных для заданного кластера Kusto и базы данных.</span><span class="sxs-lookup"><span data-stu-id="27ecb-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="27ecb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27ecb-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="27ecb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27ecb-105">DESCRIPTION</span></span>
<span data-ttu-id="27ecb-106">Возвращает список участников базы данных для заданного кластера Kusto и базы данных.</span><span class="sxs-lookup"><span data-stu-id="27ecb-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="27ecb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27ecb-107">EXAMPLES</span></span>

### <span data-ttu-id="27ecb-108">Пример 1: список участников базы данных, указанных в кластере и базе данных Kusto</span><span class="sxs-lookup"><span data-stu-id="27ecb-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="27ecb-109">Вышеприведенная команда возвращает список участников базы данных, указанных в кластере и базе данных Kusto.</span><span class="sxs-lookup"><span data-stu-id="27ecb-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="27ecb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27ecb-110">PARAMETERS</span></span>

### <span data-ttu-id="27ecb-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="27ecb-111">-ClusterName</span></span>
<span data-ttu-id="27ecb-112">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="27ecb-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="27ecb-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="27ecb-113">-DatabaseName</span></span>
<span data-ttu-id="27ecb-114">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="27ecb-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="27ecb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ecb-115">-DefaultProfile</span></span>
<span data-ttu-id="27ecb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27ecb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27ecb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ecb-117">-ResourceGroupName</span></span>
<span data-ttu-id="27ecb-118">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="27ecb-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="27ecb-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27ecb-119">-SubscriptionId</span></span>
<span data-ttu-id="27ecb-120">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="27ecb-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="27ecb-121">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="27ecb-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="27ecb-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27ecb-122">-Confirm</span></span>
<span data-ttu-id="27ecb-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27ecb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27ecb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27ecb-124">-WhatIf</span></span>
<span data-ttu-id="27ecb-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="27ecb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27ecb-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="27ecb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27ecb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ecb-127">CommonParameters</span></span>
<span data-ttu-id="27ecb-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27ecb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ecb-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27ecb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ecb-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27ecb-130">INPUTS</span></span>

## <span data-ttu-id="27ecb-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27ecb-131">OUTPUTS</span></span>

### <span data-ttu-id="27ecb-132">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="27ecb-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="27ecb-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="27ecb-133">NOTES</span></span>

<span data-ttu-id="27ecb-134">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="27ecb-134">ALIASES</span></span>

## <span data-ttu-id="27ecb-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27ecb-135">RELATED LINKS</span></span>

