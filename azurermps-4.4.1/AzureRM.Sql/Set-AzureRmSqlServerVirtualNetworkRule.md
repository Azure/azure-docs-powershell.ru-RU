---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 355b8fdffd5d1e9e16fe9bfaf504d627a8b9b167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735028"
---
# <span data-ttu-id="b2568-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b2568-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="b2568-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2568-102">SYNOPSIS</span></span>
<span data-ttu-id="b2568-103">Изменение конфигурации правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b2568-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2568-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2568-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2568-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2568-105">DESCRIPTION</span></span>
<span data-ttu-id="b2568-106">Эта команда изменяет конфигурацию правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b2568-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>


<span data-ttu-id="b2568-107">Чтобы управлять набором правил виртуальных сетей на сервере, используйте вместо этого "Add-AzureRmSqlServerVirtualNetworkRule" и "Remove-AzureRmSqlServerVirtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="b2568-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="b2568-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2568-108">EXAMPLES</span></span>

### <span data-ttu-id="b2568-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b2568-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="b2568-110">Изменение существующего правила виртуальной сети с помощью нового идентификатора подсети виртуальной сети, содержащего сведения о новой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b2568-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="b2568-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2568-111">PARAMETERS</span></span>

### <span data-ttu-id="b2568-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2568-112">-ResourceGroupName</span></span>
<span data-ttu-id="b2568-113">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2568-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="b2568-114">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b2568-114">-ServerName</span></span>
<span data-ttu-id="b2568-115">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b2568-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b2568-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="b2568-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="b2568-117">Имя правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b2568-117">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="b2568-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="b2568-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="b2568-119">Идентификатор подсети виртуальной сети для правила.</span><span class="sxs-lookup"><span data-stu-id="b2568-119">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="b2568-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2568-120">-Confirm</span></span>
<span data-ttu-id="b2568-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b2568-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2568-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2568-122">-WhatIf</span></span>
<span data-ttu-id="b2568-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b2568-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2568-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b2568-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2568-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2568-125">-DefaultProfile</span></span>
<span data-ttu-id="b2568-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2568-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2568-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2568-127">CommonParameters</span></span>
<span data-ttu-id="b2568-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2568-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2568-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2568-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2568-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2568-130">INPUTS</span></span>

### <span data-ttu-id="b2568-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b2568-131">System.String</span></span>

## <span data-ttu-id="b2568-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2568-132">OUTPUTS</span></span>

### <span data-ttu-id="b2568-133">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="b2568-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="b2568-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2568-134">NOTES</span></span>

## <span data-ttu-id="b2568-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2568-135">RELATED LINKS</span></span>

