---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f4744eee1e93867ea150819a8f4bcadc5ac8a35b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003064"
---
# <span data-ttu-id="8b9ca-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8b9ca-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="8b9ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b9ca-102">SYNOPSIS</span></span>
<span data-ttu-id="8b9ca-103">Получает или перечисляет правило виртуальной SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="8b9ca-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="8b9ca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b9ca-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b9ca-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b9ca-105">DESCRIPTION</span></span>
<span data-ttu-id="8b9ca-106">Эта команда возвращает определенное правило виртуальной SQL Server Azure или список правил виртуальной сети Azure SQL Server под сервером.</span><span class="sxs-lookup"><span data-stu-id="8b9ca-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="8b9ca-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b9ca-107">EXAMPLES</span></span>

### <span data-ttu-id="8b9ca-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b9ca-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="8b9ca-109">Получает одно правило виртуальной SQL Server Azure</span><span class="sxs-lookup"><span data-stu-id="8b9ca-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="8b9ca-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8b9ca-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="8b9ca-111">Получает список правил виртуальной SQL Server Azure для сети, которые находятся под указанным сервером</span><span class="sxs-lookup"><span data-stu-id="8b9ca-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="8b9ca-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8b9ca-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="8b9ca-113">Возвращает список правил виртуальной SQL Server Azure для указанного сервера, которые начинаются с virtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="8b9ca-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="8b9ca-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b9ca-114">PARAMETERS</span></span>

### <span data-ttu-id="8b9ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b9ca-115">-DefaultProfile</span></span>
<span data-ttu-id="8b9ca-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8b9ca-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b9ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b9ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b9ca-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b9ca-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="8b9ca-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8b9ca-119">-ServerName</span></span>
<span data-ttu-id="8b9ca-120">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="8b9ca-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="8b9ca-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="8b9ca-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="8b9ca-122">Имя правила виртуальной сети Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="8b9ca-122">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b9ca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b9ca-123">CommonParameters</span></span>
<span data-ttu-id="8b9ca-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b9ca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b9ca-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b9ca-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b9ca-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b9ca-126">INPUTS</span></span>

### <span data-ttu-id="8b9ca-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8b9ca-127">System.String</span></span>

## <span data-ttu-id="8b9ca-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b9ca-128">OUTPUTS</span></span>

### <span data-ttu-id="8b9ca-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="8b9ca-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="8b9ca-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b9ca-130">NOTES</span></span>

## <span data-ttu-id="8b9ca-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b9ca-131">RELATED LINKS</span></span>
