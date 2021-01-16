---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c9b25327d170d05a4c2ad97b3cb7ce7626fbfec9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403983"
---
# <span data-ttu-id="f8218-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="f8218-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="f8218-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8218-102">SYNOPSIS</span></span>
<span data-ttu-id="f8218-103">Возвращает список основной базы данных для кластера и базы данных "Кузто".</span><span class="sxs-lookup"><span data-stu-id="f8218-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="f8218-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f8218-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f8218-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8218-105">DESCRIPTION</span></span>
<span data-ttu-id="f8218-106">Возвращает список основной базы данных для кластера и базы данных Кусто.</span><span class="sxs-lookup"><span data-stu-id="f8218-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="f8218-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f8218-107">EXAMPLES</span></span>

### <span data-ttu-id="f8218-108">Пример 1. Список глав баз данных для кластера и базы данных "Кузто"</span><span class="sxs-lookup"><span data-stu-id="f8218-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="f8218-109">Вышеуказанная команда возвращает список основной базы данных для данного кластера и базы данных "Кузто".</span><span class="sxs-lookup"><span data-stu-id="f8218-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="f8218-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8218-110">PARAMETERS</span></span>

### <span data-ttu-id="f8218-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f8218-111">-ClusterName</span></span>
<span data-ttu-id="f8218-112">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="f8218-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f8218-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f8218-113">-DatabaseName</span></span>
<span data-ttu-id="f8218-114">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="f8218-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f8218-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8218-115">-DefaultProfile</span></span>
<span data-ttu-id="f8218-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8218-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8218-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8218-117">-ResourceGroupName</span></span>
<span data-ttu-id="f8218-118">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="f8218-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f8218-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8218-119">-SubscriptionId</span></span>
<span data-ttu-id="f8218-120">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f8218-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f8218-121">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="f8218-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f8218-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8218-122">-Confirm</span></span>
<span data-ttu-id="f8218-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8218-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8218-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8218-124">-WhatIf</span></span>
<span data-ttu-id="f8218-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8218-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8218-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f8218-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8218-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8218-127">CommonParameters</span></span>
<span data-ttu-id="f8218-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8218-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8218-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8218-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8218-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8218-130">INPUTS</span></span>

## <span data-ttu-id="f8218-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8218-131">OUTPUTS</span></span>

### <span data-ttu-id="f8218-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="f8218-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="f8218-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f8218-133">NOTES</span></span>

<span data-ttu-id="f8218-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f8218-134">ALIASES</span></span>

## <span data-ttu-id="f8218-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8218-135">RELATED LINKS</span></span>

