---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8c680cf87deedf5fc4bd8671a60db4329a1f68ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735042"
---
# <span data-ttu-id="112cc-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="112cc-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="112cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="112cc-102">SYNOPSIS</span></span>
<span data-ttu-id="112cc-103">Удаляет правило виртуальной сети Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="112cc-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="112cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="112cc-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="112cc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="112cc-105">DESCRIPTION</span></span>
<span data-ttu-id="112cc-106">Эта команда удаляет правило виртуальной сети Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="112cc-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="112cc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="112cc-107">EXAMPLES</span></span>

### <span data-ttu-id="112cc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="112cc-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="112cc-109">Удаление существующего правила виртуальной сети SQL Server для Azure</span><span class="sxs-lookup"><span data-stu-id="112cc-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="112cc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="112cc-110">PARAMETERS</span></span>

### <span data-ttu-id="112cc-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="112cc-111">-ResourceGroupName</span></span>
<span data-ttu-id="112cc-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="112cc-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="112cc-113">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="112cc-113">-ServerName</span></span>
<span data-ttu-id="112cc-114">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="112cc-114">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="112cc-115">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="112cc-115">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="112cc-116">Имя правила виртуальной сети для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="112cc-116">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="112cc-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="112cc-117">-Confirm</span></span>
<span data-ttu-id="112cc-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="112cc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="112cc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="112cc-119">-WhatIf</span></span>
<span data-ttu-id="112cc-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="112cc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="112cc-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="112cc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="112cc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="112cc-122">-DefaultProfile</span></span>
<span data-ttu-id="112cc-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="112cc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="112cc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="112cc-124">CommonParameters</span></span>
<span data-ttu-id="112cc-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="112cc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="112cc-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="112cc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="112cc-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="112cc-127">INPUTS</span></span>

### <span data-ttu-id="112cc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="112cc-128">System.String</span></span>

## <span data-ttu-id="112cc-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="112cc-129">OUTPUTS</span></span>

### <span data-ttu-id="112cc-130">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="112cc-130">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="112cc-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="112cc-131">NOTES</span></span>

## <span data-ttu-id="112cc-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="112cc-132">RELATED LINKS</span></span>

