---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: b583c8339ebec74fdf8df4116204b7ad5523c258
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997279"
---
# <span data-ttu-id="1b66b-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1b66b-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="1b66b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b66b-102">SYNOPSIS</span></span>
<span data-ttu-id="1b66b-103">Изменяет конфигурацию правила виртуальной сети Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1b66b-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="1b66b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b66b-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b66b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b66b-105">DESCRIPTION</span></span>
<span data-ttu-id="1b66b-106">Эта команда изменяет конфигурацию правила виртуальной сети Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1b66b-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="1b66b-107">Для управления набором виртуальных правил сети на сервере используйте add-AzSqlServerVirtualNetworkRule и Remove-AzSqlServerVirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="1b66b-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="1b66b-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b66b-108">EXAMPLES</span></span>

### <span data-ttu-id="1b66b-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1b66b-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="1b66b-110">Изменяет существующее правило виртуальной сети с помощью нового id виртуальной сети подсети, который содержит сведения о новой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1b66b-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="1b66b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b66b-111">PARAMETERS</span></span>

### <span data-ttu-id="1b66b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b66b-112">-AsJob</span></span>
<span data-ttu-id="1b66b-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1b66b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b66b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b66b-114">-DefaultProfile</span></span>
<span data-ttu-id="1b66b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1b66b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b66b-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1b66b-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="1b66b-117">Создайте правило брандмауэра, прежде чем в виртуальной сети будет включена конечная точка службы VNET.</span><span class="sxs-lookup"><span data-stu-id="1b66b-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="1b66b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b66b-118">-ResourceGroupName</span></span>
<span data-ttu-id="1b66b-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b66b-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="1b66b-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1b66b-120">-ServerName</span></span>
<span data-ttu-id="1b66b-121">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="1b66b-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="1b66b-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="1b66b-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="1b66b-123">Имя правила виртуальной сети Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="1b66b-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="1b66b-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="1b66b-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="1b66b-125">Виртуальный ИД подсети сети для правила.</span><span class="sxs-lookup"><span data-stu-id="1b66b-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="1b66b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b66b-126">-Confirm</span></span>
<span data-ttu-id="1b66b-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1b66b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b66b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b66b-128">-WhatIf</span></span>
<span data-ttu-id="1b66b-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b66b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b66b-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1b66b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b66b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b66b-131">CommonParameters</span></span>
<span data-ttu-id="1b66b-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b66b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b66b-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b66b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b66b-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b66b-134">INPUTS</span></span>

### <span data-ttu-id="1b66b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1b66b-135">System.String</span></span>

## <span data-ttu-id="1b66b-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b66b-136">OUTPUTS</span></span>

### <span data-ttu-id="1b66b-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="1b66b-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="1b66b-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b66b-138">NOTES</span></span>

## <span data-ttu-id="1b66b-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b66b-139">RELATED LINKS</span></span>
