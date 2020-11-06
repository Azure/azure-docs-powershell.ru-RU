---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 08d14217cff370557009167e09cd7e5396df4e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559436"
---
# <span data-ttu-id="17baf-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="17baf-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="17baf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17baf-102">SYNOPSIS</span></span>
<span data-ttu-id="17baf-103">Создание правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="17baf-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17baf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17baf-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17baf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17baf-105">DESCRIPTION</span></span>
<span data-ttu-id="17baf-106">Создание правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="17baf-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="17baf-107">Правила виртуальной сети используются для подключения сервера Azure SQL Server к определенной виртуальной сети, чтобы ограничить доступ к серверу Azure SQL Server только в пределах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="17baf-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="17baf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17baf-108">EXAMPLES</span></span>

### <span data-ttu-id="17baf-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="17baf-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="17baf-110">Создание правила виртуальной сети для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="17baf-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="17baf-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17baf-111">PARAMETERS</span></span>

### <span data-ttu-id="17baf-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17baf-112">-ResourceGroupName</span></span>
<span data-ttu-id="17baf-113">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="17baf-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="17baf-114">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="17baf-114">-ServerName</span></span>
<span data-ttu-id="17baf-115">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="17baf-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="17baf-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="17baf-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="17baf-117">Имя правила виртуальной сети для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="17baf-117">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="17baf-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="17baf-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="17baf-119">Идентификатор подсети виртуальной сети, указывающий сведения о Microsoft. Network</span><span class="sxs-lookup"><span data-stu-id="17baf-119">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="17baf-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17baf-120">-Confirm</span></span>
<span data-ttu-id="17baf-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="17baf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17baf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17baf-122">-WhatIf</span></span>
<span data-ttu-id="17baf-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="17baf-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17baf-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="17baf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17baf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17baf-125">-DefaultProfile</span></span>
<span data-ttu-id="17baf-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17baf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17baf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17baf-127">CommonParameters</span></span>
<span data-ttu-id="17baf-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17baf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17baf-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17baf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17baf-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17baf-130">INPUTS</span></span>

### <span data-ttu-id="17baf-131">System. String</span><span class="sxs-lookup"><span data-stu-id="17baf-131">System.String</span></span>

## <span data-ttu-id="17baf-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17baf-132">OUTPUTS</span></span>

### <span data-ttu-id="17baf-133">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="17baf-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="17baf-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="17baf-134">NOTES</span></span>

## <span data-ttu-id="17baf-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17baf-135">RELATED LINKS</span></span>

