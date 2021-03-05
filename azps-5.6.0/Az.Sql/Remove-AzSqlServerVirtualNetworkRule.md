---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 766a5bb6777d1c1ef1e077d4345b7034ede82599
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995151"
---
# <span data-ttu-id="2a23a-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2a23a-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="2a23a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a23a-102">SYNOPSIS</span></span>
<span data-ttu-id="2a23a-103">Удаляет правило виртуальной SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="2a23a-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="2a23a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a23a-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a23a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a23a-105">DESCRIPTION</span></span>
<span data-ttu-id="2a23a-106">Эта команда удаляет правило виртуальной SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="2a23a-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="2a23a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a23a-107">EXAMPLES</span></span>

### <span data-ttu-id="2a23a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a23a-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="2a23a-109">Удаление существующего правила виртуальной SQL Server Azure</span><span class="sxs-lookup"><span data-stu-id="2a23a-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="2a23a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a23a-110">PARAMETERS</span></span>

### <span data-ttu-id="2a23a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a23a-111">-AsJob</span></span>
<span data-ttu-id="2a23a-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2a23a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a23a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a23a-113">-DefaultProfile</span></span>
<span data-ttu-id="2a23a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2a23a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a23a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a23a-115">-ResourceGroupName</span></span>
<span data-ttu-id="2a23a-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a23a-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="2a23a-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2a23a-117">-ServerName</span></span>
<span data-ttu-id="2a23a-118">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="2a23a-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="2a23a-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="2a23a-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="2a23a-120">Имя виртуального правила сети Azure Sql Server</span><span class="sxs-lookup"><span data-stu-id="2a23a-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="2a23a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a23a-121">-Confirm</span></span>
<span data-ttu-id="2a23a-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2a23a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a23a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a23a-123">-WhatIf</span></span>
<span data-ttu-id="2a23a-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a23a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a23a-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a23a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a23a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a23a-126">CommonParameters</span></span>
<span data-ttu-id="2a23a-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a23a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a23a-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a23a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a23a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a23a-129">INPUTS</span></span>

### <span data-ttu-id="2a23a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2a23a-130">System.String</span></span>

## <span data-ttu-id="2a23a-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a23a-131">OUTPUTS</span></span>

### <span data-ttu-id="2a23a-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="2a23a-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="2a23a-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a23a-133">NOTES</span></span>

## <span data-ttu-id="2a23a-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a23a-134">RELATED LINKS</span></span>
