---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c0e7bc13d52633a1da5bfac2d9aec38ea3d0ee7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561395"
---
# <span data-ttu-id="c6f21-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c6f21-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="c6f21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6f21-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f21-103">Удаляет правило виртуальной сети Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6f21-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6f21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6f21-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6f21-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6f21-105">DESCRIPTION</span></span>
<span data-ttu-id="c6f21-106">Эта команда удаляет правило виртуальной сети Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6f21-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="c6f21-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6f21-107">EXAMPLES</span></span>

### <span data-ttu-id="c6f21-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c6f21-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="c6f21-109">Удаление существующего правила виртуальной сети SQL Server для Azure</span><span class="sxs-lookup"><span data-stu-id="c6f21-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="c6f21-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6f21-110">PARAMETERS</span></span>

### <span data-ttu-id="c6f21-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6f21-111">-AsJob</span></span>
<span data-ttu-id="c6f21-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c6f21-112">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="c6f21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f21-113">-DefaultProfile</span></span>
<span data-ttu-id="c6f21-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c6f21-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>


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

### <span data-ttu-id="c6f21-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6f21-115">-ResourceGroupName</span></span>
<span data-ttu-id="c6f21-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c6f21-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="c6f21-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="c6f21-117">-ServerName</span></span>
<span data-ttu-id="c6f21-118">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6f21-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c6f21-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="c6f21-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="c6f21-120">Имя правила виртуальной сети для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="c6f21-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="c6f21-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6f21-121">-Confirm</span></span>
<span data-ttu-id="c6f21-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c6f21-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6f21-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6f21-123">-WhatIf</span></span>
<span data-ttu-id="c6f21-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c6f21-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6f21-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c6f21-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6f21-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f21-126">CommonParameters</span></span>
<span data-ttu-id="c6f21-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6f21-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f21-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6f21-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f21-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6f21-129">INPUTS</span></span>

### <span data-ttu-id="c6f21-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c6f21-130">System.String</span></span>

## <span data-ttu-id="c6f21-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6f21-131">OUTPUTS</span></span>

### <span data-ttu-id="c6f21-132">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="c6f21-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="c6f21-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6f21-133">NOTES</span></span>

## <span data-ttu-id="c6f21-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6f21-134">RELATED LINKS</span></span>
