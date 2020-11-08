---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080233"
---
# <span data-ttu-id="9df38-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9df38-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="9df38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9df38-102">SYNOPSIS</span></span>
<span data-ttu-id="9df38-103">Удаляет правило виртуальной сети Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9df38-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="9df38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9df38-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9df38-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9df38-105">DESCRIPTION</span></span>
<span data-ttu-id="9df38-106">Эта команда удаляет правило виртуальной сети Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9df38-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="9df38-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9df38-107">EXAMPLES</span></span>

### <span data-ttu-id="9df38-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9df38-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="9df38-109">Удаление существующего правила виртуальной сети SQL Server для Azure</span><span class="sxs-lookup"><span data-stu-id="9df38-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="9df38-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9df38-110">PARAMETERS</span></span>

### <span data-ttu-id="9df38-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9df38-111">-AsJob</span></span>
<span data-ttu-id="9df38-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9df38-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9df38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9df38-113">-DefaultProfile</span></span>
<span data-ttu-id="9df38-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9df38-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9df38-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9df38-115">-ResourceGroupName</span></span>
<span data-ttu-id="9df38-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9df38-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="9df38-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9df38-117">-ServerName</span></span>
<span data-ttu-id="9df38-118">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9df38-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="9df38-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="9df38-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="9df38-120">Имя правила виртуальной сети для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="9df38-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="9df38-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9df38-121">-Confirm</span></span>
<span data-ttu-id="9df38-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9df38-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9df38-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9df38-123">-WhatIf</span></span>
<span data-ttu-id="9df38-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9df38-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9df38-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9df38-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9df38-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df38-126">CommonParameters</span></span>
<span data-ttu-id="9df38-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9df38-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df38-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9df38-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df38-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9df38-129">INPUTS</span></span>

### <span data-ttu-id="9df38-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9df38-130">System.String</span></span>

## <span data-ttu-id="9df38-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9df38-131">OUTPUTS</span></span>

### <span data-ttu-id="9df38-132">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="9df38-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="9df38-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="9df38-133">NOTES</span></span>

## <span data-ttu-id="9df38-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9df38-134">RELATED LINKS</span></span>
