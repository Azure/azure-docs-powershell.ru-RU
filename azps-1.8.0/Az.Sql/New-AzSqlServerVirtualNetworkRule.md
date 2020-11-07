---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8667de4551e9fc0c4baf623099f70f778ec8f0a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728877"
---
# <span data-ttu-id="5ef66-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5ef66-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="5ef66-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ef66-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef66-103">Создание правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5ef66-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="5ef66-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ef66-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ef66-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ef66-105">DESCRIPTION</span></span>
<span data-ttu-id="5ef66-106">Создание правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5ef66-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="5ef66-107">Правила виртуальной сети используются для подключения сервера Azure SQL Server к определенной виртуальной сети, чтобы ограничить доступ к серверу Azure SQL Server только в пределах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5ef66-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="5ef66-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ef66-108">EXAMPLES</span></span>

### <span data-ttu-id="5ef66-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5ef66-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="5ef66-110">Создание правила виртуальной сети для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="5ef66-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="5ef66-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ef66-111">PARAMETERS</span></span>

### <span data-ttu-id="5ef66-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ef66-112">-AsJob</span></span>
<span data-ttu-id="5ef66-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5ef66-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef66-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef66-114">-DefaultProfile</span></span>
<span data-ttu-id="5ef66-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ef66-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ef66-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ef66-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="5ef66-117">Создайте правило брандмауэра, прежде чем в виртуальной сети будет включена конечная точка службы виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="5ef66-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef66-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ef66-118">-ResourceGroupName</span></span>
<span data-ttu-id="5ef66-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ef66-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="5ef66-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5ef66-120">-ServerName</span></span>
<span data-ttu-id="5ef66-121">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5ef66-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="5ef66-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="5ef66-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="5ef66-123">Имя правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5ef66-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="5ef66-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="5ef66-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="5ef66-125">Идентификатор подсети виртуальной сети, указывающий сведения о Microsoft. Network</span><span class="sxs-lookup"><span data-stu-id="5ef66-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="5ef66-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ef66-126">-Confirm</span></span>
<span data-ttu-id="5ef66-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ef66-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ef66-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ef66-128">-WhatIf</span></span>
<span data-ttu-id="5ef66-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ef66-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ef66-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ef66-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ef66-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef66-131">CommonParameters</span></span>
<span data-ttu-id="5ef66-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ef66-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef66-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ef66-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef66-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ef66-134">INPUTS</span></span>

### <span data-ttu-id="5ef66-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5ef66-135">System.String</span></span>

## <span data-ttu-id="5ef66-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ef66-136">OUTPUTS</span></span>

### <span data-ttu-id="5ef66-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="5ef66-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="5ef66-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ef66-138">NOTES</span></span>

## <span data-ttu-id="5ef66-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ef66-139">RELATED LINKS</span></span>
