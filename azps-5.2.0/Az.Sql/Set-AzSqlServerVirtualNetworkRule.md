---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 55321b384a24e18a962b99cc40161eabbeb00160
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392500"
---
# <span data-ttu-id="5858c-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5858c-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="5858c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5858c-102">SYNOPSIS</span></span>
<span data-ttu-id="5858c-103">Изменяет конфигурацию правила виртуальной SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="5858c-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="5858c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5858c-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5858c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5858c-105">DESCRIPTION</span></span>
<span data-ttu-id="5858c-106">Эта команда изменяет конфигурацию правила виртуальной сети Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5858c-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="5858c-107">Для управления набором виртуальных правил сети на сервере используйте add-AzSqlServerVirtualNetworkRule и Remove-AzSqlServerVirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="5858c-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="5858c-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5858c-108">EXAMPLES</span></span>

### <span data-ttu-id="5858c-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5858c-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="5858c-110">Изменяет существующее правило виртуальной сети с помощью нового id подсети виртуальной сети, который содержит сведения о новой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5858c-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="5858c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5858c-111">PARAMETERS</span></span>

### <span data-ttu-id="5858c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5858c-112">-AsJob</span></span>
<span data-ttu-id="5858c-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5858c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5858c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5858c-114">-DefaultProfile</span></span>
<span data-ttu-id="5858c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5858c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5858c-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5858c-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="5858c-117">Создайте правило брандмауэра до того, как в виртуальной сети будет включена конечная точка службы VNET.</span><span class="sxs-lookup"><span data-stu-id="5858c-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="5858c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5858c-118">-ResourceGroupName</span></span>
<span data-ttu-id="5858c-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5858c-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="5858c-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5858c-120">-ServerName</span></span>
<span data-ttu-id="5858c-121">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="5858c-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="5858c-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="5858c-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="5858c-123">Имя правила виртуальной сети Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="5858c-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="5858c-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="5858c-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="5858c-125">Виртуальный ИД подсети сети для правила.</span><span class="sxs-lookup"><span data-stu-id="5858c-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="5858c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5858c-126">-Confirm</span></span>
<span data-ttu-id="5858c-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5858c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5858c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5858c-128">-WhatIf</span></span>
<span data-ttu-id="5858c-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5858c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5858c-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5858c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5858c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5858c-131">CommonParameters</span></span>
<span data-ttu-id="5858c-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5858c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5858c-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5858c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5858c-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5858c-134">INPUTS</span></span>

### <span data-ttu-id="5858c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5858c-135">System.String</span></span>

## <span data-ttu-id="5858c-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5858c-136">OUTPUTS</span></span>

### <span data-ttu-id="5858c-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="5858c-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="5858c-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5858c-138">NOTES</span></span>

## <span data-ttu-id="5858c-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5858c-139">RELATED LINKS</span></span>
