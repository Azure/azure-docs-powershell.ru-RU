---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 2955834fdb5c902b7495fe212cb9e697b0cee940
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732828"
---
# <span data-ttu-id="9e415-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9e415-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="9e415-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e415-102">SYNOPSIS</span></span>
<span data-ttu-id="9e415-103">Создание правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9e415-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e415-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e415-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e415-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e415-105">DESCRIPTION</span></span>
<span data-ttu-id="9e415-106">Создание правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9e415-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="9e415-107">Правила виртуальной сети используются для подключения сервера Azure SQL Server к определенной виртуальной сети, чтобы ограничить доступ к серверу Azure SQL Server только в пределах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9e415-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="9e415-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e415-108">EXAMPLES</span></span>

### <span data-ttu-id="9e415-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9e415-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="9e415-110">Создание правила виртуальной сети для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="9e415-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="9e415-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e415-111">PARAMETERS</span></span>

### <span data-ttu-id="9e415-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e415-112">-AsJob</span></span>
<span data-ttu-id="9e415-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9e415-113">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e415-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e415-114">-DefaultProfile</span></span>
<span data-ttu-id="9e415-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9e415-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e415-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e415-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="9e415-117">Создайте правило брандмауэра, прежде чем в виртуальной сети будет включена конечная точка службы виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="9e415-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e415-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e415-118">-ResourceGroupName</span></span>
<span data-ttu-id="9e415-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e415-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e415-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9e415-120">-ServerName</span></span>
<span data-ttu-id="9e415-121">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9e415-121">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e415-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="9e415-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="9e415-123">Имя правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9e415-123">Azure Sql Server Virtual Network Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e415-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="9e415-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="9e415-125">Идентификатор подсети виртуальной сети, указывающий сведения о Microsoft. Network</span><span class="sxs-lookup"><span data-stu-id="9e415-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e415-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e415-126">-Confirm</span></span>
<span data-ttu-id="9e415-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e415-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e415-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e415-128">-WhatIf</span></span>
<span data-ttu-id="9e415-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e415-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e415-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e415-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e415-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e415-131">CommonParameters</span></span>
<span data-ttu-id="9e415-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e415-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e415-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e415-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e415-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e415-134">INPUTS</span></span>

### <span data-ttu-id="9e415-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9e415-135">System.String</span></span>

## <span data-ttu-id="9e415-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e415-136">OUTPUTS</span></span>

### <span data-ttu-id="9e415-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="9e415-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="9e415-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e415-138">NOTES</span></span>

## <span data-ttu-id="9e415-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e415-139">RELATED LINKS</span></span>
