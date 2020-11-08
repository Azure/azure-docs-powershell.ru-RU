---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 55321b384a24e18a962b99cc40161eabbeb00160
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245180"
---
# <span data-ttu-id="19e24-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="19e24-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="19e24-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19e24-102">SYNOPSIS</span></span>
<span data-ttu-id="19e24-103">Изменение конфигурации правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="19e24-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="19e24-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19e24-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19e24-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19e24-105">DESCRIPTION</span></span>
<span data-ttu-id="19e24-106">Эта команда изменяет конфигурацию правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="19e24-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="19e24-107">Чтобы управлять набором правил виртуальных сетей на сервере, используйте вместо этого "Add-AzSqlServerVirtualNetworkRule" и "Remove-AzSqlServerVirtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="19e24-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="19e24-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19e24-108">EXAMPLES</span></span>

### <span data-ttu-id="19e24-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="19e24-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="19e24-110">Изменение существующего правила виртуальной сети с помощью нового идентификатора подсети виртуальной сети, содержащего сведения о новой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="19e24-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="19e24-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19e24-111">PARAMETERS</span></span>

### <span data-ttu-id="19e24-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19e24-112">-AsJob</span></span>
<span data-ttu-id="19e24-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="19e24-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19e24-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e24-114">-DefaultProfile</span></span>
<span data-ttu-id="19e24-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="19e24-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19e24-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="19e24-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="19e24-117">Создайте правило брандмауэра, прежде чем в виртуальной сети будет включена конечная точка службы виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="19e24-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="19e24-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19e24-118">-ResourceGroupName</span></span>
<span data-ttu-id="19e24-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19e24-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="19e24-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="19e24-120">-ServerName</span></span>
<span data-ttu-id="19e24-121">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="19e24-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="19e24-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="19e24-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="19e24-123">Имя правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="19e24-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="19e24-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="19e24-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="19e24-125">Идентификатор подсети виртуальной сети для правила.</span><span class="sxs-lookup"><span data-stu-id="19e24-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="19e24-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19e24-126">-Confirm</span></span>
<span data-ttu-id="19e24-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19e24-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19e24-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19e24-128">-WhatIf</span></span>
<span data-ttu-id="19e24-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19e24-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19e24-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19e24-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19e24-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e24-131">CommonParameters</span></span>
<span data-ttu-id="19e24-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19e24-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e24-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19e24-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e24-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19e24-134">INPUTS</span></span>

### <span data-ttu-id="19e24-135">System. String</span><span class="sxs-lookup"><span data-stu-id="19e24-135">System.String</span></span>

## <span data-ttu-id="19e24-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19e24-136">OUTPUTS</span></span>

### <span data-ttu-id="19e24-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="19e24-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="19e24-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="19e24-138">NOTES</span></span>

## <span data-ttu-id="19e24-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19e24-139">RELATED LINKS</span></span>
